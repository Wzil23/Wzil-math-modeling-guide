# Claude Code 数学建模指南

> 用 Claude Code 完成数学建模竞赛论文的完整工作流：8 个斜杠命令，从读题到打包支撑材料。

## 快速开始

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

# 4. 开始使用
/mmsetup    # 配置
/mmstep1    # 读题
...
```

## 命令一览

| 命令 | 作用 |
|------|------|
| `/mmsetup` | 配置语言、格式、比赛类型 |
| `/mmstep1` | 读取题目和数据 |
| `/mmstep2` | 方案分析（brainstorming） |
| `/mmstep3` | 制定计划（writing-plans） |
| `/mmstep4` | 建模分析 |
| `/mmstep5` | 编程求解 |
| `/mmstep6` | 论文撰写 + 自检润色 |
| `/mmstep7` | 打包支撑材料 |

## 依赖 Skill

| Skill | 来源 |
|-------|------|
| math-modeling | [XiaoMaColtAI/math-modeling-skill](https://github.com/XiaoMaColtAI/math-modeling-skill) |
| brainstorming, writing-plans, subagent-driven-development | [obra/superpowers](https://github.com/obra/superpowers) |
| nature-reviewer, nature-figure | [Yuan1z0825/nature-skills](https://github.com/Yuan1z0825/nature-skills) |
| stop-slop | [hardikpandya/stop-slop](https://github.com/hardikpandya/stop-slop) |

## 详细文档

完整使用指南和各步骤说明见 **[ClaudeCode数学建模指南.md](怎么用ClaudeCode做数学建模/ClaudeCode数学建模指南.md)**

## License

MIT
