# Claude Code 数学建模实战指南

> 用 Claude Code 完成一份数学建模竞赛论文的完整流程，从读题到打包支撑材料，全程自动化。

## 特性

- **8 步完整流程**：配置 → 读题 → 分析 → 计划 → 建模 → 编程 → 论文 → 打包
- **Slash Command 一键触发**：`/mmsetup`、`/mmstep1` 到 `/mmstep7`
- **多模态图像识别**：自动派发子代理识别题目中的示意图和图表
- **模型合理性检查**：在编码过程中自动检测公式错误、结果异常
- **图表质量保障**：SCI/Nature 标准绘图，支持 SVG + PNG 双格式
- **论文自检润色**：审稿人审查 → 图表检查 → 去 AI 味三重保障
- **支撑材料合规**：自动检查身份信息泄露、文件完整性

## 快速开始

### 1. 安装 Claude Code

```bash
npm install -g @anthropic-ai/claude-code
```

### 2. 安装所需 Skill

| Skill | 类型 | 用途 | 来源 |
|-------|------|------|------|
| `math-modeling` | 自定义 skill | 建模手、编程手、论文手三阶段流程 | [XiaoMaColtAI/math-modeling-skill](https://github.com/XiaoMaColtAI/math-modeling-skill) |
| `brainstorming` | superpowers | 题目分析、方案探索 | [obra/superpowers](https://github.com/obra/superpowers) |
| `writing-plans` | superpowers | 制定实现计划 | [obra/superpowers](https://github.com/obra/superpowers) |
| `subagent-driven-development` | superpowers | 并行处理独立子问题 | [obra/superpowers](https://github.com/obra/superpowers) |
| `nature-reviewer` | nature-skills | 审稿人视角审查论文 | [Yuan1z0825/nature-skills](https://github.com/Yuan1z0825/nature-skills) |
| `nature-figure` | nature-skills | 图表质量检查 | [Yuan1z0825/nature-skills](https://github.com/Yuan1z0825/nature-skills) |
| `stop-slop` | 自定义 skill | 去 AI 味检查和润色 | [hardikpandya/stop-slop](https://github.com/hardikpandya/stop-slop) |

克隆安装：

```bash
# 数学建模 skill
git clone https://github.com/XiaoMaColtAI/math-modeling-skill.git ~/.claude/skills/math-modeling

# superpowers（含 brainstorming、writing-plans、subagent-driven-development）
git clone https://github.com/obra/superpowers.git ~/.claude/skills/superpowers

# nature skills（含 nature-reviewer、nature-figure）
git clone https://github.com/Yuan1z0825/nature-skills.git ~/.claude/skills/nature-skills

# stop-slop
git clone https://github.com/hardikpandya/stop-slop.git ~/.claude/skills/stop-slop
```

### 3. 安装本项目

```bash
git clone https://github.com/Wzil23/Wzil-math-modeling-guide.git
cd Wzil-math-modeling-guide
```

### 4. 部署 Slash Command

按 `部署SlashCommand.md` 中的说明，将提示词文件部署为 Claude Code 的 slash command。

### 5. 开始使用

```
/mmsetup    → 配置语言、格式、比赛类型
/mmstep1    → 读取题目和数据
/mmstep2    → 方案分析
/mmstep3    → 制定计划
/mmstep4    → 建模分析
/mmstep5    → 编程求解
/mmstep6    → 论文撰写
/mmstep7    → 打包支撑材料
```

## 工作流程

```
/mmsetup    配置（语言/格式/比赛/TDD）
    ↓
/mmstep1    读取题目 PDF + 格式要求 + 附件数据
    ↓
/mmstep2    brainstorming 逐题探索建模思路
    ↓            ↓
/mmstep3    writing-plans 拆分任务 → 计划文档
    ↓
/mmstep4    建模手：Model Contract → 选型 → 推导 → 质检
    → 题目分析报告.md + 术语表格.md + 模型说明图
    ↓
/mmstep5    编程手：写代码 → 出图表 → 质检
    → 代码 + 结果表格 + 可视化图表 + HTML面板
    ↓
/mmstep6    论文手：写初稿 → 自审 → 英文化 → 审查 → 润色
    → 论文.docx / 论文.pdf
    ↓
/mmstep7    收集文件 → 合规检查 → 压缩打包
    → 支撑材料.zip
```

## 命令速查表

| 命令 | 作用 | 产出 |
|------|------|------|
| `/mmsetup` | 配置语言、格式、比赛类型 | 配置信息 |
| `/mmstep1` | 读取题目和数据 | 题目结构确认 |
| `/mmstep2` | brainstorming 方案探索 | 设计文档 |
| `/mmstep3` | writing-plans 任务拆分 | 计划文档 |
| `/mmstep4` | 建模分析 | 题目分析报告.md、术语表格.md、模型说明图 |
| `/mmstep5` | 编程求解 | 代码、结果表格、图表、HTML面板 |
| `/mmstep6` | 论文撰写 + 自检润色 | 论文.docx / 论文.pdf |
| `/mmstep7` | 打包支撑材料 | 支撑材料.zip |

## 项目结构

```
ClaudeCode数学建模提示词/
├── 00-快速设置.md           ← /mmsetup 参考
├── 01-准备工作.md           ← /mmstep1 参考
├── 02-题目分析与方案设计.md  ← /mmstep2 参考
├── 03-制定计划.md           ← /mmstep3 参考
├── 04-建模分析.md           ← /mmstep4 参考
├── 05-代码实现.md           ← /mmstep5 参考
├── 06-论文撰写.md           ← /mmstep6 参考
├── 07-支撑文件打包.md       ← /mmstep7 参考
├── 98-总览.md               ← 文件索引
└── 99-一次性发送版.md       ← 全流程合并版
```

## 前置条件

- **Claude Code**：命令行版或桌面版
- **Python 3.10+**：`pip install numpy pandas matplotlib scipy openpyxl`
- **LaTeX**（可选，美赛用）：MiKTeX 或 TeX Live
- **API 访问**：Anthropic 账号或通过 CC-switch 使用国产 API

## 关键设计

- **每步暂停确认**：每个小步骤完成后 Claude 会暂停，等用户确认后再继续
- **图表推荐方案**：建模和编程阶段会推荐 2-3 种图表方案，由用户选择
- **强制 Skill 调用**：nature-figure、nature-reviewer、stop-slop 通过 Skill 工具调用，不会被跳过
- **多模态识别**：主代理没有多模态能力，遇到图片自动派发 opus 子代理处理
- **人称统一**：提示词统一为 Claude 视角（"用户"），无歧义

## 详细文档

- [ClaudeCode数学建模指南.md](ClaudeCode数学建模指南.md) — 完整的使用指南
- [部署SlashCommand.md](部署SlashCommand.md) — 在新电脑上部署的说明

## License

MIT
