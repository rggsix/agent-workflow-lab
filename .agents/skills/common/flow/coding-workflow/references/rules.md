# 流程规则

一句话定位：定义 coding-workflow 的 7 步流程与执行边界。

## 7步流程

1. 意图对齐（技术返述，确认后再继续）
2. 规划（调用 `planning`，结果写入 `plan.md`）
3. ToDo 同步（规划后预置：风险项/后续项）
4. 编码执行（按 `plan.md` 中的 planning 结果顺序推进；可调实现细节但需记录偏差；仅在需增删计划条目或越界时触发 human-in-loop）
5. ToDo 同步（编码后校正：新增项/完成项）
6. review + human review
7. commit（必须走 commit skill）

## 步骤与技能映射

1. 步骤1 意图对齐 -> `intent-align`
2. 步骤2 规划 -> `planning`
3. 步骤3 ToDo 同步（规划后） -> `precoding-todo`
4. 步骤4 编码执行 -> `execute-coding`（遇阻断走 `human-in-loop gate`）
5. 步骤5 ToDo 同步（编码后） -> `postcoding-todo`
6. 步骤6 review + human review -> `coding-workflow` + `human-in-loop gate`
7. 步骤7 commit -> `commit`

## 边界

- 本 skill 的职责是维护 plan 并按步骤唤起对应 skill，不替代被唤起 skill 的细则。
- 涉及状态写入时必须遵守 workspace 路径映射。
- 默认不包含测试、日志沉淀、项目 skills 更新（可后置）。
- 规划阶段通过 `planning` 输出并写入 `plan.md`，后续步骤只读该文件。

## 完成条件

- 当前 plan 全部打钩。
- ToDo 已完成二次同步。
- commit 已完成。
