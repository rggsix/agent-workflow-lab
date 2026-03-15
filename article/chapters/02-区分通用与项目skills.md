# 区分通用 Skills 与项目 Skills

Q: 为什么要区分通用/项目?
A: 保证skills可以最大程度被迁移

```markdown
通用skills是在同语言的项目中可以复用的(甚至跨语言项目可以复用的)
- 举例: 代码规范, commit规则等
项目skills则是主要与当前项目的业务逻辑相关
- 举例: 版本号管理, 常用全局变量与全局方法
```

## 通用skills分层
考虑拓展性, 通用skills分为3层:
- **basic**: 系统基础, 比如workspace在这层, 非常基础的能力 or 全局配置 or 基础原则等属于这层
- **flow**: 流程控制, 可以理解成 planner, 比如编码流程skills就属于这一层
- **operation**: 执行者, 可以理解成worker, 比如todo, commit, 注释等都属于这一层, 负责执行具体任务

所以skills目录应该是这样

```
/skills
  /common              # 通用技能
    /basic		 # 基建skills
    /flow		 # 流程控制skills
    /operation		 # 执行者skills, 可以理解成worker
  /project_specific    # 当前项目技能
```
