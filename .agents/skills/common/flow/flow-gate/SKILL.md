---
name: flow-gate
description: 编码流程闸门。凡涉及代码改动的请求，必须先进入本 skill 做分流判定（fast_path 或 full_workflow）；未通过分流不得直接进入编码执行。本 skill 只做判定，不执行代码修改。
---

# 编码流程闸门

先判定，再决定是否进入完整编码流程。

## 必读引用

- [references/rules.md](references/rules.md): 闸门边界与分流规则。
- [references/output.md](references/output.md): 固定输出契约与下一步动作。
