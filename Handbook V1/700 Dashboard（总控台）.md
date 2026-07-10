

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

> **AI Drama Factory 应如何让 Operator 实时掌握整个 Factory 的运行状态？**

Dashboard（总控台）。

是整个 ADF-OS 的入口。

负责统一展示：

Factory 当前状态。

运行情况。

资源使用。

生产进度。

商业表现。

帮助 Operator。

实时观察。

统一管理。

持续优化。

整个 AI Drama Factory。

---

# 二、Dashboard 定位（Dashboard Position）

Dashboard。

不是：

管理后台首页。

也不是：

菜单入口。

Dashboard。

是整个 Factory 的 Operating Cockpit（运行驾驶舱）。

Operator。

进入 Factory 后。

首先看到的。

应是：

整个 Factory 当前运行状态。

而不是：

系统菜单。

---

# 三、设计目标（Purpose）

Dashboard 的目标不是：

展示更多数据。

而是：

建立统一。

实时。

可观测。

可管理。

可决策。

的 Factory Operating Center。

帮助 Operator。

在一个界面。

掌握整个 Factory。

---

# 四、核心展示内容（Core Views）

Dashboard 应统一展示：

## Factory Overview

Factory 当前总体运行状态。

---

## Business Stage

当前：

Market。

Planning。

Production。

Distribution。

Growth。

各阶段运行情况。

---

## Workshop Status

所有 Workshop。

当前状态。

等待数量。

运行数量。

异常数量。

---

## Project Status

Project：

进行中。

完成。

失败。

暂停。

---

## Resource Status

GPU。

CPU。

Memory。

Storage。

API。

AI 服务。

---

## Production Metrics

今日：

生产数量。

成功率。

成本。

效率。

---

## Growth Intelligence

运营表现。

增长趋势。

重点 Insight。

---

# 五、Operator 能力（Operator Capabilities）

Dashboard 应支持：

- 查看 Factory
- 管理 Project
- 查看 Workshop
- 查看 Resource
- 查看 Analytics
- 查看 Alert（未来）
- 查看 Logs（未来）

Dashboard。

统一作为：

Operator 的工作入口。

---

# 六、运行视图（Operating View）

Dashboard 推荐采用：

Factory Live View。

例如：

```text
Market Intelligence

↓

Production Planning

↓

Production

↓

Distribution

↓

Growth

↓

Evolution
```

每一个 Stage。

实时显示：

运行状态。

Project 数量。

健康度。

---

# 七、设计原则（Design Principles）

ADF-OS 坚持：

## Factory First

首先展示 Factory。

而不是菜单。

---

## Real-Time

实时更新。

---

## Observability

系统可观测。

---

## Decision Support

帮助 Operator 做决策。

---

## Unified Management

统一管理整个 Factory。

---

# 八、Non-Goals（非目标）

本章不负责：

- Project 管理
- Asset 管理
- Analytics 页面
- System Settings
- Workflow 编辑器

这些能力。

将在后续章节继续定义。

---

# 九、Dependencies（依赖关系）

Depends On：

- Part V Core System
- Part VI Workshop Design

Affects：

- 全部 ADF-OS
- 全部 Operator Experience

Dashboard。

是整个 Factory 的统一运行入口。

---

# 十、本章总结

Dashboard。

不是：

后台首页。

而是：

AI Drama Factory 的 Operating Cockpit。

它帮助 Operator。

实时观察。

统一管理。

持续优化。

整个 Factory。

Dashboard。

永远代表：

Factory 当前正在发生什么。

---

**End**