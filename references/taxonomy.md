# Taxonomy, Tags, Links, And Files

## Default Categories

Use one primary category for each formal topic note. Raw Notes can remain in `00_Inbox_待整理` only until classification is clear. Once a Raw Note has a clear first-level category, move it into that category folder and update its filing status.

```md
00_Inbox_待整理
01_选题与内容素材
02_读书学习
05_AI产品经理
06_商业案例
07_方法论
09_可用工具和网页
10_生活内容
11_旅行
12_待判断
```

## Category Guide

- `00_Inbox_待整理`: temporary holding area for raw screenshots whose value, source, or destination is not yet clear. Do not leave already-classified Raw Notes here.
- `01_选题与内容素材`: content ideas, titles, topics, writing directions, 小红书/video/article hooks, copy material, scripts, prompts, literary/文艺 excerpts, art/exhibition notes, and reusable case素材. If unsure whether “灵感” should be separate, merge it here.
- `02_读书学习`: books, reading notes, book fragments, course material, exam-prep material, concepts, explanations, and study material. Use this for the learning material itself, not for methods about how to learn.
- `05_AI产品经理`: AI PM interviews, AI agents, AI applications, AI product opportunities, and AI project resume material.
- `06_商业案例`: business models, growth cases, brand cases, marketing cases, and company cases.
- `07_方法论`: thinking frameworks, analysis models, workflows, review methods, and communication methods.
- `09_可用工具和网页`: useful tools, websites, online services, browser pages, software references, resource directories, and links worth revisiting.
- `10_生活内容`: daily life information, personal routines, health habits, home matters, consumption references, errands, family or social-life notes.
- `11_旅行`: trip ideas, itineraries, destinations, routes, hotels, restaurants, transportation, travel notes, and travel planning material.
- `12_待判断`: incomplete or ambiguous material that needs user confirmation.

## Classification Rules

Classify by likely future use, not by surface content alone.

Purpose beats surface format. Do not over-weight where the screenshot came from, how it looks, or whether it resembles a social post, prompt snippet, or content note. First decide what the user will most likely use the information for:

- Reading or studying the material itself -> `02_读书学习`.
- Planning a trip, route, destination, hotel, restaurant, or attraction -> `11_旅行`.
- AI-assisted product work, competitor analysis, industry research, monitoring scripts, or knowledge-system workflows -> `05_AI产品经理`.
- Reusable writing, expression, hooks, literary material, art/exhibition notes, or content素材 -> `01_选题与内容素材`.

Use platform style only as secondary evidence. A Xiaohongshu-style travel note is still travel if its future use is itinerary planning. A prompt-looking competitor-analysis workflow is still AI/product work if its future use is AI-assisted research or PM work.

Examples:

- 小红书 screenshot used for title imitation -> `01_选题与内容素材`.
- Reusable prompt, copy, title, or script fragment -> `01_选题与内容素材`.
- 文学、文艺、祝福文字、情绪表达、艺术展览、看展记录、作品解读 -> `01_选题与内容素材`.
- Book cover, book excerpt, course note, exam-prep note, or learning material itself -> `02_读书学习`.
- AI Agent article used for job interviews -> `05_AI产品经理`.
- AI prompt/workflow for competitor teardown, industry intelligence, market monitoring, weekly reports, or product research -> `05_AI产品经理`, even if it appears inside a social-media post.
- Industry trend screenshot used for AI product work -> `05_AI产品经理`; if it is only a general webpage/resource to revisit, use `09_可用工具和网页`.
- Useful website, SaaS product page, online tool, or resource list -> `09_可用工具和网页`.
- Recipe, fitness note, purchase reference, or household information -> `10_生活内容`.
- Destination, route, hotel, food guide, or travel itinerary -> `11_旅行`.

If no future use is clear, use `12_待判断` and ask for confirmation in the MOC.

## Priority Classification Rules

Apply these before ordinary keyword matching.

1. Sensitive health/private records first:
   - Medical reports, lab reports, identity numbers, doctors, hospitals, test results, blood/serum/glucose/reference ranges -> `10_生活内容`.
   - Filing decision should usually be `入库但需用户判断`.
   - Do not classify as business just because the screenshot contains a hospital vendor or company name.
2. Low-quality OCR first:
   - If OCR is mostly broken symbols, short fragments, or impossible text, use `12_待判断`.
   - Add tags such as `OCR低置信度` and `视觉素材待确认`.
   - Do not let an isolated OCR fragment such as `ai` trigger `05_AI产品经理`.
3. Literary/art material:
   - “愿你…”, blessings, poetic language, literary excerpts, art exhibitions, artists, galleries, artworks, sculpture, painting, exhibition commentary -> `01_选题与内容素材`.
4. Reading/study material:
   - Books, book names, course notes, exam-prep materials, concepts, explanations, and study content itself -> `02_读书学习`.
   - Methods about reading, prompting AI to read, or creating a learning workflow -> `07_方法论`, not `02_读书学习`.
