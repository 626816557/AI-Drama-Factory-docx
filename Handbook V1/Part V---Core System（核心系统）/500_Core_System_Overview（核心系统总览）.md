

> Version：V1.0
>
> Status：Draft
>
> Last Update：2026-07-07
>
> Owner：AI Drama Factory

---

# 一、本文档回答什么问题？（Purpose）

本文档回答一个核心问题：

> AI Drama Factory 的核心系统（Core System）是什么？

Business（商业）回答的是 Factory 为什么存在。

Content Strategy（内容战略）回答的是 Factory 生产什么内容。

Core System（核心系统）回答的是：

> Factory 如何运转。

它定义 Factory 内部所有模块的职责、边界、协作方式以及运行机制。

Core System 是整个 AI Drama Factory 的操作系统（Operating System）。

所有后续模块都必须遵循这里定义的架构。

---

# 二、什么是 Core System？（What is Core System）

Core System 是 AI Drama Factory 的中央控制层。

它负责管理 Factory 的所有运行过程。

包括：

- 项目（Project）
- 工作流（Workflow）
- 任务（Task）
- 数据（Data）
- 资产（Asset）
- AI 服务（AI Providers）
- 生产车间（Workshops）
- 质量控制（Quality）
- 学习反馈（Learning）

它本身并不直接生产内容。

而是协调所有模块共同完成生产。

因此：

Core System 更像 Factory 的大脑（Brain）。

而不是某一个车间。

---

# 三、Core System 的职责（Responsibilities）

Core System 负责以下能力：

## Factory Coordination（工厂协调）

协调所有模块之间的协作。

例如：

Project 创建后。

Workflow 自动启动。

Workflow 调度对应 Workshop。

Workshop 完成后更新状态。

Quality 完成后进入下一阶段。

整个过程都由 Core System 协调。

---

## Standard Protocol（统一协议）

定义所有模块之间的通信协议。

例如：

Project Protocol

Workflow Protocol

Asset Protocol

Character Protocol

Scene Protocol

Evaluation Protocol

所有模块必须遵循统一协议。

而不是自由通信。

---

## Data Management（数据管理）

统一管理 Factory 所有数据。

包括：

Project

Workflow

Task

Asset

Character

Prompt

Run

Quality

Evaluation

Publishing

Analytics

Core System 是数据生命周期的管理者。

而不是数据生产者。

---

## Resource Scheduling（资源调度）

统一调度：

AI Provider

GPU

Storage

Database

Worker

API

后续云端部署后。

资源调度全部由 Core System 完成。

---

## Quality Governance（质量治理）

Factory 不允许任何 Workshop 自己决定是否合格。

所有质量判断：

统一进入：

Quality System。

形成统一标准。

---

## Learning Loop（学习闭环）

Core System 负责：

收集反馈。

更新知识。

优化生产。

形成持续学习能力。

---

# 四、Core System 的设计原则（Design Principles）

Core System 遵循以下原则。

## Single Source of Truth（唯一事实来源）

Factory 中所有状态。

只能存在一个真实来源。

例如：

Project Status。

只能由 Core System 维护。

不能由多个模块分别维护。

---

## Protocol First（协议优先）

模块之间禁止直接耦合。

所有通信必须通过统一协议。

协议稳定。

实现可以演进。

---

## Event Driven（事件驱动）

Core System 采用事件驱动架构。

例如：

Project Created

Workflow Started

Workshop Finished

Quality Passed

Video Published

所有流程都围绕事件推进。

而不是模块之间直接调用。

---

## Stateless Workshop（无状态车间）

Workshop 只负责执行任务。

不保存长期状态。

长期状态统一交给 Core System。

这样：

任何 Workshop 都可以被替换。

---

## Extensible（可扩展）

Core System 不依赖任何具体 AI 模型。

未来可以：

新增 Workshop。

新增 AI Provider。

新增平台。

无需修改核心架构。

---

# 五、Core System 与其它部分的关系（Architecture Position）

整个 AI Drama Factory 的层级如下：

```text
Business（商业）

↓

Content Strategy（内容战略）

↓

Core System（核心系统）

↓

AI Production（AI 生产）

↓

Engineering（工程）

↓

Operations（运营）

↓

Infrastructure（基础设施）
```

Business 决定方向。

Content Strategy 决定内容。

Core System 决定运行方式。

AI Production 完成生产。

Engineering 提供技术实现。

Operations 完成商业运营。

Infrastructure 提供底层支撑。

---

# 六、Core System 的组成（Modules）

Core System 将逐步拆分为以下模块：

500 Core System Overview（核心系统总览）

501 Factory Architecture（工厂架构）

502 Data Model（数据模型）

503 Workflow Engine（工作流引擎）

504 Factory Protocol（工厂协议）

505 Memory System（记忆系统）

506 Asset Management（资产管理）

507 Quality System（质量系统）

508 Evaluation System（评估系统）

509 Learning System（学习系统）

510 Optimization System（优化系统）

每个模块独立负责一个领域。

共同组成 Factory Operating System。

---

# 七、与当前代码的关系（Current Implementation）

当前 M2 已完成：

Foundation（基础层）

包括：

- Config（配置中心）
- Environment（环境管理）
- Logger（日志系统）
- Errors（异常体系）

Persistence（持久化层）

包括：

- Storage（存储系统）
- Database（数据库）

这些模块提供底层能力。

但真正的业务组织方式。

将在 Core System 中定义。

未来：

Kernel、Centers、Workshops 都必须围绕 Core System 运行。

---

# 八、本章总结（Summary）

Core System 是 AI Drama Factory 的操作系统。

它不是一个模块。

而是整个 Factory 的运行规则。

它决定：

数据如何流动。

模块如何协作。

资源如何调度。

质量如何治理。

知识如何积累。

Factory 如何持续成长。

从 Part V 开始。

AI Drama Factory 将正式从「一组功能模块」演进为「一个完整的软件系统」。

---

**End**