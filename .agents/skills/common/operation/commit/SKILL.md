---
name: commit
description: 执行原子化 git 提交。用于在不 push、不改配置、不用强制命令的前提下，完成变更分组、staging 与 commit，并保证一个 commit 只表达一个逻辑变更。
---

# Commit

只做原子化 `git add` + `git commit`。

## 必读引用

- [references/rules.md](references/rules.md): 提交边界、原子化原则与安全禁令。
- [references/flow.md](references/flow.md): 从 diff 分析到分组提交的执行流程。
- [references/message.md](references/message.md): commit message 格式与文案约束。
