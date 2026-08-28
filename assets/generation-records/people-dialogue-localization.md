# Generation record: people-dialogue-localization.png

- Date: 2026-08-28
- Tool: built-in image_gen.imagegen
- Underlying model: not exposed by the tool.
- Type: newly generated static concept image, not a Wan-generated video frame.
- Output: `assets/covers/people-dialogue-localization.png`
- Prompt mapping: `prompts/people-dialogue-localization.md`, entry 01.
- Visual notes: A small pale microphone-stand label in the initial image triggered one targeted edit. Selected image preserves the speaking/listening distinction, two normal microphones and rainy window; no readable screen, caption, logo or watermark. This still does not verify speech, lip synchronization or language performance.

## Complete initial generation prompt

```text
Use case: photorealistic-natural
Asset type: 16:9 cinematic dialogue still concept image for a video prompt collection.
Primary request: Two adult hosts seated across a small desk in a modest community radio studio during rain. The host in a deep green shirt is speaking naturally into a normal broadcast microphone; the other host wearing a brick-red knitted sweater has their mouth closed and listens attentively, looking toward the speaker. Exactly two microphones, one in front of each host, mounted on ordinary plausible stands. Rain-streaked windows are visible through the studio glass behind them.
Style/medium: photorealistic documentary cinema still, natural adult faces, believable skin texture, fabric and acoustic panel detail, authentic everyday radio studio.
Composition/framing: horizontal 16:9 medium two-shot, both faces and microphones clearly separated; natural seated posture and hands quietly resting on the desk. One uninterrupted scene, no split screen.
Lighting/mood: intimate warm studio practical light balanced by cool rainy window light.
Constraints: exactly two adults, only the green-shirt host's mouth is speaking; brick-red-sweater host's lips closed. Exactly two normal microphones with coherent wiring and stands. No captions, no subtitles, no readable screen, no visible text or logos, no watermark, no floating UI, no duplicated fingers or extra limbs.
```

## Complete targeted edit prompt

```text
Use case: precise-object-edit
Edit target: the provided community radio studio image.
Change only the small pale label on the vertical lower section of the microphone stand in front of the host wearing the brick-red sweater: remove this label and every letter or marking there, replacing it with the same plain matte black surface as the rest of the stand. Also keep both microphones entirely unbranded, with no text anywhere.
Preserve everything else exactly: both adult hosts, all facial features, green-shirt speaker with mouth open, red-sweater listener with lips closed, natural hands, both microphone shapes and cables, rainy window, desk, lighting, colors and 16:9 composition. Do not add any object, text, logo, watermark or label.
```
