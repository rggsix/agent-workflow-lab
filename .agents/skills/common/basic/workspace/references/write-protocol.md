# 写入协议

1. 读取 `assets/workspace.yaml`。
2. 识别当前执行 skill 名（作为映射键）。
3. 在 `skills.<skill_name>` 下查找路径。
4. 写入目标文件。
5. 校验写入位置是否在 `.ai-workspace/` 内。

## 失败处理

- 映射缺失：立即报错并请求人类添加映射。
- 路径越界：拒绝写入并返回错误。
- 无明确人类授权：禁止修改 `workspace.yaml`。
