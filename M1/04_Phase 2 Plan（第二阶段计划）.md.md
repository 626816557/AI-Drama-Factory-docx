# AI Drama Factory

# Phase 2 Plan（第二阶段计划）

> Version：1.0
>
> Status：Planning
>
> Milestone：M1 → Phase 2
>
> Last Update：2026-07-01
>
> Owner：AI Drama Factory

---

# Preface（前言）

AI Drama Factory Handbook V1 已正式完成。

Architecture（架构）。

Business（商业）。

Workshop（车间）。

ADF-OS（控制中心）。

AI Infrastructure（AI 基础设施）。

Data Center（数据中心）。

Governance（治理）。

均已完成整体设计。

Phase 2 的目标。

不再是继续设计。

而是：

将 Handbook。

逐步变成真正的软件系统。

因此。

Phase 2。

并不是 Coding Sprint（编码冲刺）。

而是：

Implementation Phase（实现阶段）。

所有开发。

均以：

Handbook First（Handbook 优先）。

Architecture Driven Development（架构驱动开发）。

为最高原则。

---

# Part I

# Phase 2 Objectives（第二阶段目标）

Phase 2 的核心目标：

不是：

快速开发。

而是：

稳定实现。

Factory 的每一个模块。

都应严格按照：

Handbook。

Architecture。

Decision Log。

进行实现。

Phase 2 的最终成果：

应完成：

AI Drama Factory V1 MVP（最小可行产品）。

实现：

从 Project 创建。

到短剧发布。

完整运行闭环。

---

# Part II

# Development Principles（开发原则）

Phase 2 全程遵循以下原则。

## Handbook First（Handbook 优先）

所有功能。

必须来源于：

Handbook。

禁止：

边写边设计。

禁止：

脱离 Architecture。

直接 Coding。

---

## Architecture Before Implementation（架构先于实现）

Architecture。

永远领先：

Implementation。

所有重大修改。

先进入：

Architecture Review。

之后：

才能开发。

---

## Capability Driven（能力驱动）

Factory。

建设：

Capability。

而不是：

Script。

所有实现。

最终均抽象为：

Capability。

---

## Incremental Evolution（渐进演进）

Factory。

采用：

渐进建设。

每完成一个阶段。

立即进入：

Review。

避免：

一次性构建巨大系统。

---

## Freeze Frequently（阶段冻结）

每完成：

一个重要阶段。

均进行：

Freeze。

保证：

Architecture。

长期稳定。

---

# Part III

# Capability Roadmap（能力建设路线）

Phase 2 不按照：

时间。

而按照：

依赖关系（Dependency）。

进行建设。

---

## Stage 1

### Foundation（基础层）

目标：

建立：

Factory 的基础能力。

包括：

- Project Structure（项目结构）
- Config Center（配置中心）
- Logger（日志）
- Environment（环境配置）
- SQLite（数据库）
- Storage（存储）
- Common Utils（公共工具）
- Error Handling（异常处理）

完成标准：

Factory。

拥有统一基础设施。

---

## Stage 2

### ADF Kernel（ADF 内核）

目标：

建立：

Factory Core。

包括：

- Kernel
- Task Manager
- State Manager
- Event Bus
- Scheduler
- Queue
- Lifecycle Manager

完成标准：

Factory。

具备：

统一调度能力。

---

## Stage 3

### Workflow Engine（工作流引擎）

目标：

建立：

Workflow Engine。

负责：

Workflow。

Step。

Execution。

Retry。

Rollback。

Workflow State。

完成标准：

Factory。

能够执行：

完整 Workflow。

---

## Stage 4

### Project Center（项目中心）

目标：

建立：

Project 生命周期。

包括：

Project。

Episode。

Scene。

Asset。

Production。

Publishing。

Analytics。

完成标准：

Factory。

能够管理：

完整 Project。

---

## Stage 5

### Knowledge Center（知识中心）

目标：

建立：

