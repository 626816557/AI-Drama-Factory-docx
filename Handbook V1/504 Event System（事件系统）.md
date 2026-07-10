

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

> **AI Drama Factory 应如何通过 Event（事件）驱动整个 Factory 自动运行？**

Event System（事件系统）。

负责连接整个 Factory。

当某个事件发生时。

通知相关模块。

触发新的任务。

推动整个生命周期持续向前运行。

Event。

不是业务。

而是：

Factory 的神经系统。

---

# 二、设计目标（Purpose）

Event System 的目标不是：

传递消息。

而是：

建立统一。

可靠。

可追踪。

可扩展。

的事件驱动机制。

让 Factory 从：

"主动调用"

演进为：

"自动响应"。

---

# 三、核心原则（Core Principles）

Factory 坚持：

## Event-Driven（事件驱动）

Factory 内部。

所有重要变化。

都应抽象为 Event。

例如：

Project Created。

Workshop Completed。

Publishing Finished。

Analytics Generated。

Learning Completed。

事件发生后。

由相关模块决定下一步动作。

---

## Loose Coupling（低耦合）

Event 只负责通知。

不负责业务逻辑。

事件发布者。

无需知道：

谁会处理事件。

事件消费者。

也无需知道：

事件来自哪里。

各模块。

通过 Event 解耦。

---

## Standard Event（统一事件）

所有 Event。

统一采用标准格式。

至少包含：

- Event ID
- Event Type
- Project ID
- Source
- Timestamp
- Payload

统一标准。

便于扩展。

---

## Traceability（可追踪）

所有 Event。

均应记录。

包括：

发布时间。

处理结果。

处理模块。

处理耗时。

形成完整事件链路。

---

## Reliability（可靠性）

重要 Event。

不得丢失。

支持：

重试。

补偿。

失败记录。

保证 Factory 稳定运行。

---

# 四、Event 与 Scheduler 的关系

Factory 中。

Event 与 Scheduler。

职责完全不同。

Event。

负责：

**Trigger（触发）**

Scheduler。

负责：

**Schedule（调度）**

标准流程如下：

```text
Event

↓

Scheduler

↓

Task

↓

Workshop

↓

Engine
```

Event 决定：

发生了什么。

Scheduler 决定：

下一步应该做什么。

---

# 五、事件分类（Event Categories）

Factory 推荐支持：

## Project Event

例如：

- Project Created
- Project Archived

---

## Workshop Event

例如：

- Workshop Started
- Workshop Completed
- Workshop Failed

---

## Task Event

例如：

- Task Created
- Task Running
- Task Completed
- Task Failed

---

## Engine Event

例如：

- Engine Started
- Engine Finished
- Engine Timeout

---

## Publishing Event

例如：

- Publishing Started
- Publishing Completed

---

## Analytics Event

例如：

- Analytics Generated

---

## Learning Event

例如：

- Knowledge Updated
- Model Improved

---

# 六、事件生命周期（Event Lifecycle）

Factory 推荐统一流程：

```text
Event Created

↓

Published

↓

Received

↓

Processed

↓

Completed
```

处理失败时。

进入：

```text
Retry

↓

Failed
```

所有状态。

统一记录。

---

# 七、事件结构（Event Structure）

每一个 Event。

建议包含：

- Event ID
- Event Type
- Project ID
- Source Module
- Target Module（可选）
- Payload
- Timestamp
- Status

Event 应保持轻量。

避免携带大量业务数据。

---

# 八、设计原则（Design Principles）

Factory 坚持：

## Event First

所有状态变化。

优先抽象为 Event。

---

## Loose Coupling

模块之间。

不直接依赖。

---

## Standard Message

统一消息格式。

---

## Reliable Delivery

可靠传递。

---

## Full Traceability

全过程可追踪。

---

# 九、Non-Goals（非目标）

本章不负责：

- Task 调度策略
- Workflow 定义
- Engine 实现
- Plugin 扩展
- 消息中间件选型

这些内容。

将在后续章节继续定义。

---

# 十、Dependencies（依赖关系）

Depends On：

- 500 Project Lifecycle
- 501 Workshop Architecture
- 502 Engine Architecture
- 503 Task Scheduler

Affects：

- 505 Plugin System
- 全部 Workshop
- 全部 Engine

Event System。

为整个 Factory 提供统一事件机制。

---

# 十一、本章总结

Event System。

负责：

发现变化。

发布变化。

通知变化。

Factory 不再依赖模块之间直接调用。

而是：

通过统一 Event。

驱动整个生命周期持续运行。

Event。

构成了 AI Drama Factory 的神经系统。

---

**End**