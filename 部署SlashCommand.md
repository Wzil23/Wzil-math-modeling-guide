# 在新电脑上部署

## 前提条件

确保新电脑上已安装以下 skill：
- `math-modeling`（含建模手、编程手、论文手的完整 references 目录）
- `brainstorming`属于（superpower skill）
- `writing-plans`属于（superpower skill）
- `subagent-driven-development`属于（superpower skill）
- `nature-reviewer`、`nature-figure`属于（nature skill）
- `stop-slop`

## 部署步骤

1. 把本文件夹的所有 .md 文件复制到新电脑的桌面

2. 将下面这段话发给 Claude Code：

```
读取桌面上"数学建模提示词"文件夹里的以下 .md 文件，每个文件对应创建一个 slash command 到 ~/.claude/commands/ 目录下：

- 00-快速设置.md → mmsetup.md
- 01-准备工作.md → mmstep1.md
- 02-题目分析与方案设计.md → mmstep2.md
- 03-制定计划.md → mmstep3.md
- 04-建模分析.md → mmstep4.md
- 05-代码实现.md → mmstep5.md
- 06-论文撰写.md → mmstep6.md
- 07-支撑文件打包.md → mmstep7.md

command 文件的内容就是对应 .md 文件中代码块里的提示词部分，不要包含代码块外的说明文字。
```

3. 重启 Claude Code

4. 输入 `/mmsetup` 测试是否部署成功
