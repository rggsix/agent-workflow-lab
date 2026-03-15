# 区分通用 Skills 与项目 Skills

```
Q: 为什么要区分?
A: 保证skills可以最大程度被迁移

通用skills是在同语言的项目中可以复用的(甚至跨语言项目可以复用的)
- 举例: 代码规范, commit规则等
项目skills则是主要与当前项目的业务逻辑相关
- 举例: 版本号管理, 常用全局变量与全局方法

所以skills目录应该是这样
/skills
  /common              # 通用技能
  /project_specific    # 当前项目技能
```
