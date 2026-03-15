# 通用 Skills 清单

## 1. basic skills

##### 1. workspace

- [workspace](../../.agents/skills/common/basic/workspace/SKILL.md)

## 2. flow skills

## 3. operation skills

##### 1. [todo](../../.agents/skills/common/operation/todo/SKILL.md)

管理长期待办（active + archive），保持低认知负担。

路径位于

```
- 进行中: .ai-workspace/todo/active.md
- 已归档: .ai-workspace/todo/archive/YYYY-MM.md
```

具体格式

```markdown
# P0
- [ ] [需求标签] 待办事项简述 (YYYY-MM-DD)

# P1
...

# P2
...
```

#### 2. [commit](../../.agents/skills/common/operation/commit/SKILL.md)

原子化提交规则与约束（只做 add/commit，禁止 push/force/config 改动）。
