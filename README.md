## AI 协同开发实践：一个可演化的脚手架与 skills 组合实验

##### 这是一份在实际项目中整理出来的协作实践记录，偏个人经验，持续演化中。

##### 希望它能帮你在高频 AI 协作下，减少决策噪点，保持对项目的掌控感。

###### (⚠️这不是一个成熟方案, 只是探索。)

---

# 前言

我在大量使用 AI 协同开发后，发现开发变快了，但项目越来越容易失控。

代码很多是 AI 写的，我只负责 review 和决策。迭代很快，掌控感却在下降。

所以我觉得应该 给 AI 协作加一层“脚手架”。

你可以理解这是一套 skills 组合包，用来：

- 统一低价值决策（error、log、commit、ToDo 等）
- 降低认知噪点
- 让注意力集中在关键结构上
- 自动闭环风险

> 目标很简单：**让复杂系统在高速迭代下尽量维持可控**。

> ✏️ 标记表示该步骤已在实际项目中验证。

适合中长期维护的商业项目。轻量 demo 没必要使用。

> Skills 不只是给 AI 用的，它也是协作双方的约定。

---

# 如何使用它

我建议你遵循这个**人机****协作循环**配合使用:

##### **明确意图** → **定义单一任务** → AI执行 → Review ↔ 再执行 → 提交

这属于一种典型的 **Human-in-the-Loop (HITL)** 协作模式

判断一个意图是否“明确”，可以用一个简洁标准：

> **这个任务在commit message里一句话能不能说清楚**

---



# 目录

1. 在项目中引入 Skills

> 略

2. [区分通用 Skills 与项目 Skills](./article/chapters/02-区分通用与项目skills.md)
3. [基础设施](./article/chapters/03.基础设施.md)
4. [Install Skills（冷启动, agent入职）](./article/chapters/04-install-skills-冷启动-agent入职.md)

> todo

1. [编码流程 Skills](./article/chapters/05-编码流程-skills.md)
2. [通用 Skills 清单](./article/chapters/06-通用skills清单.md)
3. [项目 Skills 清单](./article/chapters/07-项目skills清单.md)
4. [关联：SDLC / Agentic Flow / Spec](./article/chapters/08-关联-sdlc-agentic-flow-spec.md)
