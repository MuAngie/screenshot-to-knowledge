# Markdown Templates

Use these templates for Obsidian-ready output. Preserve headings unless the user's own knowledge-base conventions require different names.

## Raw Note

```md
---
title: 截图 001 原始记录
type: raw_screenshot
source_type: screenshot
source_platform: 未记录
created: YYYY-MM-DD
status: 待归档
confidence: medium
category_suggestion:
  - 00_Inbox_待整理
tags:
  - 截图
  - 待整理
source_file: 原始截图路径
---

# 截图 001 原始记录

## 0. 原图

![[_Source_Images/YYYY-MM/原图文件名.PNG]]

## 1. 截图基本信息

- 截图编号：001
- 可见来源：
- 画面类型：
- 主要语言：
- 信息密度：高 / 中 / 低
- 识别置信度：high / medium / low

## 2. 原始文字识别

> 尽量保留截图中的原文。
> 如果无法完整识别，需要标注缺失或模糊。
> 可以清理中文字符之间和中文标点附近的多余 OCR 空格，但不要改写原意；英文、URL、代码、文件名和产品名中的空格要保留。

## 3. 主要内容整理

把 Raw Note 中可读信息整理成可以直接阅读的完整内容。不要只是取 OCR 前几行做摘要；应基于完整 OCR 和画面上下文，排除明显状态栏、按钮、纯符号、过短碎片、乱码和不合理误读，保留相对连续、可理解的信息。

如果截图中有明显结构标记，例如 `1.`、`1、`、`一、`、`第一点`、`第一步`、`Step 1`，优先整理成分点或步骤段落。

撰写时先判断内容类型，再选择组织方式：

- 文章、观点、文学文艺片段：按原文逻辑整理为连贯段落，保留表达重点，不改写成商业分析。
- 方法、流程、教程：按“背景/目标/步骤/注意点/适用场景”组织，能分步就分步。
- 报告、体检、订单、账单、个人资料：按事实字段整理，不做专业结论，不扩展成行业或商业判断。
- 工具、网页、资源清单：按“名称/用途/入口/可用价值”整理。
- 低置信 OCR：只整理能确定的连续信息，把不确定部分放到“不确定信息”。

主要内容整理不是摘要。它应该比一句话更完整，让读者不看原图也能理解截图里可保留的信息。

## 4. 可提取信息

- 关键词：
- 关键句：用一句话总结本截图的核心信息，不要与第 3 节重复堆叠同一段内容。优先回答“这张截图值得保留的核心信息是什么”。进入 Phase 2 归档后，在本行末尾添加稳定块标识 `^core-summary`，供分类板块页嵌入引用。
- 涉及对象：
- 涉及平台：仅填写截图文字或画面中明确出现的平台名称
- 涉及行业：
- 涉及方法：
- 涉及案例：

## 5. 不确定信息

- 仅记录因图片模糊、裁切、遮挡、分辨率不足、文字过小、画面不完整等外部因素导致的无法识别内容。

## 6. Phase 2 评估预留

> Phase 1 不填写本节。进入 Phase 2 后，再补充信息价值、入库判断、建议分类和建议标签。
```

## Writing Rules for Raw Notes

Use these rules when filling `## 3. 主要内容整理` and `## 4. 可提取信息`.

### 主要内容整理

- Read the full OCR text and the visible screenshot context before writing.
- Do not summarize by copying the first few OCR lines.
- Remove obvious noise: status bar text, navigation labels, buttons, page chrome, isolated symbols, broken fragments, duplicated OCR, and text that is clearly a recognition error.
- Preserve meaningful structure from the source. If the source has numbered items, steps, chapters, bullet lists, table rows, or section titles, turn them into readable paragraphs or lists.
- Keep the content type stable. A medical report remains a personal health record; a literary excerpt remains writing/material; a tool page remains a resource; a method remains a method.
- Do not invent missing context. If the screenshot cannot prove a field, leave it blank or move it to uncertainty.

### 关键句 / 摘要

