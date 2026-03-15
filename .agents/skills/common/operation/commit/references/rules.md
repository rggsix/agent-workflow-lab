# 提交规则

一句话定位：定义 commit skill 的硬边界，确保提交原子且安全。

## 允许

- `git add`
- `git commit`

## 禁止

- `git push`
- 修改 `git config`
- 强制命令（如 `--force`、`reset --hard`）
- 跳过 hooks

## 原子化原则

1. 每个 commit 只能表达一个逻辑变更。
2. diff 含多个无关联变更时，必须拆分为多个 commit。
3. 即使只改一行，只要逻辑无关联，也必须独立提交。

## 安全规则

1. 永远不要提交 `.env` 或敏感文件。
2. 不执行 push。
3. 不执行 force。
4. 不修改 git 配置。
