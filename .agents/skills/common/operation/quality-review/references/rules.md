# 规则

一句话定位：只检查代码质量，不讨论需求匹配。

## 必须

1. 仅在 spec-review 通过后执行。
2. 读取实际改动代码（diff 或文件）。
3. 检查维度：结构/命名/可维护性/测试/风险点。
4. 若无问题，输出“Quality OK”。

## 输出格式

```text
Quality Review
- reason: [质量问题] 清晰且可执行的说明
- file: path/to/file
- line: 12
```

## 禁止

- 不讨论需求是否实现（交给 spec-review）。
- 不扩展范围到未改动代码。
