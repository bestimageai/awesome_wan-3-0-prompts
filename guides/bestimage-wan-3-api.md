# Wan 3.0 API workflow on bestimage.ai

Maintained by the [bestimage.ai](https://bestimage.ai/) team. This guide covers Wan 3.0 API requests, input preparation, polling, and cost control. [Back to the library](../README.md)

## Documentation and API host

Use the [Wan 3.0 documentation](https://bestimage.ai/docs/?page=api%2Fwan-3-0) and the selected model page to verify current fields before calling the service. **`https://api.flaq.ai` is the API host for bestimage.ai**, used for both submission and polling. Use an API key issued through your bestimage.ai account and keep it outside public files.

Check availability, account permissions, input requirements and pricing for your selected model and region before starting a generation.

## Choose one of four routes

| Model ID | Input role | English model page |
|---|---|---|
| `wan-3.0-text-to-video` | Written scene and output settings | [Text to Video](https://bestimage.ai/models/alibaba/wan-3-0-text-to-video/) |
| `wan-3.0-image-to-video` | Required start **and end** images | [Image to Video](https://bestimage.ai/models/alibaba/wan-3-0-image-to-video/) |
| `wan-3.0-reference-to-video` | Prompt and optional multimodal references | [Reference to Video](https://bestimage.ai/models/alibaba/wan-3-0-reference-to-video/) |
| `wan-3.0-video-edit` | Source footage and a bounded edit | [Video Edit](https://bestimage.ai/models/alibaba/wan-3-0-video-edit/) |

All four use `POST /api/v1/video/task`, then `GET /api/v1/video/{task_id}` with bearer authentication. These are platform-specific identifiers; Alibaba's native model ID `wan3.0-video` and native `media` request shape are not interchangeable with this wrapper.

### Shared request fields

| Field | API contract |
|---|---|
| `model_name` | One of the four route IDs above |
| `prompt` | Scene, action, camera, sound or edit instruction |
| `duration` | Output duration from 2 to 30 seconds; additional edit limits apply |
| `resolution` | `480p`, `720p`, `1080p` |
| `aspect_ratio` | `16:9`, `9:16`, `1:1`, `4:3`, `3:4` |
| `sound` | Optional boolean; documented default is `true` |
| `seed` | Optional integer from 0 to 2147483647 |

The durations in the catalog are creative settings, not guarantees of exact action timing. A requested camera move, identity lock, translation, sign, or physical effect must still be reviewed in the actual output. Reusing a seed does not guarantee identical results across model or platform revisions.

### Input limits that are easy to miss

- **Image to Video:** both `image_url` and `image_end_url` are required by the bestimage.ai API. Prepare a physically plausible transition between them. Do not silently submit a one-frame recipe as this two-frame route.
- **Images:** JPEG, JPG, PNG without alpha, BMP, or WebP; each side 240–8000 pixels in the documentation.
- **Video Edit:** `video_url` is an MP4 or MOV clip, at most 15 seconds, each side 240–4096 pixels. **Source duration plus requested output duration must not exceed 30 seconds.** A 10-second source and 10-second output total 20 seconds.
- **Reference to Video:** up to 10 `images`, 5 `videos`, and 5 `audios`. Each reference video or audio clip is 1–15 seconds. **The video collection totals at most 15 seconds, and the audio collection separately totals at most 15 seconds.** Five 15-second clips do not satisfy that combined limit.
- Reference videos use MP4/MOV and the dimensions above; reference audio uses WAV/MP3.
- `files` accepts at most one documented office, PDF, text, or Markdown file URL. PDF, Word, PowerPoint, Keynote, and Pages documents have a documented 50-page limit. Check the current page for exact supported extensions.
- `links` accepts at most one public webpage. **`files` and `links` cannot be sent together.** The documentation distinguishes domestic and overseas webpage access. Do not assume a login-protected or regional URL can be parsed.
- References must be reachable by the service and authorized for the intended use. Do not publish private documents, credentials, customer information or temporary signed URLs in a contribution. Do not make private data public just to satisfy URL access.

## Submission and bounded polling example

The following JavaScript uses Node's built-in `fetch`; no library installation is required on a compatible runtime. Set `BESTIMAGE_API_KEY` in your own environment using a key issued through your bestimage.ai account. Never paste a key into a public file or issue.

```javascript
// Usage: save as wan-example.mjs, then run: node wan-example.mjs
// Prerequisite: set BESTIMAGE_API_KEY locally using a key from your bestimage.ai account.
// Running this example submits one paid/credit-consuming task according to your account terms.
const API_BASE = 'https://api.flaq.ai';
const API_KEY = process.env.BESTIMAGE_API_KEY;
if (!API_KEY) throw new Error('Set BESTIMAGE_API_KEY locally before running.');

async function request(path, options = {}) {
  const response = await fetch(`${API_BASE}${path}`, {
    ...options,
    headers: {
      'Content-Type': 'application/json',
      Authorization: `Bearer ${API_KEY}`,
      ...options.headers,
    },
    signal: AbortSignal.timeout(30000),
  });
  if (!response.ok) throw new Error(`HTTP ${response.status}: inspect the response privately.`);
  const body = await response.json();
  if (body.code !== 0 || !body.data) {
    throw new Error(body.message || 'Unexpected API response.');
  }
  return body.data;
}

// Submit once. Do not automatically resubmit after an ambiguous timeout.
const submitted = await request('/api/v1/video/task', {
  method: 'POST',
  body: JSON.stringify({
    model_name: 'wan-3.0-text-to-video',
    prompt: 'Create a 10-second documentary shot of an adult archivist unfolding one star map on a wooden table at dawn. Slide the camera slowly to the right. Preserve the paper, hands, brass lamp, and room. Sound: paper and distant birds. No text, music, or cuts.',
    duration: 10,
    resolution: '720p',
    aspect_ratio: '16:9',
    sound: true,
    seed: 42,
  }),
});
const taskId = submitted.task_id;
if (typeof taskId !== 'string' || !taskId) throw new Error('Missing task_id; check the account history before retrying.');
console.log('Save this task ID:', taskId);

async function waitForVideo(id) {
  for (let attempt = 0; attempt < 60; attempt += 1) {
    const task = await request(`/api/v1/video/${encodeURIComponent(id)}`);
    if (task.task_status === 'succeed') {
      const videoUrl = task.task_result?.videos?.[0]?.url;
      if (!videoUrl) throw new Error('Task succeeded but no video URL was returned.');
      return videoUrl;
    }
    if (task.task_status === 'failed') {
      throw new Error(task.task_status_msg || 'Video task failed.');
    }
    if (!['submitted', 'processing'].includes(task.task_status)) {
      throw new Error(`Unexpected task status: ${task.task_status}`);
    }
    await new Promise((resolve) => setTimeout(resolve, 5000));
  }
  throw new Error(`Polling stopped after 60 checks. Task ${id} may still be running; do not submit a duplicate.`);
}

const videoUrl = await waitForVideo(taskId);
console.log('Review the returned video:', videoUrl);
```

The request timeout and polling limit are client safeguards, not service time guarantees. A 429, authentication failure, network error, unknown status or malformed response stops this example. Inspect the task or account history before retrying; a network error after submission does not prove that the task was never created. Record the returned task ID before further processing. Do not follow an arbitrary returned `response_url` with your bearer key; the example polls the documented host explicitly.

## Route-specific request bodies

Replace the example media URLs below with your own authorized, service-reachable assets. `example.com` URLs are placeholders for input media, **not working sample files**. These bodies use the same submission and polling flow above.

### Image to Video

```json
{
  "model_name": "wan-3.0-image-to-video",
  "prompt": "Preserve the travel kettle, tabletop, hands, and lighting. The upper hand lifts the handle while the lower hand holds the base; the silicone body unfolds continuously into the end-frame shape. No new parts, heating, or text.",
  "image_url": "https://example.com/authorized-start.jpg",
  "image_end_url": "https://example.com/authorized-end.jpg",
  "duration": 10,
  "resolution": "720p",
  "aspect_ratio": "16:9",
  "sound": true,
  "seed": 42
}
```

### Reference to Video

```json
{
  "model_name": "wan-3.0-reference-to-video",
  "prompt": "Image 1 defines only the adult performer's identity and clothing. Image 2 defines only the rehearsal room. Video 1 defines only sitting and standing timing, not its person or background. Generate a new 12-second static-camera scene with one chair and continuous foot contact.",
  "images": ["https://example.com/authorized-person.jpg", "https://example.com/authorized-room.jpg"],
  "videos": ["https://example.com/authorized-motion.mp4"],
  "duration": 12,
  "resolution": "720p",
  "aspect_ratio": "16:9",
  "sound": true,
  "seed": 42
}
```

This example intentionally does not include a reference file or webpage. When one is useful, add either `files` or `links` according to the current interface, never both. Source video and audio duration totals must be checked before submission; a brief's output duration does not tell you the input total.

### Video Edit

```json
{
  "model_name": "wan-3.0-video-edit",
  "prompt": "Change only the exterior weather through the office windows to light drizzle. Preserve the people, gestures, furniture, camera, cuts, and ten-second duration. Keep rain outside the glass; do not alter the meeting or add text.",
  "video_url": "https://example.com/authorized-ten-second-source.mp4",
  "duration": 10,
  "resolution": "720p",
  "aspect_ratio": "16:9",
  "sound": false,
  "seed": 42
}
```

This body assumes a ten-second source, so source plus output totals twenty seconds. Measure the real source first. Exact lip-sync replacement, pixel-perfect masks, guaranteed voice preservation, and frame-accurate dubbing are not established by these examples; do not present the generic edit route as a verified specialist tool.

## GPT Image 2 reference-frame workflow

[GPT Image 2](https://bestimage.ai/models/openai/gpt-image-2/) creates still images. [GPT Image 2 Edit](https://bestimage.ai/models/openai/gpt-image-2-edit/) modifies images and combines approved references. Consult the [separate image API documentation](https://bestimage.ai/docs/?page=api%2Fgpt-image-2). Neither is a Wan video model.

1. Write a still-image brief that defines subject identity, object geometry, composition, and light. A useful example is the collapsed travel kettle at the beginning of [product brief 01](../prompts/ads-and-products.md).
2. Generate and review a starting still with the image route, then use the edit route or another approved process to prepare a compatible end frame. This is a suggested manual workflow, not an implemented pipeline.
3. Check actual dimensions, format, transparency, rights, geometry, and the physical plausibility of the transition. An attractive start and end pair may still be impossible to connect continuously.
4. Supply the approved images to Wan's documented I2V route, or give references distinct roles in R2V. Inspect the resulting video independently.

The image API documentation uses `POST /api/v1/image/task` and `GET /api/v1/image/{task_id}`, with the same publicly documented request host. Its body differs from the video body:

```json
{
  "model_name": "gpt-image-2",
  "prompt": "A realistic still of an unbranded collapsed travel kettle on a slate-gray tabletop, gray-white silicone body, coral handle, rigid white base, soft side light, no text or logos.",
  "width": 16,
  "height": 9,
  "resolution": "1k",
  "quality": "medium"
}
```

In this contract, `width` and `height` are **ratio values**, not pixel dimensions. The example requests 16:9, not a 16×9-pixel image. The edit route uses `model_name: "gpt-image-2-edit"` and requires `image_url_list` with 1–16 images in the documentation; do not substitute Wan's `images` or `image_url` fields. Verify current image resolution and quality choices on the linked page.

For the eight concept illustrations in this library, see the [image prompts and generation details](../assets/README.md).

## Cost control without inherited price claims

- Check the selected route and account's current displayed unit, price, minimum charge, failure policy, and any promotion before submitting.
- For a rate quoted per output second, a rough planning calculation is `planned output seconds × current displayed rate × planned attempts`. This is not an invoice formula; account terms and input billing may differ.
- Start with a short test at an appropriate lower resolution, then review action, identity, geometry, and sound before requesting more attempts.
- Change one creative variable at a time. Record the prompt, references, seed, settings and model revision when available; do not claim the seed makes the experiment deterministic.
- Increase quality only for approved concepts. Keep a human approval step before any larger batch.
- Record failures and preserve task IDs. Do not resubmit automatically because polling is slow.

No fixed prices, discounts, coupons, affiliate commissions, refunds or generation-speed promises are stated here. If a platform field is unavailable or the account does not support a workflow, stop and confirm the intended route rather than silently substituting another model.
