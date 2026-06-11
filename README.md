# Claude Code 数学建模指南

> :trophy: 用 Claude Code 完成数学建模竞赛论文的完整工作流：8 个斜杠命令，从读题到打包支撑材料。

---

## :rocket: 快速开始

```bash
# 1. 克隆本项目
git clone https://github.com/Wzil23/Wzil-math-modeling-guide.git
cd Wzil-math-modeling-guide

# 2. 安装所需 skill
git clone https://github.com/XiaoMaColtAI/math-modeling-skill.git ~/.claude/skills/math-modeling
git clone https://github.com/obra/superpowers.git ~/.claude/skills/superpowers
git clone https://github.com/Yuan1z0825/nature-skills.git ~/.claude/skills/nature-skills
git clone https://github.com/hardikpandya/stop-slop.git ~/.claude/skills/stop-slop

# 3. 部署 slash command（按 部署SlashCommand.md 操作）

# 4. 启动 Claude Code，开始使用
/mmsetup    # :gear: 配置
/mmstep1    # :book: 读题
```

---

## :clipboard: 命令一览

| 命令 | 作用 |
|------|------|
| `/mmsetup` | :gear: 配置语言、格式、比赛类型 |
| `/mmstep1` | :book: 读取题目和数据 |
| `/mmstep2` | :bulb: 方案分析（brainstorming） |
| `/mmstep3` | :calendar: 制定计划（writing-plans） |
| `/mmstep4` | :triangular_ruler: 建模分析 |
| `/mmstep5` | :computer: 编程求解 |
| `/mmstep6` | :pencil: 论文撰写 + 自检润色 |
| `/mmstep7` | :package: 打包支撑材料 |

---

## :wrench: 前置准备

使用前需要安装以下环境（详细步骤见 [ClaudeCode数学建模指南.md](ClaudeCode数学建模指南.md)）：

| 环境 | 说明 |
|------|------|
| :penguin: **Git** | 版本控制，克隆 skill 仓库用 |
| :green_circle: **Node.js** (v18+) | Claude Code 运行时依赖 |
| :robot: **Claude Code** | Anthropic 官方命令行 AI 工具 |
| :key: **API 配置** | Anthropic 账号 或 cc-switch 切换国产 API |
| :snake: **Python** (3.10+) | 数学建模编程环境 |
| :jigsaw: **Skill** (4个仓库，含7个skill) | math-modeling、brainstorming、writing-plans、subagent-driven-development、nature-reviewer、nature-figure、stop-slop |
| :hammer_and_wrench: **Slash Command** | 将提示词映射为斜杠命令 |
| :page_facing_up: **LaTeX** (可选) | 美赛需要，国赛可用 Word 替代 |

---

## :jigsaw: 依赖 Skill

| Skill | 来源 | 用途 |
|-------|------|------|
| math-modeling | [XiaoMaColtAI/math-modeling-skill](https://github.com/XiaoMaColtAI/math-modeling-skill) | :brain: 建模手 / :hand: 编程手 / :speech_balloon: 论文手 |
| brainstorming, writing-plans, subagent-driven-development | [obra/superpowers](https://github.com/obra/superpowers) | :bulb: 方案分析 / :calendar: 计划制定 / :arrows_counterclockwise: 并行处理 |
| nature-reviewer, nature-figure | [Yuan1z0825/nature-skills](https://github.com/Yuan1z0825/nature-skills) | :mag: 审稿审查 / :bar_chart: 图表质量 |
| stop-slop | [hardikpandya/stop-slop](https://github.com/hardikpandya/stop-slop) | :sparkles: 去 AI 味润色 |

---

## :open_book: 详细文档

完整使用指南和各步骤说明见 **[ClaudeCode数学建模指南.md](怎么用ClaudeCode做数学建模/ClaudeCode数学建模指南.md)**

---

## :balance_scale: License

MIT
