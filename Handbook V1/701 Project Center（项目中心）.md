

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

> **AI Drama Factory 应如何统一管理整个 Factory 的 Production Projects？**

Project Center（项目中心）。

负责统一管理：

Factory 中所有 Project。

包括：

创建。

运行。

暂停。

恢复。

归档。

观察。

Project。

是 Factory 的核心业务对象。

Project Center。

是整个 Factory 的 Production Command Center（生产指挥中心）。

---

# 二、Project Center 定位（Position）

Project Center。

不是：

Project List。

也不是：

CRUD 页面。

Project Center。

负责统一管理：

整个 Factory 的 Production Missions（生产任务）。

帮助 Operator。

观察。

控制。

组织。

全部 Project。

---

# 三、设计目标（Purpose）

Project Center 的目标不是：

维护项目数据。

而是：

建立统一。

实时。

可追踪。

可恢复。

可管理。

的 Production Management System。

帮助 Operator。

掌握整个 Factory 的生产情况。

---

# 四、核心展示内容（Core Views）

Project Center 应统一展示：

## Active Projects

当前生产中的 Project。

---

## Planned Projects

等待进入生产的 Project。

---

## Completed Projects

已完成 Project。

---

## Archived Projects

历史归档 Project。

---

## Failed Projects

失败。

暂停。

异常 Project。

---

## Project Timeline

Project 生命周期。

运行历史。

关键节点。

---

# 五、Operator 能力（Operator Capabilities）

Project Center 应支持：

- 创建 Project
- 启动 Project
- 暂停 Project
- 恢复 Project
- 取消 Project
- 查看 Blueprint
- 查看 Production Status
- 查看 Project History

Project Center。

统一作为：

Factory Project Command。

---

# 六、Project 生命周期视图（Lifecycle View）

Project 推荐统一展示：

```text
Planning

↓

Production

↓

Distribution

↓

Growth

↓

Evolution

↓

Archived
```

Operator。

能够实时查看：

Project 当前阶段。

---

# 七、设计原则（Design Principles）

ADF-OS 坚持：

## Mission Oriented

围绕 Production Mission。

---

## Real-Time

实时状态。

---

## Traceability

全过程追踪。

---

## Recoverability

支持恢复。

---

## Unified Control

统一控制。

---

# 八、Non-Goals（非目标）

本章不负责：

- Workshop 运行
- Asset 管理
- Analytics
- GPU
- Model

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
- 全部 Production Pipeline

Project Center。

是整个 Factory 的 Production Command Center。

---

# 十、本章总结

Project Center。

不是：

Project List。

而是：

Production Mission Center。

它帮助 Operator。

统一管理。

统一观察。

统一控制。

整个 Factory 的 Production Projects。

Project。

始终是 Factory 的核心业务对象。

---

**End**