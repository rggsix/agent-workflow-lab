# 执行流程

一句话定位：定义 commit 的顺序流程（ToDo 闭环 -> 分组 -> 提交）。

## 顺序步骤

1. 触发前置：先执行 `postcoding-todo`（除非人类明确要求跳过）。
2. 分析当前 `git diff`（含 staged 与 unstaged）。
3. 判断是否存在多个独立逻辑变更。
4. 若存在多个逻辑变更：
   - 明确分组边界。
   - 分别 `git add` 对应文件。
   - 分别生成 commit message。
   - 分别 `git commit`。
5. 若仅一个逻辑变更：
   - `git add` 相关文件。
   - 生成 commit message。
   - `git commit`。
6. 循环执行步骤 2-5，直到工作区清空（`git status --short` 无输出）。
7. 若遇到必须保留或无法归组的改动，暂停并请求人类明确指示。

## 顺序约束

- 未完成步骤1不得执行 git add/commit。
- 必须显式输出“已执行 postcoding-todo”确认行，否则拒绝进入提交步骤。