5. Travel requires context:
   - City names such as 北京、上海、东京 do not classify as travel by themselves.
   - Use `11_旅行` only when city/destination terms appear with route, itinerary, hotel, ticket, scenic spot, restaurant, map, food guide, or travel planning context.

## Category Boundary Rules

### `05_AI产品经理`

Use for AI product understanding and AI PM work:

- AI Agent/RAG/LLM product mechanics.
- AI product design, AI PM interviews, AI product jobs, model selection, AI application strategy.
- Product decisions around AI workflows, permissions, UX, data, pricing, risk, or business fit.

Do not use `05` for general AI tools, GitHub projects, prompts, or broken OCR.

### `07_方法论`

Use for reusable ways of doing work:

- Methods, processes, frameworks, SOPs, PRD/MRD/BRD structures, requirements analysis, competitor analysis.
- Prompting methods, learning methods, reading workflows, “how to ask AI”, “how to use Codex”.
- Step-by-step material where the future value is the procedure.

### `09_可用工具和网页`

Use for resources to open, collect, install, or use:

- Tools, websites, GitHub projects, Skill lists, plugins, software references, useful links.
- AI tool lists and online generators.
- “Create an HTML learning website” can be `09` if the future value is the generated tool; use `07` if the future value is the prompt/workflow method.

### Weak Keyword Warnings

Never classify from these weak keywords alone:

- `公司` does not imply `06_商业案例`.
- `购物` does not imply `10_生活内容`; it may appear in art/environmental text.
- `北京` / `上海` / `东京` do not imply `11_旅行`.
- Isolated OCR fragments like `ai`, `A7`, or mixed Latin noise do not imply `05_AI产品经理`.

## Information Value Fields

Use these controlled values where helpful:

```md
信息类型：观点 / 案例 / 数据 / 方法 / 灵感 / 问题 / 工具资源 / 网页资源 / 行业知识 / 内容素材 / 生活信息 / 旅行信息 / 待判断
可复用价值：高 / 中 / 低 / 待判断
适合用途：写作 / 面试准备 / 竞品分析 / 个人灵感 / 学习复盘 / 项目资料 / 工具收藏 / 生活参考 / 旅行规划
入库判断：入库内容 / 待判断内容 / 入库但需用户判断
```

## Filing Decisions

Use filing decisions to decide how far a Raw Note should be processed.

- `入库内容`: Use when the Raw Note is readable, has clear preservation value, and can support future writing, learning, competitor analysis, interview preparation, inspiration, tool collection, life reference, travel planning, or project material.
- `待判断内容`: Use when text is unreadable, OCR is incomplete, context is severely missing, the main information cannot be judged, or preservation value is unclear.
- `入库但需用户判断`: Use when the content has preservation value but involves sensitive information, professional-judgment boundaries, multiple plausible categories, or naming/linking choices that materially affect later organization.

Do not force every Raw Note into a topic note. A good screenshot knowledge base preserves low-confidence material without over-synthesizing it.

## Tag Rules

Use concise Chinese tags. Raw Notes usually need 2-5 tags. Topic notes usually need 3-8 tags.

Good examples:

```md
#AI产品经理
#小红书
#内容选题
#内容素材
#产业知识
#可用工具
#网页资源
#生活内容
#旅行
#竞品分析
#读书学习
#方法论
#文艺表达
#艺术展览
#健康信息
#隐私待确认
#OCR低置信度
```

Avoid redundant tag clusters such as:

```md
#AI
#人工智能
#智能AI
#AI产品
#AI产品经理
#人工智能产品经理
```

Prefer a smaller set:

```md
#AI产品经理
#AI产品
#内容素材
```

## Backlink Rules

Backlinks must be meaningful. Do not create links just to increase density.

Default limits per topic note:

- 上级分类：1-3 links.
- 强相关主题：3-5 links.
- 延伸主题：0-3 links.

Avoid vague links unless the user explicitly uses them as vault indexes:

```md
[[知识]]
[[内容]]
[[信息]]
[[学习]]
[[想法]]
```

## Naming Rules

Raw Note filenames:

```md
screenshot_001_raw.md
screenshot_002_raw.md
YYYY-MM-DD_主题_raw.md
```

Topic note filenames:

```md
AI产品经理面试题回答框架.md
小红书爆款标题结构.md
实用AI网页工具清单.md
东京三日旅行路线.md
家庭常备药整理.md
```

## Folder Structure

Default output folder:

```md
/Obsidian_Knowledge_Output
  /00_Inbox_待整理
  /01_选题与内容素材
  /02_读书学习
  /05_AI产品经理
  /06_商业案例
  /07_方法论
  /09_可用工具和网页
  /10_生活内容
  /11_旅行
  /12_待判断
  /_NonText_Images_待整理
```

`_NonText_Images_待整理` 用于存放主要内容不是文字信息的照片、纯视觉参考、无文字图片、表情包、场景图或图片素材。此文件夹中的图片不在 Phase 1 强行生成文字型 Raw Note；移动图片时需要记录原始路径和移动后路径，交付时告知用户已移动的文件清单。
