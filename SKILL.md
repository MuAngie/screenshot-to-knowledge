---
name: screenshot-to-obsidian-knowledge
description: Convert screenshots and saved visual captures into traceable Obsidian Raw Notes, category boards, and optional topic notes. Use for screenshot OCR, extraction, classification, archiving, linking, uncertainty handling, or knowledge-base packaging.
---

# Screenshot To Obsidian Knowledge

## Core Rules

- Preserve visible facts before interpreting them. Never invent cropped, blurred, or missing context.
- Copy every processed image to the output directory's `_Source_Images/YYYY-MM` while keeping the source file unchanged.
- For each text-information screenshot, create one Raw Note and embed its copied image.
- For each non-text image, record the original path, copied path, and routing reason; do not create a text-style Raw Note.
- Keep screenshot facts, OCR uncertainty, and assistant synthesis visibly separate.
- For sensitive or high-stakes content, organize only the visible information and avoid professional judgments.

## Defaults

- Ask preference questions only when the answer would materially change classification, naming, folders, tags, or links. Never interrupt Phase 1 for preferences.
- Use the default first-level taxonomy when no user taxonomy is available.
- Always create Raw Notes, category boards, and a global index. Create topic notes only when requested or when a stable reusable topic is clearly supported.
- Deliver exactly one `YYYY-MM_截图整理索引.md` per batch. It serves as both the batch index and the image copy/routing manifest; do not keep a second standalone Markdown copy list for the same batch.
- Keep backlinks meaningful and sparse.
- In Raw Note frontmatter, keep necessary operational metadata but omit `type`, `title`, `source_type`, and `source_platform`. Topic notes may keep `type: knowledge_note`. Put the readable title in the filename and H1; record visible platforms in the body. Follow an explicit user schema instead.

## Process

1. Run `references/phase-1-intake-raw-capture.md` to count, route, copy, read, preserve, and capture screenshots.
2. Run `references/phase-2-evaluation-knowledge-notes.md` to evaluate, classify, file, build boards, and optionally synthesize topics.

For 1-5 screenshots, inline output is acceptable. For 6-20, summarize in chat and write complete files. For more than 20, prioritize a complete folder package and concise handoff.

## Deliverables

- One Raw Note per text-information screenshot.
- One combined batch index: group text screenshots by category, embed both `![[raw_note#^keywords]]` and `![[raw_note#^core-summary]]` for every Raw Note, link every non-text image with its routing reason, and include a copy/routing manifest covering all processed images.
- One board page per populated first-level category, embedding both `![[raw_note#^keywords]]` and `![[raw_note#^core-summary]]`.
- A shallow global index linking category boards.
- Filing decisions and an uncertainty list.
- Optional traceable topic notes.

## Completion Checks

- Every processed image is copied exactly once to `_Source_Images/YYYY-MM`, and every source file remains unchanged.
- Processed-image count = copied-image count = copy-manifest count, and every copied path exists.
- Text-screenshot count = Raw Note count = OCR JSON count = keyword-preview count = core-summary-preview count; non-text-image count = routing-reason count.
- Every Raw Note in the batch index has both previews; every non-text image has a resolvable image link and routing reason; copy-manifest rows equal the processed-image count.
- After a full two-phase run, do not retain a separate `YYYY-MM_图片复制与分流清单.md`. If Phase 1 created one as an intermediate artifact, delete it only after validating the combined batch index.
- Filed Raw Notes are in their category folders; unresolved classification alone uses `12_待判断`.
- Raw Notes preserve source facts, uncertainty is explicit, and frontmatter follows the property rule above.
- Board links resolve; topic-note claims link back to source Raw Notes.

## References

- Read `references/templates.md` when writing notes or indexes.
- Read `references/taxonomy.md` when classifying, tagging, naming, filing, or linking.
