# 规则

一句话定位：只检查“是否按计划/需求实现”。

## 必须

1. 读取 `coding-workflow` 的 `plan.md` 或明确需求文本。
2. 读取实际改动代码（diff 或文件）。
3. 识别三类问题：少做 / 多做 / 偏离。
4. 若无问题，输出“Spec OK”。

## 输出格式

```text
Spec Review
- reason: [少做|多做|偏离] 清晰且可执行的说明
- file: path/to/file
- line: 12
```

## 禁止

- 不读代码只看描述。
- 不评审风格与质量（交给 quality-review）。
