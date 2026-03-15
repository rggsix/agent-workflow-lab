# 提交规则

一句话定位：定义 commit skill 的硬边界，确保提交原子且安全。

## 强制触发

1. 凡涉及 `git add` 或 `git commit` 的请求，必须先进入本 skill。
2. 未完成原子化分组与规则校验，不得执行提交。
3. 触发本 skill 后，完成标准是 `git` 工作区清空（无 staged/unstaged/untracked 改动）。
4. 若存在必须保留的改动，需先获得人类明确指示，再按指示跳过。
5. commit 前必须执行 `postcoding-todo` 做二次 ToDo 整理（除非人类明确要求跳过）。
6. 未显式确认“已执行 postcoding-todo”，不得进入提交流程。
7. 提交前检查是否存在 `coding-workflow/plan.md`
   - 若存在，读取 `Task-ID` 并用于所有原子提交。
   - 若不存在，commit message 也要包含 `[task-id: 无]`, 不允许不写`task-id`模块

## 禁止

- `git push`
- 修改 `git config`
- 强制命令（如 `--force`、`reset --hard`）
- 跳过 hooks

## 原子化原则

1. 每个 commit 只能表达一个逻辑变更。
2. diff 含多个无关联变更时，必须拆分为多个 commit。
3. 即使只改一行，只要逻辑无关联，也必须独立提交。

## 例外

plan.md不需要单独原子化提交, 可跟任意commit一起提交

## 安全规则

1. 永远不要提交 `.env` 或敏感文件。
2. 不执行 push。
3. 不执行 force。
4. 不修改 git 配置。
