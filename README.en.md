# cute-baby-photo-illustration

A reusable Agent Skill for turning baby, child and parent-child photos into warm colored-pencil and crayon doodle illustrations.

[中文](README.md) · [Installation](INSTALL.md) · [Prompts](references/prompts.md) · [Validation](VALIDATION.md)

## What this package does

The workflow preserves recognizable features, expression, clothing, pose and important props. It combines finely shaded pencil faces, uneven crayon outlines, pink cheek hatching, visible paper grain and sparse playful decorations.

**This is an instruction package, not an image model or standalone application.** An agent with an existing image-editing tool can follow it to perform an actual edit and review the returned image. A text-only host can provide labeled prompts only. Installation does not provision image capabilities, API credits, credentials or an external service. No executable API client is included.

## Usage

Install the complete folder using [INSTALL.md](INSTALL.md), attach a source photo, then ask:

> Use cute-baby-photo-illustration with classic-crayon on this photo. Preserve the original expression and clothes.

Optional style references must be distinguished from the source photo. The source controls identity and pose; style images guide only visual treatment. Alternatively, provide the instructions and relevant reference files to a capable assistant for one conversation; this is not a global installation.

## Presets

| Preset | Treatment |
|---|---|
| `classic-crayon` | Default: detailed pencil face, grainy outlines, vivid accents |
| `soft-pencil` | Softer pencil work and creamy colors |
| `playful-doodle` | Stronger crayon texture and playful marks |
| `avatar-clean` | Square portrait with fewer decorations |
| `milestone-poster` | Portrait 3:4 layout with room for user-specified text |

The default keeps the source aspect ratio. User instructions take priority over presets, subject to tool capabilities. See [style details](references/style-presets.md) and [tool integration](references/image-tools.md).

## Privacy and license

Three user-supplied reference screenshots informed the generic visual notes. None of those screenshots, source photographs, creator signatures or attachment addresses are included. Keep personal photos and generated results outside this repository. Ignore rules are only a safeguard; review files before publishing.

MIT covers this project's original instructions and documentation. It does not license third-party images, characters or trademarks. See [provenance](references/provenance.md) and [LICENSE](LICENSE).

## Validation status

Static structure and relative-link checks are documented in [VALIDATION.md](VALIDATION.md). No end-to-end baby photo edit was run for this release. Image quality and identity preservation remain dependent on the host tool and require visual acceptance for each output.
