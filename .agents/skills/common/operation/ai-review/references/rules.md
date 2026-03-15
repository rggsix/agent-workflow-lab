# 规则

一句话定位：定义 AI review 的两段式闭环与停止条件。

## 必须

1. 输入范围：仅基于本轮改动 diff 与相关文件。
2. 执行顺序（含循环）：
   1. `ai-review` 调用 `spec-review`。
   2. 若 `spec-review` 有问题：`ai-review` 修复后 **重新执行 `spec-review`**，直到 `Spec OK` 或 `spec-review` 已执行超 3 次。
   3. `Spec OK` 后，`ai-review` 调用 `quality-review`。
   4. 若 `quality-review` 有问题：`ai-review` 修复后 **重新执行 `quality-review`**，直到 `Quality OK` 或 `quality-review` 已执行超 3 次。
   5. 两者均 OK 后，`ai-review` 输出“无问题”。
   6. reviewer 输出结果交给 `ai-review` 汇总，`ai-review` 在流程结束后统一回写 `plan.md`。
3. `spec-review` 未通过不得进入 `quality-review`。
4. 若达到次数上限仍有问题，触发 human-in-loop。

## 禁止

- 复检前跳过修复。
- 引入超出本轮范围的改动。
