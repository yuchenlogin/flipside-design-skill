---
name: flipside-design
description: Apply the FLIPSIDE print-workshop aesthetic to presentations, websites, interfaces, motion graphics, and visual storytelling. Use when the user invokes flipside-design, 翻面美学, 印刷工坊美学, or asks to reuse the visual language of the referenced FLIPSIDE video. This is an aesthetic layer over the requested deliverable, not a requirement to turn every task into a game or a website.
metadata:
  version: "1.0.0"
  source-reviewed: "2026-10-29"
---

# 翻面 · 印刷工坊美学

Create clear, purposeful work that feels assembled from paper, ink, prints, instruments, and a small physical world. Combine disciplined information hierarchy with tactile materials and spatial transitions. Preserve the user's subject, facts, language, medium, and explicit constraints.

## Start with the reference, then choose a treatment

Before designing, read [visual-system.md](references/visual-system.md). Inspect these bundled source frames with an image-viewing tool:

- [Print settings](references/frames/0028.4-print-settings.jpg): information hierarchy, calibration marks, paper, annotation.
- [Shop board](references/frames/0069.0-shop-board.jpg): collection/detail layout, type roles, selective emphasis.
- [Home](references/frames/0019.4-home.jpg): warm light, cool enclosure, framed scene, stable navigation.

For motion, also read [motion.md](references/motion.md) and inspect the source sequence matching the intended action. For a return visit where these references are already in context, do not reload them needlessly.

Use [composition-components.md](references/composition-components.md) for layouts and states; [media-adaptation.md](references/media-adaptation.md) for the requested medium. Read [evidence.md](references/evidence.md) when explaining the source, checking a disputed feature, or choosing a less familiar motif.

Apply the appropriate presentation, document, website, or other production workflow when available. This skill supplies aesthetic decisions; it does not replace file-format requirements, factual verification, responsive implementation, or the user's requested output. Choose a workflow that supports that output: an HTML slide request stays HTML even if another presentation workflow defaults to PPTX.

## The visual grammar

1. **Paper and dark enclosure work together.** Warm ivory reading surfaces sit against ink, navy, wood, or a cool shadow field. A page may be predominantly light or dark. Color has a structural role.
2. **Images look drawn and printed.** Use articulate dark contours, simplified hard-edged light/shadow, selective halftone or hatching, and restrained wear. Photographs and scientific images may retain their original appearance inside a print-like frame.
3. **Typography has distinct jobs.** Heavy Chinese sans for navigation and strong headings; Song/Ming-style serif for selected editorial names; condensed Latin/numerals for display numbers and labels; calm, legible text for explanation. Use the substitution guidance, not an invented identification of the original fonts.
4. **Order carries information; imperfection carries material.** Align columns, labels, charts, and text rigorously. Put small irregularities in edges, ink, or one physical object, rather than randomly rotating the whole interface.
5. **A useful object explains the function.** Choose a specimen, proof sheet, archive, optical comparator, register, map, or workbench when it helps the content. Keep the chosen metaphor coherent within the scene.
6. **Motion describes a change.** A roll reveals a new surface; a hinge reveals another side; a push-in enters a selected detail; a transfer moves content from its source to its destination; a stamp confirms a completed state.
7. **Navigation stays dependable.** The source repeatedly anchors section identity at the upper left, context at the upper right, secondary controls along an edge, and a primary action near the lower right. Translate that hierarchy to the medium; do not mechanically copy screen coordinates.

## Decide before producing

Resolve these choices from the request; ask only if a missing answer materially changes the work:

- **Content:** what must the audience understand or do first?
- **Container:** light proof sheet, dark exhibition/workshop, or alternating chapter/content scenes?
- **Metaphor:** choose one useful organizing object, or use neutral editorial structure if an object adds no clarity.
- **Type:** heading, body, editorial accent, numeric roles; usually two main families plus an optional numeric face.
- **Intensity:** quiet, balanced, or expressive, as defined in `media-adaptation.md`.
- **Motion:** none for static output; otherwise select actions according to meaning and hierarchy.

Write these decisions into the working design notes or explain them briefly when useful. Do not burden the user with a preliminary questionnaire or insert process notes into the final product.

## Tokens and implementation freedom

[design-tokens.json](assets/design-tokens.json) and [flipside-tokens.css](assets/flipside-tokens.css) are a reusable starting palette and scale, designed from the observations. They are **recommended implementation values**, not recovered source code or exact original parameters.

- Preserve the relationships among paper, ink, navy, rust, and secondary accents; adapt values for projection, contrast, brand constraints, or existing UI.
- Use real text, semantic controls, and vector shapes for editable information. Use images for material and illustration.
- Maintain a clear reading layer above texture. Keep plots, formulas, code, and small text clean.
- Build original content. Bundled reference images are analysis references, not background assets to paste into unrelated deliverables.

## Evidence discipline

The reference is a 10:27.53 public video, inspected at 768 × 480 and 30 fps. Still timestamps are from decoded frames; motion sheets sample every 0.2 s. The exact font files, rendering implementation, animation curves, and original design-token values were not available.

Keep three categories separate: **observed source behavior**, **interpretation of that behavior**, and **new adaptation rules**. In particular:

- The color-vision controls are accessibility simulations, not theme-palette options.
- The source mixes object-like interfaces with screen-space controls; do not label all of it purely diegetic.
- Regular editorial motion is present. Do not claim that the source uses low-frame-rate stop motion, pervasive jitter, chromatic misregistration, or a particular shader without further evidence.
- Preserve literal data accuracy. A decorative coin pile in the source is not evidence of a valid quantitative encoding.

## Finish with a visual check

Judge the rendered result at its intended viewing size:

- Can the audience find the main point or action before noticing the texture?
- Are paper/ink/cool shadow roles recognizable without every page sharing one layout?
- Do typography, materials, and illustrations belong together?
- Does a metaphor make the information easier to understand?
- Are selected, hovered, owned/completed, and disabled states distinguishable where relevant?
- Is motion motivated, finite, and quieter for frequent actions than for chapter transitions?
- Do small text, charts, equations, and keyboard/touch controls remain usable? Check plotted mark geometry against axes and values, not just the displayed numbers.
- Does the work avoid drifting into generic sepia vintage, neon cyberpunk, glossy glass UI, or a three-card template on every page?

Use the user's actual task to validate the result. Do not generate unrelated showcase pages, publish anything, install fonts, or add sound solely because this skill was invoked.
