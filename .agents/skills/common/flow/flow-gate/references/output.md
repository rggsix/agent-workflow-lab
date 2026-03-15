# 输出契约

一句话定位：统一 flow-gate 的输出格式，避免分流结果歧义。

## 输出字段

- `decision`: `fast_path` | `full_workflow`
- `reason`: 一句话说明判定依据
- `next_step`: 下一步动作名

## 示例

```yaml
decision: fast_path
reason: 需求单一且低风险，边界清晰
next_step: direct_execute
```

```yaml
decision: full_workflow
reason: 涉及多步骤与潜在影响面，需进入完整流程
next_step: coding-workflow
```
