# 执行流程

一句话定位：定义 commit 的顺序流程（ToDo 闭环 -> 分组 -> 提交）。

## 顺序步骤

1. 触发前置：先执行 `postcoding-todo`（除非人类明确要求跳过）。
2. 解析所有修改, 按修改目的进行文件级别拆分。
3. 先输出“分组清单”（包含每组文件与目的）。
4. 按分组清单依次执行：
   - `git add` 对应文件。
   - 生成 commit message。
   - `git commit`。
5. 循环执行步骤 2-4，直到工作区清空（`git status --short` 无输出）。
6. 若遇到必须保留或无法归组的改动，暂停并请求人类明确指示。

## 分组清单示例
格式示例
```text
分组清单：
1) 目的：更新 ai-review 流程映射
   文件：
   - .agents/skills/common/flow/coding-workflow/references/rules.md
   - .agents/skills/common/flow/coding-workflow/references/plan-file.md

2) 目的：同步流程文档
   文件：
   - article/chapters/05-编码流程-skills.md
```

## 顺序约束

- 未完成步骤1不得执行 git add/commit。
- 必须显式输出“已执行 postcoding-todo”确认行，否则拒绝进入提交步骤。
- 未输出“分组清单”不得执行 git add/commit。