Knowledge Base。

包括：

Prompt。

Decision。

Best Practice。

Failure。

Analytics。

Reference。

完成标准：

Factory。

拥有：

Learning Capability。

---

## Stage 6

### Workshop System（车间系统）

目标：

建立：

Workshop Registry。

Workshop Runtime。

Workshop API。

Workshop Configuration。

逐步迁移：

Spider。

Mapper。

Validator。

Director。

Renderer。

Publishing。

完成标准：

所有生产能力。

统一进入：

Workshop。

---

## Stage 7

### AI Infrastructure（AI 基础设施）

目标：

建立：

Provider Layer。

Capability Layer。

Model Router。

Prompt Manager。

Rate Limiter。

AI Cache。

完成标准：

Factory。

能够自由切换：

LLM。

Image。

Video。

Speech。

Provider。

---

## Stage 8

### Content Pipeline（内容流水线）

目标：

完成：

End-to-End。

Production Pipeline。

包括：

Spider。

Project。

Director。

Renderer。

Video。

Publishing。

完成标准：

Factory。

能够自动完成：

完整短剧生产。

---

## Stage 9

### Operations（运营体系）

目标：

建立：

Analytics。

ROI。

Publishing Strategy。

Growth Loop。

A/B Testing。

Dashboard。

完成标准：

Factory。

拥有：

运营能力。

---

## Stage 10

### Commercial MVP（商业 MVP）

目标：

完成：

AI Drama Factory V1。

MVP。

实现：

真实商业运行。

包括：

自动生产。

自动发布。

自动分析。

自动优化。

完成标准：

Factory。

进入：

Commercial Validation（商业验证）。

---

# Part IV

# Milestone Planning（里程碑规划）

## M2

Foundation Completed（基础层完成）

Factory。

具备：

统一基础能力。

---

## M3

ADF Kernel Completed（ADF 内核完成）

Factory。

拥有：

统一调度能力。

---

## M4

Workshop Completed（车间体系完成）

全部 Workshop。

完成迁移。

---

## M5

End-to-End Pipeline Completed（端到端流水线完成）

Factory。

能够自动完成：

短剧生产。

---

## M6

Commercial MVP Completed（商业 MVP 完成）

Factory。

正式进入：

真实商业验证。

---

# Part V

# Success Criteria（成功标准）

Phase 2 完成后。

Factory 应满足：

✅ Handbook 全部落地。

✅ Workshop 全部运行。

✅ SQLite 数据中心建立。

✅ ADF Kernel 完成。

✅ Workflow Engine 完成。

✅ Knowledge Base 建立。

✅ AI Infrastructure 建立。

✅ End-to-End Pipeline 跑通。

✅ Commercial MVP 可运行。

---

# Part VI

# Out of Scope（本阶段不包含）

以下能力。

暂不属于：

Phase 2。

统一进入：

Architecture Backlog。

包括：

- Multi-Agent（多智能体）
- Plugin Marketplace（插件市场）
- Graph RAG（图谱 RAG）
- Kubernetes（K8s）
- Multi-Tenant（多租户）
- Factory Cluster（工厂集群）
- Global Factory Network（全球工厂网络）
- Enterprise Governance（企业级治理）

这些能力。

将在未来版本中逐步评估。

---

# Summary（总结）

Phase 2。

不是：

一次普通开发。

而是：

AI Drama Factory 从 Architecture（架构）走向 Software（软件）的关键阶段。

整个 Phase 2。

坚持：

Handbook First。

Architecture Driven。

Capability Driven。

Incremental Evolution。

通过：

Foundation。

ADF Kernel。

Workflow。

Workshop。

Knowledge。

AI Infrastructure。

逐步建立：

真正的 AI Drama Factory。

当 Phase 2 完成时。

Factory 将拥有：

完整的端到端自动化生产能力。

并正式进入：

Commercial MVP（商业最小可行产品）阶段。

---

**End**