---
name: workspace
description: Workspace 是基础设施管理者。用于定义并维护官方状态域与持久化路径规则；凡是需要写入 todo、日志、文档、决策等项目状态的 skill，都必须先通过 Workspace 获取路径，禁止自行发明存储位置。
---

# Workspace

统一状态域与路径真相源。

## 必读引用

- [references/rules.md](references/rules.md): Workspace 的强约束规则。
- [references/write-protocol.md](references/write-protocol.md): 写入前后必须执行的步骤。
- [assets/workspace.yaml](assets/workspace.yaml): 官方状态域路径配置源。
