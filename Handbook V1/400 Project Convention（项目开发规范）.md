

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

> **AI Drama Factory 项目应遵循哪些长期开发规范？**

Project Convention 是整个项目的最高开发规范。

它定义：

- 如何开发
- 如何协作
- 如何演进
- 如何维护

未来。

所有开发人员。

所有 AI。

所有自动化工具。

都应遵循本规范。

---

# 二、设计目标（Purpose）

Project Convention 的目标不是限制开发。

而是：

> **保证项目能够长期稳定演进。**

随着项目不断扩大。

开发人员不断增加。

AI 工具不断变化。

项目仍应保持：

- 一致性
- 可维护性
- 可理解性
- 可扩展性

---

# 三、适用范围（Scope）

本规范适用于：

- 前端开发
- 后端开发
- AI Engine
- Workshop
- Prompt
- 数据库
- 配置
- 文档
- 测试
- 部署

任何进入 AI Drama Factory 仓库的内容。

都应遵循本规范。

---

# 四、核心原则（Core Principles）

AI Drama Factory 坚持以下开发原则。

## Handbook First

Handbook 是整个项目的最高设计文档。

任何代码实现。

都应以 Handbook 为依据。

当代码与 Handbook 冲突时。

应优先检查设计。

而不是直接修改代码。

---

## Design Before Development

任何重要功能。

应先完成设计。

再开始开发。

避免：

边开发。

边设计。

边推翻。

---

## Freeze Before Expansion

已经 Freeze 的设计。

不得随意修改。

新增能力。

优先通过扩展实现。

而不是破坏已有结构。

---

## Single Source of Truth

任何规范。

任何设计。

任何架构。

都应只有一个权威来源。

避免：

多个文档描述同一件事情。

导致长期不一致。

---

## Continuous Evolution

Factory 鼓励持续优化。

但：

所有优化。

都应经过：

讨论。

设计。

Review。

最终再进入 Handbook。

---

# 五、开发流程（Development Process）

Factory 推荐统一开发流程。

```
Idea

↓

Discussion

↓

Backlog

↓

Design

↓

Review

↓

Freeze

↓

Development

↓

Testing

↓

Release
```

任何重要功能。

都不应跳过设计阶段。

---

# 六、变更原则（Change Management）

Factory 不反对修改。

但反对：

无序修改。

所有重大变更。

应满足：

- 有明确原因
- 有影响分析
- 有设计方案
- 有 Review
- 有版本记录

保证整个项目长期稳定。

---

# 七、Review 原则（Review Policy）

Review 的目标不是挑错。

而是：

提高整体质量。

Review 应坚持：

- 尊重事实
- 尊重设计
- 尊重数据
- 尊重长期维护

发现问题。

提出方案。

避免无意义争论。

---

# 八、Backlog 原则（Backlog Policy）

所有新想法。

默认进入 Backlog。

不得直接修改已 Freeze 的 Handbook。

Backlog 的作用是：

保存灵感。

等待成熟。

统一 Review。

成熟后。

再正式进入设计。

---

# 九、版本原则（Versioning）

Handbook。

Architecture。

代码。

数据库。

API。

均应具有明确版本。

重大变更。

应记录：

- 原因
- 时间
- 影响
- 决策结果

保证项目历史可追溯。

---

# 十、设计原则（Design Principles）

Factory 坚持：

## Long-term Thinking

所有设计。

优先考虑长期维护。

---

## Simplicity

简单优于复杂。

在满足需求的前提下。

优先选择更容易理解、更容易维护的方案。

---

## Consistency

保持统一风格。

统一命名。

统一流程。

统一规范。

---

## Evolution

允许系统持续成长。

但避免频繁推倒重来。

---

## Documentation First

重要设计。

必须有文档。

文档不是开发结束后的补充。

而是开发的开始。

---

# 十一、Non-Goals（非目标）

本章不负责：

- 具体目录结构（见 401）
- 命名规范（见 402）
- Git 流程（见 404~406）
- Prompt 规范（见 407）
- 数据库设计（见 409）

这些将在后续章节分别定义。

---

# 十二、Dependencies（依赖关系）

Depends On：

- 300 Overall Architecture
- 301 Product Architecture
- 302 Technical Architecture

Affects：

- Part IV 全部章节
- Part V Core System
- Part VI Workshop Design
- 后续全部开发工作

---

# 十三、本章总结

Project Convention 是 AI Drama Factory 的开发宪法。

它不规定具体实现。

而规定：

整个项目应如何长期健康发展。

未来。

任何设计。

任何开发。

任何 AI 自动生成代码。

都应遵循本规范。

---

**End**