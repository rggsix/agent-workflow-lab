# 通用 Skills 清单

## 1. basic skills

##### 1. [workspace](../../.agents/skills/common/basic/workspace/SKILL.md)

管基础设施和官方状态路径，所有持久化写入都先问它。

## 2. flow skills

##### 1. [flow-gate](../../.agents/skills/common/flow/flow-gate/SKILL.md)

先判定要不要进完整编码流程，避免小改动过度流程化。

##### 2. [coding-workflow](../../.agents/skills/common/flow/coding-workflow/SKILL.md)

完整编码流程编排器，按步骤调用各个子技能。

##### 3. [intent-align](../../.agents/skills/common/flow/intent-align/SKILL.md)

开工前快速对齐意图，避免理解跑偏。

##### 4. [planning](../../.agents/skills/common/flow/planning/SKILL.md)

输出可执行的 spec-lite 计划，写入 plan.md。

##### 5. [execute-coding](../../.agents/skills/common/flow/execute-coding/SKILL.md)

按 plan.md 执行编码，偏差要记录。

## 3. operation skills

##### 1. [todo](../../.agents/skills/common/operation/todo/SKILL.md)

长期待办的主技能，负责 active/归档。

##### 2. [precoding-todo](../../.agents/skills/common/operation/precoding-todo/SKILL.md)

编码前先识别“现在不做但必须闭环”的风险点。

##### 3. [postcoding-todo](../../.agents/skills/common/operation/postcoding-todo/SKILL.md)

编码后补齐遗漏/隐患/优化点，并触发闭环。

##### 4. [todo-closure](../../.agents/skills/common/operation/todo-closure/SKILL.md)

专门负责 ToDo 闭环归档，减少漏标。

##### 5. [ai-review](../../.agents/skills/common/operation/ai-review/SKILL.md)

AI 自检闭环：spec-review → quality-review → 修复复检。

##### 6. [spec-review](../../.agents/skills/common/operation/spec-review/SKILL.md)

只看“做对没做对”，对照计划查少做/多做/偏离。

##### 7. [quality-review](../../.agents/skills/common/operation/quality-review/SKILL.md)

只看质量：结构/命名/可维护性/测试/风险点。

##### 8. [ask-next](../../.agents/skills/common/operation/ask-next/SKILL.md)

人类问“下一步做什么”时，读 todo 给 1-3 条建议。

##### 9. [commit](../../.agents/skills/common/operation/commit/SKILL.md)

原子化提交规则与约束（只做 add/commit，禁止 push/force/config 改动）。