- The key sentence is a one-sentence summary of the screenshot's core retainable information.
- It should be derived after reading the full OCR and main-content整理, not before.
- It should not repeat the same paragraph as `主要内容整理`.
- Prefer a neutral sentence like: “这张截图记录了……”， “这张截图主要说明……”， or “这张截图可作为……的资料。”
- If the content is weak or unclear, say so directly: “这张截图只保留了部分可识别信息，主题仍需确认。”
- Do not use generic filler in the final filed key sentence, such as “这张截图主要包含……核心内容是……”. Keep only the actual core content.
- After Phase 2 filing, add `^core-summary` to the end of the key sentence line and treat that line as the single source of truth for category-board previews.

### 格式清理

- Remove extra spaces between Chinese characters: `我 们 要 做` -> `我们要做`.
- Remove spaces around Chinese punctuation: `你好 ， 世界` -> `你好，世界`.
- Keep spaces inside English names, product names, code, URLs, file paths, numbers with units, and mixed-language terms when the space is meaningful.
- Normalize repeated blank lines to one blank line between sections.
- Keep Markdown headings stable. Do not create decorative headings or overly nested lists.
- Do not use formatting cleanup to rewrite the user's meaning.

## Category Board Page

Use when the user has not requested second-level topic notes. One board page per first-level category is enough.

```md
# 分类名称

- 分类：01_选题与内容素材
- 截图数量：N

## Raw Notes

- [[screenshot_001_raw]]：
  ![[screenshot_001_raw#^core-summary]]
- [[screenshot_002_raw]]：
  ![[screenshot_002_raw#^core-summary]]
```

Do not copy the preview text into the board page. The board page should embed the Raw Note's `^core-summary` block so edits to the Raw Note key sentence automatically update the board display.

## Global Index

The global index should stay shallow. It should link to category board pages, not list every Raw Note.

```md
# 截图整理总索引

- 源目录：
- 输出目录：
- 处理日期：
- 截图总数：
- 文字信息截图：
- 非文字或低文字截图：

## 分类入口

- [[01_选题与内容素材]]：N 张
- [[02_读书学习]]：N 张
```

## Topic Knowledge Note

```md
---
title: 主题标题
type: knowledge_note
source_type:
  - screenshot
created: YYYY-MM-DD
status: 可复用
category:
  - 分类名称
tags:
  - 标签1
  - 标签2
  - 标签3
related:
  - "[[相关主题1]]"
  - "[[相关主题2]]"
source_notes:
  - "[[screenshot_001_raw]]"
---

# 主题标题

## 1. 这是什么

用 2-4 句话说明这篇笔记整理的核心内容。

## 2. 原始信息来源

- [[screenshot_001_raw]]
- [[screenshot_002_raw]]

## 3. 核心观点

- 观点 1：
- 观点 2：
- 观点 3：

> 每个核心观点都应来自上方列出的 Raw Note。若属于整理者理解，需要明确标注为“我的理解”。

## 4. 结构化整理

根据内容选择合适的小节，不要机械保留所有类型。

### 方法型内容

- 背景：
- 问题：
- 方法：
- 步骤：
- 注意点：
- 可复用模板：

### 案例型内容

- 案例对象：
- 案例背景：
- 做法：
- 结果：
- 可借鉴点：

### 设计型内容

- 设计对象：
- 视觉特征：
- 交互特征：
- 可复用规则：
- 适合场景：

### 产品型内容

- 用户：
- 场景：
- 痛点：
- 解决方案：
- 功能点：
- 产品机会：

### 学习型内容

- 概念：
- 解释：
- 例子：
- 易错点：
- 延伸问题：

## 5. 可复用价值

这部分内容未来可以用于：

-
-
-

## 6. 我的理解

基于截图信息进行适度加工，但不要伪装成截图原文。

## 7. 可行动方向

- 可以写成：
- 可以用于：
- 可以继续研究：
- 可以关联到：

## 8. Obsidian 关联

### 上级分类

- [[分类名称]]

### 强相关主题

- [[相关主题1]]
- [[相关主题2]]

### 延伸主题

- [[延伸主题1]]
- [[延伸主题2]]
```

## Uncertainty Block

Use this wording when information is unclear:

```md
## 不确定信息

- 该截图部分文字模糊，以下内容可能识别不完整。
- 该截图局部被裁切或遮挡，无法确认完整内容。
- 该截图文字过小或分辨率不足，OCR 结果可信度较低。
```
