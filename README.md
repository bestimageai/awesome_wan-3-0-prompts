<p align="center"><a href="https://bestimage.ai/"><img src="assets/bestimage-logo.svg" width="72" alt="bestimage.ai logo"></a></p>

# Awesome Wan 3.0 Prompts

**148 video directing briefs across 14 categories, adapted and maintained by the [bestimage.ai](https://bestimage.ai/) team.** Plan a clear event, assign input roles, direct the camera and sound, and inspect continuity before production.

[![Website](https://img.shields.io/badge/bestimage.ai-Website-2563eb)](https://bestimage.ai/)
[![Wan API](https://img.shields.io/badge/Wan_3.0-API-2563eb)](https://bestimage.ai/models/alibaba/wan-3-0-text-to-video/)
[![GPT Image API](https://img.shields.io/badge/GPT_Image_2-API-2563eb)](https://bestimage.ai/models/openai/gpt-image-2/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

English · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Português do Brasil](README.pt-BR.md) · [Italiano](README.it.md) · [العربية](README.ar.md) · [Русский](README.ru.md) · [Bahasa Indonesia](README.id.md) · [ไทย](README.th.md) · [Tiếng Việt](README.vi.md)

![Concept frame for the observatory map-room scene: an archivist opens a star map in dawn light](assets/wan-3-prompt-collection-hero.png)

*Static concept art created with the built-in image generation tool, not a Wan 3.0 video output. See [image prompts and provenance](assets/README.md).*

## Start with a shot you can inspect

1. Choose a brief from the [complete scene index](prompts/README.md).
2. Replace its adjustable details and prepare every listed input. References are roles, not files supplied by this repository.
3. Select the matching route and set duration, ratio, resolution, and sound in that interface. Text alone does not configure an API request.
4. Generate a small trial, then check the visible action, geometry, identity, timing, and sound against the brief's review target.

**148 video directing briefs across 14 categories**. The first six categories contain Chinese directing briefs; the other eight contain English briefs. Fifteen languages have localized entry guides and one shared comparison prompt, **not full translations of all 148 briefs**. Comparison prompts and translated copies are not counted as additional catalog entries.

## Prompt formula

```text
[Output] duration + aspect ratio + medium
[Subject] stable identity or product details
[World] place + time + spatial relationships
[Action] cause → continuous process → visible result
[Camera] framing + one primary move + final position
[Look] light + palette + material
[Sound] ambience + action sound + exact dialogue or silence
[Constraints] unchanged elements + likely scene-specific failures
```

## A complete comparison prompt

**Mode:** Text to Video · **Settings:** 10 seconds, 16:9, sound on · **Inputs:** none

```text
Create a 10-second, 16:9 documentary shot in a quiet community tool library. One adult volunteer with short curly hair, a mustard apron, and a rolled-up navy shirt repairs a small red desk fan while it is unplugged. From 0–3 seconds, the volunteer places the detached protective grille beside the stationary fan. From 3–7 seconds, they wipe dust from one blade with a soft cloth while the camera slides slowly to the right at tabletop height. From 7–10 seconds, they put down the cloth and align the grille with the housing, without plugging in or starting the fan. Window light reveals worn metal and cotton texture. Sound: cloth brushing, one soft grille click, quiet room ambience; no speech or music. Preserve the same person, fan, three blades, red housing, and unplugged cable. No spinning blades, extra tools, readable labels, subtitles, or cuts.
```

**Adjust:** apron color, fan color, room light. **Review:** the fan stays unplugged and still; blade count and hand contact remain consistent. This is a creative concept, not an electrical repair instruction.

## Choose the input route

| Route | Prepare | Direct and verify |
|---|---|---|
| Text to Video | A complete scene description | One event with a cause, intermediate action, and visible result |
| Image to Video | Start **and end** images for the documented bestimage.ai route | Explain the physical transition; lock geometry and composition |
| Reference to Video | Optional identity, object, space, motion, or sound references | Give each asset one role; exclude unwanted details from the reference |
| Video Edit | Source footage plus one bounded change | Preserve the source performance, duration, camera, and all unchanged regions |

These are the routes documented by bestimage.ai, not a claim that every Wan product exposes the same controls. Alibaba's [official Wan 3.0 release material](https://modelstudio.alibabacloud.com/intl/blog/wan3-ai-video-generation-model/) describes longer video, multimodal input, and audiovisual generation. Consult [capabilities and limits](guides/model-capabilities.md) for the distinction between model announcements, platform fields, and untested creative instructions.

## Wan 3.0 API on bestimage.ai

Use the model pages to inspect the current playground and public request examples.

| Model / purpose | English entry |
|---|---|
| Wan 3.0 Text to Video — scenes from written briefs | [Model and API](https://bestimage.ai/models/alibaba/wan-3-0-text-to-video/) |
| Wan 3.0 Image to Video — transitions between designed frames | [Model and API](https://bestimage.ai/models/alibaba/wan-3-0-image-to-video/) |
| Wan 3.0 Reference to Video — identity and multimodal direction | [Model and API](https://bestimage.ai/models/alibaba/wan-3-0-reference-to-video/) |
| Wan 3.0 Video Edit — changes to existing clips | [Model and API](https://bestimage.ai/models/alibaba/wan-3-0-video-edit/) |

Read the [API workflow and cost-control guide](guides/bestimage-wan-3-api.md) for request bodies, polling, input validation, and trial planning. **The bestimage.ai API host is `https://api.flaq.ai`.** Use an API key issued through your bestimage.ai account.

Check the selected model page and your account before spending credits.

## GPT Image 2 API for reference-frame preparation

[GPT Image 2](https://bestimage.ai/models/openai/gpt-image-2/) generates still images; [GPT Image 2 Edit](https://bestimage.ai/models/openai/gpt-image-2-edit/) edits images and combines visual references. Use them to prepare a character sheet, product reference, or an approved starting and ending composition before a Wan video task.

They are **separate image models**, not Wan video endpoints. Export and inspect the stills, then supply suitable images to the selected Wan route. This repository does not automate the handoff or claim that the concept illustrations were generated through those APIs. See the [reference-frame workflow](guides/bestimage-wan-3-api.md#gpt-image-2-reference-frame-workflow).

## Browse all 148 briefs

| Category | Count | What to direct |
|---|---:|---|
| [Cinematic storytelling](prompts/cinematic-storytelling.md) | 8 | Archive discoveries, quiet suspense, spatial transitions |
| [Ads and products](prompts/ads-and-products.md) | 8 | Product mechanisms, materials, pouring, repeatable hero shots |
| [UGC, food and travel](prompts/ugc-food-travel.md) | 8 | Host-led demonstrations, craft visits, food and place |
| [Action and sports](prompts/action-sports.md) | 8 | Contact, momentum, readable lanes, controlled movement |
| [Animation and fantasy](prompts/anime-fantasy.md) | 8 | Ceramic, paper, textile and miniature worlds |
| [Music, comedy and social](prompts/music-comedy-social.md) | 8 | Short performance, comic timing, and loops |
| [Professional business and public service](prompts/professional-business.md) | 13 | Service explainers, accessible communication, operations |
| [Education and science](prompts/education-science.md) | 13 | Demonstration models, observation, cause and effect |
| [Architecture, hospitality and mobility](prompts/architecture-mobility.md) | 13 | Spatial continuity, routes, scale and interior walkthroughs |
| [Production control and editing](prompts/production-control.md) | 13 | Reference roles, local edits, continuity and delivery checks |
| [Commerce, beauty and retail](prompts/commerce-beauty-retail.md) | 12 | Refills, fit, packaging, accessible handling and catalog work |
| [People, dialogue and localization](prompts/people-dialogue-localization.md) | 12 | Speaker turns, pauses, language and listener reactions |
| [Nature, animals and seasons](prompts/nature-animals-seasons.md) | 12 | Non-invasive observation, water, weather and seasonal change |
| [Industrial and manufacturing](prompts/industrial-manufacturing.md) | 12 | Inspection, material flow, guarded equipment and process visuals |

## Selected concept frames

Each still illustrates the first brief in its linked category. A still cannot demonstrate temporal consistency, lip sync, model accuracy, or the safety of a depicted process.

| Product direction | Sports continuity |
|---|---|
| [![Unbranded collapsible travel kettle](assets/covers/product-commercial.png)](prompts/ads-and-products.md) | [![Two track cyclists changing the lead on a velodrome](assets/covers/cinematic-action.png)](prompts/action-sports.md) |

| Ceramic fantasy | Retail refill |
|---|---|
| [![A celadon carp above a pottery workbench](assets/covers/eastern-fantasy.png)](prompts/anime-fantasy.md) | [![Refill pouch pouring soap into an open bottle](assets/covers/commerce-beauty-retail.png)](prompts/commerce-beauty-retail.md) |

| Dialogue | Nature | Industrial inspection |
|---|---|---|
| [![Two community radio presenters taking turns](assets/covers/people-dialogue-localization.png)](prompts/people-dialogue-localization.md) | [![Kingfisher above a rising wetland tide](assets/covers/nature-animals-seasons.png)](prompts/nature-animals-seasons.md) | [![Guarded jar inspection line](assets/covers/industrial-manufacturing.png)](prompts/industrial-manufacturing.md) |

## Guides and contributions

The [prompting guide](guides/prompting-guide.md), [capabilities guide](guides/model-capabilities.md), and [troubleshooting guide](guides/troubleshooting.md) are maintained in Simplified Chinese. The API guide is in English. Localized READMEs identify this coverage instead of implying that every guide is translated.

Read [CONTRIBUTING.md](CONTRIBUTING.md) or [简体中文投稿说明](CONTRIBUTING.zh-CN.md) before sharing a prompt or media. Include exact settings, input roles, rights, observations, and an honest tested/untested status. Never share credentials, private documents, or expiring signed media URLs. Use the [prompt form](.github/ISSUE_TEMPLATE/prompt.yml) to prepare the required submission details.

## About bestimage.ai

This prompt library is curated and maintained by the [bestimage.ai](https://bestimage.ai/) team, connecting practical creative workflows with image and video model APIs.

## Earn with the bestimage.ai Affiliate Program

Build tutorials, share prompts, or publish API integrations? Join the [bestimage.ai Affiliate Program](https://bestimage.ai/affiliate-program/) and earn commissions by introducing your audience to bestimage.ai.

- **20%** on a referred user's first valid paid order.
- **10%** on subsequent valid paid orders made within **60 days after that user registers**.

Order eligibility and payouts follow the [current affiliate agreement](https://bestimage.ai/affiliate-agreement/).

## License

[MIT](LICENSE).
