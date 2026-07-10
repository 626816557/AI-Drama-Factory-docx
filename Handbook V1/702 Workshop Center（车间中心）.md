

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

> **AI Drama Factory 应如何实时观察、管理和调度所有 Workshop 的运行状态？**

Workshop Center（车间中心）。

负责统一展示：

整个 Factory 所有 Workshop 的实时运行情况。

包括：

运行状态。

任务数量。

执行效率。

资源占用。

异常情况。

帮助 Operator。

持续观察整个 Factory 的生产状态。

---

# 二、Workshop Center 定位（Position）

Workshop Center。

不是：

Workshop 配置页面。

也不是：

Workshop 列表。

Workshop Center。

是整个 Factory 的 Workshop Command Center（车间指挥中心）。

它帮助 Operator。

实时掌握：

每一个 Workshop 当前正在发生什么。

---

# 三、设计目标（Purpose）

Workshop Center 的目标不是：

管理 Workshop 信息。

而是：

建立统一。

实时。

可观测。

可调度。

可恢复。

的 Workshop Operation Center。

帮助整个 Factory。

保持稳定运行。

---

# 四、核心展示内容（Core Views）

Workshop Center 应统一展示：

## Workshop Status

所有 Workshop 当前状态。

---

## Running Tasks

当前运行中的 Task。

---

## Waiting Queue

等待中的 Task。

---

## Throughput

生产吞吐量。

---

## Success Rate

成功率。

---

## Failure Analysis

失败情况。

异常原因。

---

## Resource Usage

CPU。

GPU。

Memory。

API。

资源占用。

---

# 五、Operator 能力（Operator Capabilities）

Workshop Center 应支持：

- 查看 Workshop
- 启停 Workshop（按权限）
- 查看 Queue
- Retry Task
- Pause Task
- 查看 Logs
- 查看 Metrics
- 查看 Health Status

帮助 Operator。

统一调度整个 Factory。

---

# 六、运行视图（Operating View）

Workshop 推荐统一展示：

```text
Workshop

↓

Queue

↓

Running

↓

Completed

↓

Failed

↓

Retry
```

Operator。

能够实时观察：

整个 Workshop 生命周期。

---

# 七、设计原则（Design Principles）

ADF-OS 坚持：

## Workshop First

围绕 Workshop 组织。

---

## Real-Time

实时运行状态。

---

## Observability

全过程可观测。

---

## Recoverability

支持恢复。

---

## Unified Operation

统一运行管理。

---

# 八、Non-Goals（非目标）

本章不负责：

- Project 生命周期
- Asset 管理
- GPU 管理
- Analytics
- Business Strategy

这些能力。

将在其它 Center 中完成。

---

# 九、Dependencies（依赖关系）

Depends On：

- 700 Dashboard
- Part V Core System
- Part VI Workshop Design

Affects：

- 全部 Workshop
- 全部 Task
- 全部 Engine

Workshop Center。

是整个 Factory 的车间运行中心。

---

# 十、本章总结

Workshop Center。

不是：

配置页面。

而是：

Workshop Command Center。

它帮助 Operator。

实时观察。

统一管理。

持续优化。

整个 Factory 的车间运行。

Workshop。

始终是 Factory 的核心生产单元。

---

**End**