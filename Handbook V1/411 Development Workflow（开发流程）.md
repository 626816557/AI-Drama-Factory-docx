

> Version：V1.0
>
> Status：Draft
>
> Last Update：2026-07-01
>
> Owner：AI Drama Factory

---

# 一、本文档回答什么问题？

本文档回答：

> **AI Drama Factory 应如何开展软件开发工作？**

Development Workflow 定义整个项目的标准开发流程。

包括：

- 需求提出
- 设计
- 开发
- 测试
- Review
- 发布

统一流程。

保证整个 Factory 长期稳定演进。

---

# 二、设计目标（Purpose）

Development Workflow 的目标不是：

增加流程。

而是：

降低返工。

降低风险。

提高质量。

保证：

设计。

开发。

测试。

始终保持一致。

---

# 三、核心原则（Core Principles）

Factory 坚持：

## Handbook First

任何开发。

始于 Handbook。

而不是代码。

---

## Design Before Code

任何重要功能。

先完成设计。

再开始编码。

---

## Small Iteration

每次开发。

只完成一个明确目标。

避免：

一次完成整个系统。

---

## AI Assisted

Factory 鼓励：

使用 AI。

辅助：

设计。

编码。

Review。

测试。

但最终责任。

仍属于开发者。

---

## Continuous Improvement

每完成一次开发。

Factory 都应：

总结。

学习。

持续优化开发流程。

---

# 四、标准开发流程（Standard Workflow）

Factory 推荐统一流程：

```
Idea

↓

Discussion

↓

Backlog

↓

Handbook Design

↓

Architecture Review

↓

Task Breakdown

↓

Development

↓

Testing

↓

Code Review

↓

Merge

↓

Release

↓

Retrospective（复盘）
```

任何重要功能。

原则上不得跳过设计阶段。

---

# 五、阶段说明

## 1、Idea

提出新的想法。

不直接进入开发。

---

## 2、Discussion

讨论：

是否有价值。

是否符合 Factory 战略。

---

## 3、Backlog

成熟之前。

统一进入 Backlog。

避免影响当前开发。

---

## 4、Handbook Design

进入正式设计。

修改 Handbook。

形成统一规范。

---

## 5、Architecture Review

确认：

是否符合整体架构。

是否影响已有设计。

---

## 6、Task Breakdown

将设计拆解为：

多个独立开发任务。

每个 Task 应：

- 可独立开发
- 可独立测试
- 可独立 Review

---

## 7、Development

按照 Handbook。

完成具体实现。

开发过程中。

不得随意修改设计。

---

## 8、Testing

完成：

单元测试。

集成测试。

必要的人工验证。

保证功能符合设计。

---

## 9、Code Review

Review：

是否符合：

Architecture。

Convention。

Implementation。

Review 通过后。

方可 Merge。

---

## 10、Merge

合并进入：

Main。

保持主分支始终稳定。

---

## 11、Release

发布新版本。

同步：

文档。

版本号。

Change Log。

---

## 12、Retrospective（复盘）

发布结束后。

分析：

成功经验。

存在问题。

优化建议。

必要时：

进入 Backlog。

等待下一轮演进。

---

# 六、AI 在开发中的角色

AI 可以参与：

- 设计建议
- Task 拆解
- 编码
- 测试
- Review
- 文档生成

AI 是：

开发助手。

不是最终决策者。

任何重要设计。

仍应经过人工确认。

---

# 七、开发产物（Deliverables）

每次开发。

至少应产生：

- Handbook 更新（如涉及设计）
- 源代码
- 测试结果
- Git Commit
- Change Log（如涉及版本）

保证每一次开发都有完整记录。

---

# 八、设计原则（Design Principles）

Factory 坚持：

## Design Driven

设计驱动开发。

---

## Documentation Driven

文档驱动实现。

---

## Task Driven

任务驱动开发。

---

## AI Collaborative

人与 AI 协同。

---

## Continuous Evolution

持续演进。

持续优化。

---

# 九、Non-Goals（非目标）

本章不负责：

- Review 流程（412）
- Release 流程（413）
- 项目管理工具选择
- Scrum 或 Kanban 实施细节

---

# 十、Dependencies（依赖关系）

Depends On：

- 400 Project Convention
- Part III：Architecture

Affects：

- 全部开发流程
- 全部代码实现
- 全部 AI 协作方式

---

# 十一、本章总结

Development Workflow 定义了 AI Drama Factory 的标准开发流程。

Factory 不依赖：

经验。

灵感。

个人习惯。

而依赖：

统一设计。

统一规范。

统一流程。

未来。

所有开发。

都应从 Handbook 开始。

最终回到 Handbook。

形成持续演进的闭环。

---

**End**