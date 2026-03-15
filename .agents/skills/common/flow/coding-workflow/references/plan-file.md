# Plan 文件规则

一句话定位：定义 coding-workflow 的单计划文件模型，避免并发和归档噪音。

## 存储与并发

1. 仅允许一个活动 plan。
2. 写入前必须通过 workspace 映射获取 `coding-workflow` 路径；缺失则报错并请求人类处理。
3. 使用单文件：`plan.md`。
4. 流程开始前检查 `plan.md`：若已存在，先归档并删除，再开始新流程。

## 文件模板

```md
# Coding Workflow Plan

## 人类输入原文

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
- [ ] 步骤5: AI review [coding-workflow]

## 偏差说明（执行后填写）

- ...
```

## 生命周期

- 执行中：逐步打钩。
- 新流程开始前：归档并删除旧 `plan.md`，再创建新 `plan.md`。

## 归档规则

1. 归档目录：`archive/`（位于 `coding-workflow` 路径下）。
2. 归档命名：`YYYY-MM-DD-<seq>-<slug>.md`。
3. 归档内容：完整保留当次 `plan.md`。
