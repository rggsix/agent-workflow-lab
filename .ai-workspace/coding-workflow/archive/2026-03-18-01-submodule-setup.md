# Coding Workflow Plan

Task-ID: 20260318-01

## 人类输入原文

更新一下submodule

哦, 忘了, 这个没配, 参考这个项目配一下submodule, 原来里面的内容不要了

## AI返述确认

目标是将当前仓库的 `.agents/skills` 从普通跟踪目录改为 submodule，并对齐参考项目 `/Users/pwrd/Documents/work_ihuman/iOS/ihumanlive-iOS` 的配置与指针；当前目录下原有 `.agents/skills` 内容不保留，其它文件不额外改动，不提交 commit。

## 规划产出（planning skill 产物）

观察结果：当前仓库尚未配置 submodule，`.agents/skills` 以普通目录形式被 Git 跟踪；参考项目在 `.agents/skills` 路径配置了 URL 为 `git@github.com:rggsix/agent-workflow-skills.git` 的 submodule，当前指针为 `5517c4649c389502921e25d7252135339ec4b0e0`。
约束要点：需要移除现有 `.agents/skills` 普通目录跟踪并改为 gitlink；保留 `.agents` 其它内容；不提交 commit。

执行步骤（spec-lite）：
1. 清理当前仓库中已跟踪的 `.agents/skills` 普通目录内容，并写入与参考项目一致的 `.gitmodules` 配置。
2. 以参考项目同一 URL 和 commit 将 `.agents/skills` 接入为 submodule，确保工作区结构正确。
3. 校验 git 状态、submodule 状态和目录结果，记录必要偏差并准备进入 AI review。

- [x] 步骤1: 意图对齐 [intent-align]
- [x] 步骤2: 规划 [planning]
- [x] 步骤3: ToDo 同步（规划后） [precoding-todo]
- [x] 步骤4: 编码执行 [execute-coding]
- [x] 步骤5: AI review [ai-review]

## AI Review 记录（reviewer 输出）

- Spec review: OK。`.agents/skills` 已按需求从普通目录替换为 submodule，URL 与指针均对齐参考项目，未扩展到其它业务文件。
- Quality review: OK。采用本地仓库作为种子添加 submodule，再将 origin/.gitmodules 回写为正式远端 URL，避免了在受限环境里留下本地路径依赖。

## 偏差说明（执行后填写）

- 无功能偏差；实现上使用参考项目本地已存在的 submodule git 仓库完成接入，再同步回正式远端 URL，以适配当前环境限制。
