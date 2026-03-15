---
name: commit
description: 执行原子化 git 提交。凡涉及 `git add` 或 `git commit` 的请求，必须先使用本 skill 完成分组与规则校验；未通过校验不得提交。触发本 skill 后必须持续提交直到清空 git 工作区（除非人类明确要求保留某些改动）。提交过程中禁止 push、改配置和强制命令。
---

# Commit

只做原子化 `git add` + `git commit`。

## 必读引用

- [references/rules.md](references/rules.md): 提交边界、原子化原则与安全禁令。
- [references/flow.md](references/flow.md): 从 diff 分析到分组提交的执行流程。
- [references/message.md](references/message.md): commit message 格式与文案约束。
