# Screenshot to Obsidian Knowledge

把散落在相册、下载目录和聊天记录里的截图，整理成有来源、可分类、能检索的 Obsidian Markdown 知识库。

[English Skill instructions](./SKILL.md) · [中文 Skill 说明](./SKILL.zh-CN.md)

## 它解决什么问题

很多截图保存时觉得有用，之后却很难再次找到。这个 Skill 不只提取 OCR 文本，还会保留原图、生成可追溯的 Raw Note，并把内容整理进适合长期使用的 Obsidian 目录。

它会明确区分：

- 截图中能够确认的事实
- 模糊、裁切或 OCR 低置信度内容
- 整理过程中产生的理解与归纳

缺失的上下文不会被自动补写。

## 主要产出

- 每张文字信息截图对应一篇 Raw Note
- 所有已处理图片的原图副本与复制清单
- 按未来用途归档的一级分类目录
- 带关键词和关键句预览的分类板块页
- 只链接分类板块页的浅层总索引
- 入库判断、不确定信息清单，以及按需生成的主题笔记

## 工作流程

### Phase 1：接收与原始记录

统计图片、区分文字截图与非文字图片、复制原图、执行 OCR、保留可见信息，并生成 Raw Note。

### Phase 2：评估与知识化

按未来用途分类和归档，生成分类板块页与总索引；只有用户要求或材料明确形成稳定主题时，才生成主题笔记。

## 安装

以下方式任选一种。Codex 会自动检测 Skill；如果没有立即出现，重启 Codex。

### 使用 Skill Installer

在 Codex 中输入：

```text
请使用 $skill-installer 从 https://github.com/MuAngie/screenshot-to-knowledge 安装这个 skill。
```

### 手动安装到个人目录

PowerShell：

```powershell
New-Item -ItemType Directory -Force "$HOME\.agents\skills" | Out-Null
git clone https://github.com/MuAngie/screenshot-to-knowledge.git "$HOME\.agents\skills\screenshot-to-obsidian-knowledge"
```

macOS / Linux：

```bash
mkdir -p "$HOME/.agents/skills"
git clone https://github.com/MuAngie/screenshot-to-knowledge.git "$HOME/.agents/skills/screenshot-to-obsidian-knowledge"
```

### 安装到当前项目

如果只想在某个仓库中使用，把它放进该仓库的 `.agents/skills`：

```bash
mkdir -p .agents/skills
git clone https://github.com/MuAngie/screenshot-to-knowledge.git .agents/skills/screenshot-to-obsidian-knowledge
```

Codex 官方的 Skill 目录与调用说明见 [Build skills](https://learn.chatgpt.com/docs/build-skills)。

## 使用

在 Codex CLI 或 IDE 中显式调用：

```text
$screenshot-to-obsidian-knowledge
请把这些截图整理成 Obsidian 知识库，输出到 D:/MyVault/截图整理。
```

也可以直接描述任务，让 Codex 根据 Skill 的 `description` 自动选择它。

更多示例：

```text
把这批截图先做原始记录和 OCR，完成 Phase 1 后停止。
```

```text
使用我的现有 Obsidian 分类体系整理这些截图，同时保留原图和不确定信息。
```

```text
这些 Raw Notes 已经生成好了，请从 Phase 2 开始分类、归档并创建板块页。
```

## 默认输出结构

```text
Obsidian_Knowledge_Output/
├── 00_Inbox_待整理/
├── 01_选题与内容素材/
├── 02_读书学习/
├── 05_AI产品经理/
├── 06_商业案例/
├── 07_方法论/
├── 09_可用工具和网页/
├── 10_生活内容/
├── 11_旅行/
├── 12_待判断/
└── _Source_Images/
    └── YYYY-MM/
```

用户已有目录、标签或 Frontmatter 规范时，以用户规范为准。

## 使用边界

- 纯图片、照片、表情包和视觉素材会单独分流，不强行生成文字型 Raw Note。
- 模糊、裁切或无法确认的信息会保留不确定性标记，不会被猜测补全。
- 医疗、法律、金融及敏感隐私内容只整理可见信息，不替用户做专业判断。
- 原始图片不会被修改；每张已处理图片只复制一次到输出目录。

## 仓库结构

```text
.
├── SKILL.md
├── SKILL.zh-CN.md
├── agents/
│   └── openai.yaml
└── references/
    ├── phase-1-intake-raw-capture.md
    ├── phase-2-evaluation-knowledge-notes.md
    ├── taxonomy.md
    ├── templates.md
    └── workflow.md
```
