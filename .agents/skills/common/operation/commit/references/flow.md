# 执行流程

一句话定位：定义从 diff 识别到分组提交的执行步骤。

1. 分析当前 `git diff`（含 staged 与 unstaged）。
2. 判断是否存在多个独立逻辑变更。
3. 若存在多个逻辑变更：
   - 明确分组边界。
   - 分别 `git add` 对应文件。
   - 分别生成 commit message。
   - 分别 `git commit`。
4. 若仅一个逻辑变更：
   - `git add` 相关文件。
   - 生成 commit message。
   - `git commit`。
