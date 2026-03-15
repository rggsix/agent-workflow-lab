# Plan 文件规则

一句话定位：定义 coding-workflow 的单计划文件模型，避免并发和归档噪音。

## 存储与并发

1. 仅允许一个活动 plan。
2. 写入前必须通过 workspace 映射获取 `coding-workflow` 路径；缺失则报错并请求人类处理。
3. 使用单文件：`plan.md`。
4. 若已有未完成 plan，必须先请求人类决定(human-in-loop gate)：继续或重置。

## 文件模板

```md
# Coding Workflow Plan

## 人类输入摘要

...

## AI返述确认

...

## 规划产出（planning skill 产物）

观察结果：...
约束要点：...

执行步骤（spec-lite）：
1. ...
2. ...
3. ...

- [ ] 步骤1: 意图对齐 [intent-align]
- [ ] 步骤2: 规划 [planning]
- [ ] 步骤3: ToDo 同步（规划后） [precoding-todo]
- [ ] 步骤4: 编码执行 [execute-coding]
- [ ] 步骤5: ToDo 同步（编码后） [postcoding-todo]
- [ ] 步骤6: review + human review [coding-workflow + human-in-loop gate]
- [ ] 步骤7: commit [commit]

## 偏差说明（执行后填写）

- ...
```

## 生命周期

- 执行中：逐步打钩。
- 完成后：保留该文件作为最近一次执行记录。
- 下次新流程开始前：覆盖重建 `plan.md`（不做归档）。
