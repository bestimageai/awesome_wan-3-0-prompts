# Contributing to Awesome Wan 3.0 Prompts

Thank you for helping make this a practical, testable, multilingual Wan 3.0 prompt library. This edition is maintained by the bestimage.ai team. The [guided prompt form source](.github/ISSUE_TEMPLATE/prompt.yml) defines the submission fields. Use this repository's Issues or Pull Requests to contribute. A [Simplified Chinese guide](CONTRIBUTING.zh-CN.md) is also available.

## Good contributions

- A complete original prompt that you tested, plus a useful result or observation.
- A controlled success/failure comparison for identity, motion, camera, sound, physics, or editing.
- A new production scenario that fills a real workflow gap.
- A natural localization that preserves directing intent instead of translating word for word.
- An accessibility, safety, or continuity improvement to an existing prompt.
- An original preview image without third-party brands or rights issues.

## Submit one prompt without editing the repository

Follow the [prompt submission form fields](.github/ISSUE_TEMPLATE/prompt.yml). Submit one prompt per issue and include:

1. A unique, searchable title and short practical use case.
2. The workflow: T2V, I2V with start/end frames, R2V, or video edit; state explicitly whether it was tested.
3. Duration, aspect ratio, resolution, audio setting, and platform when relevant.
4. The exact copy-ready prompt, not a summary or screenshot of the text.
5. A result link, screenshot, or concise result description where possible.
6. The role of every input reference and confirmation that you may share it.
7. Your preferred attribution, or state that you prefer no public attribution.

Never include API keys, private documents, signed URLs, personal customer data, or media you do not have permission to publish.

## Pull requests

Use a pull request for a category, substantial rewrite, guide, translation, or multiple coordinated prompts. Keep each prompt in the existing format:

````markdown
## 01｜Unique, searchable title

**Mode:** T2V · **Settings:** 10 seconds, 16:9, sound on · **Inputs:** none

```text
Complete copy-ready directing brief with action timing, camera, sound, and continuity constraints.
```

**Adjust:** the intended variables. **Review:** the visible result to inspect.
````

In the pull-request description, list the tested route or interface, scope of the change, important observations, and any new assets. Update `prompts/README.md`, the relevant README category table, and `assets/README.md` when the change affects them.

## Prompt quality checklist

- The clip has one main event with a cause, intermediate motion, and visible result.
- Reusable identity or product anchors are explicit and do not change wording between shots.
- The camera has one readable main path per shot and does not cross continuity without explanation.
- Reference roles are explicit: for example, “Image 1 = identity; Video 1 = motion rhythm only.”
- Sound and dialogue identify the source, speaker, language, pause, and silent listener where needed.
- Constraints are specific to likely failures rather than a generic keyword wall.
- The prompt does not promise unverified model limits, safety performance, or medical outcomes.

## Originality and rights

- Do not copy prompt libraries in bulk or replace only the model name, title, or adjectives.
- Do not reuse watermarked media, tracking links, affiliate copy, or promotional language. Retain any required source attribution, original author credit, license notice, and modification note; removing promotion does not remove attribution obligations.
- Do not submit unauthorized celebrity likenesses, protected franchise characters, private people, or imitation of a living artist’s style.
- When public technical material informed a factual claim, link to the primary source and summarize only what the prompt needs.
- By contributing, you confirm that you can share the text and media under this repository’s license.

Maintainers may rewrite accepted submissions for consistency, searchability, safety, and Wan 3.0 workflow clarity. Meaningful contributors can retain attribution unless they request otherwise.

## Translations

- Translate creative intent and production meaning, not source-language word order.
- Keep timecodes, aspect ratios, reference numbers, identity anchors, and immutable details exact.
- Preserve dialogue in the intended language and note regional variant or accent when it materially affects delivery.
- A new language entry should translate the current entry guide, localized prompt formula, and the complete shared comparison prompt. Do not replace it with an older edition or imply the whole catalog is translated.
- Ask a fluent reviewer to check naturalness, safety wording, and regional differences.
- Add the language code and entry link to [the language directory](locales/README.md).

## Review expectations

Maintainers review usefulness, originality, rights, safety, reproducibility, and catalog fit. A submission may be edited, split, moved, or declined with an explanation. Generated output is evidence, not proof that every platform will reproduce the same result.

## Publication and evidence boundaries

The catalog includes untested creative briefs. Mark new ideas as untested until you have real output evidence; never present a static concept image as a Wan-generated video or a benchmark. If you have tested a contribution, include the exact platform, model, settings, input roles, failures, and observation date. For each new image, record its full generation prompt, actual tool, model ID if exposed, edits, and linked catalog entry in `assets/`. Do not fabricate a model ID or copy personal absolute paths into public documentation.
