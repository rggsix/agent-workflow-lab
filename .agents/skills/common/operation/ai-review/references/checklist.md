# Checklist

一句话定位：确保 AI review 按闭环执行且不超限。

## 执行前

1. 已确定本轮 diff 范围。
2. 已确认相关文件清单。
3. 已准备调用 `spec-review` 与 `quality-review`。

## 执行后

1. 已完成 review->修复->复检。
2. 轮次未超过上限，或已触发 human-in-loop。
3. 输出“无问题”或问题清单。
