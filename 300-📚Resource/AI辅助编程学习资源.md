> 目标：学会**用 AI 帮助自己编程、解决问题**（不是学习 AI 本身）。
> 以下星标数据为 2026-10-11 用 GitHub API 逐一核实，会随时间变化。

## 首选：obra/superpowers

[obra/superpowers](https://github.com/obra/superpowers) —— ★29.7 万，目前最火的 AI 编程方法论项目之一。

它不只是一份教程，而是给 AI 编程助手装上的一整套**协作开发流程**，README 本身就是教程。核心流程：

1. 拿到需求先不写代码，让 AI 反过来问清你真正要什么
2. 把需求整理成设计稿，拆成小块给你确认
3. 生成实施计划（强调 TDD 红/绿测试、YAGNI、DRY）
4. 用子代理逐任务实现 + 审查，可自主工作数小时不偏离计划

Claude Code 安装（已上架官方插件市场，在对话框直接输入）：

```text
/plugin install superpowers@claude-plugins-official
```

装完之后，日常用 AI 写代码就是在按这套最佳实践运作——**做着做着就学会了**。

## 配套资源

| 用途 | 仓库 | 星标 |
| --- | --- | --- |
| 官方手册（Claude Code 正在用的工具） | [anthropics/claude-code](https://github.com/anthropics/claude-code) | ★15.0 万 |
| 精选索引：命令 / hooks / 工作流 / 学习资料 | [hesreallyhim/awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) | ★5.5 万 |
| 提示词基本功（官方交互式教程，9 章） | [anthropics/prompt-eng-interactive-tutorial](https://github.com/anthropics/prompt-eng-interactive-tutorial) | ★3.8 万 |
| VS Code / Copilot 用户的配置合集 | [github/awesome-copilot](https://github.com/github/awesome-copilot) | ★4.0 万 |
| Google 工程师（Addy Osmani）的软件工程全流程技能集 | [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) | ★10.5 万 |
| Anthropic 官方技能合集 | [anthropics/skills](https://github.com/anthropics/skills) | ★18.0 万 |

## 学习路径

1. **先装 superpowers**，拿真实任务练一遍完整流程（学「怎么指挥 AI 写代码」）
2. 遇到具体问题（怎么配置、怎么写规则文件）→ 去 awesome-claude-code 里查
3. 想让提问/迭代更高效 → 补提示词交互教程
4. 如果也用 VS Code / Copilot → 参考 awesome-copilot 的配置合集

## 备注

- 搜索时发现内容农场有大量编造的假数据：`forrestchang/andrej-karpathy-skills`、`affaan-m/everything-claude-code` 等"十几万星"的仓库在 GitHub 上**根本不存在**，引用前务必核实。
- 判断一个仓库是否可信：星标 + 最近更新时间（`pushed_at`）都查 GitHub API 比较稳妥。
