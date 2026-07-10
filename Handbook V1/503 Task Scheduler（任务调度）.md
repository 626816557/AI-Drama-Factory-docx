

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

> **AI Drama Factory 应如何统一调度所有生产任务？**

Task Scheduler（任务调度）。

负责管理整个 Factory 的任务执行。

包括：

- 创建任务
- 分配任务
- 排队执行
- 调度 Workshop
- 调度 Engine
- 重试失败任务
- 控制并发
- 跟踪执行状态

Task Scheduler。

是整个 Factory 的调度中心。

---

# 二、设计目标（Purpose）

Task Scheduler 的目标不是：

让任务尽快执行。

而是：

让所有任务。

按照统一规则。

稳定。

有序。

可追踪。

可恢复。

地运行。

Factory 不依赖人工协调。

而依赖统一调度。

---

# 三、核心原则（Core Principles）

Factory 坚持：

## Task-Centric（任务中心）

所有生产行为。

都应抽象为 Task。

任何 Workshop。

都不应直接调用另一个 Workshop。

所有任务。

统一交由 Scheduler 调度。

---

## Event-Driven（事件驱动）

Task 不主动执行。

而是等待触发。

例如：

Project 创建。

上一阶段完成。

发布完成。

数据分析结束。

事件发生后。

Scheduler 决定是否生成新的 Task。

---

## State-Aware（状态感知）

Scheduler 必须感知：

- Project 状态
- Workshop 状态
- Engine 状态
- Resource 状态

只有满足执行条件。

Task 才能开始运行。

---

## Retryable（可重试）

任务失败。

不代表流程结束。

Scheduler 应支持：

- Retry
- Resume
- Skip（允许时）
- Manual Intervention（必要时）

保证 Factory 持续运行。

---

## Observable（可观测）

每一个 Task。

都应记录：

开始时间。

结束时间。

执行耗时。

执行结果。

错误原因。

重试次数。

方便：

监控。

统计。

优化。

---

# 四、Task 生命周期（Task Lifecycle）

Factory 推荐统一生命周期：

```text
Created

↓

Queued

↓

Waiting

↓

Running

↓

Completed
```

异常情况下：

```text
Running

↓

Failed

↓

Retry

↓

Completed
```

或：

```text
Running

↓

Cancelled
```

所有状态。

统一由 Scheduler 管理。

---

# 五、Task 基本结构（Task Structure）

每一个 Task。

建议包含：

- Task ID
- Project ID
- Task Type
- Current State
- Priority
- Assigned Workshop
- Assigned Engine
- Retry Count
- Created Time
- Started Time
- Finished Time

Task 是 Factory 最小的调度单位。

---

# 六、任务调度流程（Scheduling Workflow）

Factory 推荐统一流程：

```text
Task Created

↓

Scheduler

↓

Select Workshop

↓

Select Engine

↓

Execute

↓

Collect Result

↓

Update State

↓

Next Task
```

Scheduler。

负责连接整个 Factory。

---

# 七、任务优先级（Task Priority）

建议支持统一优先级：

```text
Critical

High

Normal

Low

Background
```

高优先级任务。

优先执行。

避免资源竞争。

---

# 八、并发控制（Concurrency）

Scheduler。

统一控制：

- 最大并发数
- Engine 并发
- Workshop 并发
- GPU 资源
- API 调用频率

避免：

资源冲突。

模型限流。

系统过载。

---

# 九、设计原则（Design Principles）

Factory 坚持：

## Unified Scheduling

统一调度。

---

## Predictable Execution

执行过程可预测。

---

## Fault Tolerance

支持失败恢复。

---

## Resource Awareness

感知资源状态。

---

## Scalability

支持水平扩展。

---

# 十、Non-Goals（非目标）

本章不负责：

- Workflow 定义
- Engine 实现
- Event 规则
- 插件机制
- AI Provider 接入

这些内容。

将在后续章节继续定义。

---

# 十一、Dependencies（依赖关系）

Depends On：

- 500 Project Lifecycle
- 501 Workshop Architecture
- 502 Engine Architecture

Affects：

- 504 Event System
- 505 Plugin System
- 全部 Workshop
- 全部 Engine

Task Scheduler。

是 Factory 的统一调度中心。

---

# 十二、本章总结

Task Scheduler。

决定：

什么时候执行。

执行什么。

由谁执行。

如何恢复。

它统一调度：

Project。

Workshop。

Engine。

Task。

让整个 AI Drama Factory。

能够稳定。

高效。

持续运行。

---

**End**