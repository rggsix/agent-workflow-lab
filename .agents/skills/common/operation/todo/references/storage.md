# 存储规则

一句话定位：定义 ToDo 的存储位置与文件边界。

## 规则

1. 必须通过 `workspace` 获取当前 skill 的写入路径。
2. 路径映射键为 skill 名 `todo`；若映射缺失，立即报错并请求人类处理。
3. 在 ToDo 根目录只允许以下结构：
   - `active.md`
   - `archive/YYYY-MM.md`
4. 不允许自行发明路径或创建平行目录。

## 文件职责

- `active.md`: 仅存放未完成任务。
- `archive/YYYY-MM.md`: 每月归档已完成任务。
