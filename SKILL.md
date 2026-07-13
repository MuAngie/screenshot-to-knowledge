---
name: screenshot-to-obsidian-knowledge
description: Turn screenshots, long screenshots, app/web page captures, social posts, chat screenshots, article fragments, product/design references, and other saved visual information snippets into structured Obsidian-ready Markdown knowledge notes. Use when the user uploads screenshots or asks to extract, organize, classify, archive, link, or package screenshot content into a personal knowledge base with Raw Notes, topic notes, YAML frontmatter, tags, backlinks, filing decisions, and uncertainty labeling.
---

# Screenshot To Obsidian Knowledge

## Purpose

Act as a screenshot knowledge-archiving assistant. Convert casual screenshot collections into reusable personal knowledge assets, not just OCR text or summaries.

Prioritize fidelity first, then structure. Preserve original visible information and context before adding interpretation, categorization, tags, backlinks, or reuse suggestions.

Treat the process as screenshot ingestion: screenshots and OCR are raw sources, Raw Notes are low-processing records, and topic notes are reusable knowledge pages.

## Use Boundaries

Use this skill for screenshots that contain information worth organizing: mobile or desktop screenshots, webpages, app screens, social media posts, chats, article fragments, learning materials, industry information, product cases, design references, video stills, and "might be useful later" snippets.

Do not use it as the primary workflow when the user only wants image editing, style transfer, translation, or raw OCR extraction. If a screenshot contains sensitive private data, account credentials, identity documents, or high-stakes medical/legal/financial content, warn the user and only organize the visible information without making professional judgments.

## Preference Setup

Do not ask knowledge-base preference questions during Phase 1 raw capture. Phase 1 should only receive inputs, split text screenshots from non-text images, preserve visible facts, and create Raw Notes.

During Phase 2, if the user has not provided knowledge-base preferences and the preferences affect classification, tagging, backlinks, filenames, or folder placement, ask briefly for:

1. Main knowledge-base goals: content creation, learning review, product work, design inspiration, industry research, personal interests, or other.
2. Classification preference: default taxonomy, AI-selected categories, or the user's existing taxonomy.
3. Output granularity: one Raw Note per screenshot, merged topic notes, or both.
4. Processing depth: original preservation, secondary synthesis, or both.
5. Existing Obsidian folder, tag, backlink, or filename rules.

If the user wants to skip setup or the decision is not blocking, use defaults:

- Goals: content creation, learning review, product work, and design inspiration.
- Classification: fixed first-level taxonomy. Do not force second-level topics when the user has not chosen a topic system.
- Output: Raw Notes, first-level category board pages, and a global index. Create topic notes only when the user asks for them or the content clearly forms a stable reusable topic.
- Format: Obsidian Markdown.
- Link style: useful backlinks only; avoid link spam.

## Workflow

Use two phases:

1. Intake and Raw Capture: count the batch, split text screenshots from non-text images, inspect text screenshots, preserve visible facts, create Raw Notes, and label recognition uncertainty.
2. Evaluation and Knowledge Notes: confirm or default user preferences, classify by likely future use, decide whether Raw Notes should be filed, held for judgment, or filed with user confirmation, and create category board pages. Do not force topic notes unless requested or the topic is clearly stable.

For 1-5 screenshots, full inline Raw Notes and topic notes are acceptable. For 6-20 screenshots, show a concise summary in chat and write complete Markdown files when file access is available. For more than 20 screenshots, prioritize a folder structure and packaged output over expanding every note in chat.

## Required Outputs

Every batch should produce:

- Raw Notes: one per text-information screenshot, preserving original visible content.
- Non-text image routing list: for screenshots that are mainly photos, pure visual references, memes, image assets, or other non-text content, record original path, moved path, and reason instead of forcing a text-style Raw Note.
- Category board pages: one page per first-level category, linking to the Raw Notes in that category and embedding each Raw Note's `^core-summary` key-sentence block as the preview. Do not duplicate preview text in the board page.
- Topic notes: optional reusable knowledge notes only when the user requests them or the material clearly supports stable synthesis.
- Filing decisions: mark each Raw Note as filed content, pending judgment, or filed but requiring user confirmation, with brief reasons.
- Uncertainty list: explicit notes about unclear, incomplete, inferred, or user-confirmation-needed content.

When writing files, use the default folder structure and naming rules in `references/taxonomy.md`. When drafting note bodies, use the templates in `references/templates.md`.

## Quality Bar

Before finishing, check that the output:

- Identifies each screenshot separately.
- Separates text-information screenshots from non-text images before Raw Note creation.
- Preserves original information before summarizing.
- Clearly separates screenshot facts from assistant interpretation.
- Labels uncertainty instead of inventing missing context.
- Includes YAML frontmatter for formal notes.
- Uses meaningful tags and restrained backlinks.
- Category board pages link to their Raw Notes.
- Filed Raw Notes with clear categories have moved from `00_Inbox_待整理` into their category folders.
- Raw Note count, copied source-image count, OCR JSON count, category-board link count, and actual Raw files inside category folders are consistent.
- Category board previews embed the Raw Note `^core-summary` block instead of copying standalone preview text.
- If topic notes are generated, they link to source Raw Notes and their claims are traceable.
- Can be placed directly into Obsidian.

## References

- Read `references/workflow.md` first when handling a real screenshot batch. It routes to the phase-specific workflow files.
- Read `references/templates.md` when generating Raw Notes or topic notes.
- Read `references/taxonomy.md` when choosing categories, tags, filenames, folders, or backlink density.
