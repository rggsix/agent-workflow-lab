# 分流规则

一句话定位：定义 flow-gate 只做判定、不得执行的硬边界。

## 必须

1. 凡涉及代码改动的请求，必须先进入 `flow-gate`。
2. 仅做轻量判定，结论只能是 `fast_path` 或 `full_workflow`。
   1. 判定为 `fast_path` 时：不进入 `coding-workflow`，直接继续执行当前需求。
   2. 判定为 `full_workflow` 时，下一步必须进入 `coding-workflow`。

## 放行标准（`fast_path`）

清晰、单动作、低影响、低风险、无额外决策（全满足才放行）。

## 进入完整流程标准（`full_workflow`）

歧义、多步骤/跨模块、影响不明、高风险、需先确认（任一命中即进入）。

## 判定输出最小模板

```yaml
decision: fast_path | full_workflow
reason: 一句话说明命中的标准
```

## 禁止

- 直接修改代码。
- 直接提交 commit。
