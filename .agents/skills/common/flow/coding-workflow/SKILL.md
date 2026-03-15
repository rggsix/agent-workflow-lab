---
name: coding-workflow
description: 完整编码流程编排器。由 flow-gate 判定为 full_workflow 时触发；负责计划执行闭环（计划->执行->打钩->收尾）。
---
# Coding Workflow

用于复杂改动的完整流程编排。

## 触发

- `flow-gate` 输出 `full_workflow`。
- 或人类明确要求“按完整编码流程执行”。

## 必读引用

- [references/rules.md](references/rules.md): 流程步骤、边界与完成条件。
- [references/plan-file.md](references/plan-file.md): 单计划文件的读写规则。
