# AI Drama Factory

# Architecture Decision Log（架构决策日志）

> Version：1.0
>
> Status：Active
>
> Last Update：2026-07-01
>
> Owner：AI Drama Factory

---

# Preface（前言）

Architecture Decision Log（架构决策日志）。

用于记录：

AI Drama Factory 在长期演进过程中做出的重大架构决策。

本文件不是：

Handbook（最高设计文档）。

也不是：

Architecture Backlog（架构待办）。

它回答的问题只有一个：

**为什么（Why）？**

每一个 Architecture Decision（架构决策）。

都应记录：

- 背景（Background）
- 问题（Problem）
- 可选方案（Alternatives）
- 最终决策（Decision）
- 决策原因（Reason）
- 影响（Impact）
- 状态（Status）

Architecture Decision Log。

保证：

所有重要架构决策。

均可长期追溯。

---

# ADR-001

## 建立 AI Drama Factory，而不是继续扩展 Crawlee

### Background（背景）

项目最初。

所有工作都建立在 Crawlee Prototype 上。

随着功能不断增加。

Spider。

Director。

Renderer。

Publishing。

逐渐形成了一条完整流水线。

但是。

整个项目仍然以：

脚本集合（Script Collection）的方式存在。

长期维护成本不断增加。

---

### Problem（问题）

是否继续在 Crawlee 上不断扩展？

还是：

建立新的长期项目？

---

### Alternatives（候选方案）

方案 A：

继续维护 Crawlee。

方案 B：

建立全新的：

AI Drama Factory。

---

### Decision（决策）

选择：

方案 B。

建立：

AI Drama Factory。

Crawlee。

定位为：

Prototype（原型）。

AI Drama Factory。

定位为：

长期软件项目。

---

### Reason（原因）

Factory。

需要：

统一架构。

统一知识体系。

统一治理。

长期演进能力。

这些目标。

Prototype 无法满足。

---

### Impact（影响）

建立：

Handbook。

Architecture。

Governance。

Knowledge。

Factory。

进入：

长期软件工程阶段。

---

### Status

Accepted

---

# ADR-002

## Handbook First（Handbook 优先）

### Background

项目初期。

一直采用：

Coding First。

随着复杂度增加。

代码越来越难维护。

Prompt。

Workflow。

Architecture。

不断变化。

---

### Decision

正式确立：

Handbook First。

Architecture。

必须先于：

Implementation。

---

### Reason

Handbook。

作为：

Highest Design Authority（最高设计文档）。

能够保证：

统一设计。

统一语言。

统一标准。

---

### Impact

开发流程。

升级为：

Handbook

↓

Architecture

↓

Implementation

↓

Review

↓

Release

---

### Status

Accepted

---

# ADR-003

## Workshop Architecture（车间架构）

### Background

最初。

Spider。

Director。

Renderer。

只是：

独立脚本。

---

### Decision

统一抽象为：

Workshop。

所有生产能力。

均以：

Workshop。

形式存在。

---

### Reason

Workshop。

符合：

Factory。

工业化架构思想。

具有：

独立输入。

独立输出。

独立升级。

可替换。

---

### Impact

建立：

Workshop Registry。

Production Workflow。

ADF-OS。

---

### Status

Accepted

---

# ADR-004

## Capability First（能力优先）

### Background

不同 Provider。

不断变化。

模型不断升级。

---

### Decision

Factory。

统一依赖：

Capability。

而不是：

Provider。

---

### Reason

Capability。

生命周期远大于：

Provider。

避免：

Vendor Lock-in（供应商绑定）。

---

### Impact

建立：

Capability Layer。

Provider Layer。

Model Router。

---

### Status

Accepted

---

# ADR-005

## Provider Independent（能力提供方无关）

### Background

Factory。

经历了：

OpenAI。

硅基流动。

GPT-Image-2。

ComfyUI。

等多个 Provider。

---

### Decision

Factory。

永远不绑定：

具体 Provider。

---

### Reason

保证：

Replaceability（可替换）。

Scalability（可扩展）。

Future Compatibility（未来兼容）。

---

### Impact

Provider。

可自由替换。

Architecture。

保持稳定。

---

### Status

Accepted

---

# ADR-006

## SQLite 作为 V1 数据库

### Background

曾讨论：

SQLite。

PostgreSQL。

MongoDB。

MySQL。

最终目标。

是：

快速完成：

Factory MVP。

---

### Decision

V1。

统一采用：

SQLite。

未来。

根据规模。

升级 PostgreSQL。

---

### Reason

SQLite：

零运维。

零部署。

稳定。

简单。

适合单机 Factory。

---

### Impact

降低：

MVP 开发复杂度。

后续。

通过 Data Layer。

实现数据库迁移。

---

### Status

Accepted

---

# ADR-007

## GPT-Image-2 作为 V1 Renderer

### Background

Renderer。

曾测试：

Kolors。

Qwen Image。

硅基流动。

GPT-Image-2。

---

### Decision

V1 Renderer。

统一采用：

GPT-Image-2。

---

### Reason

角色一致性。

真实感。

稳定性。

整体质量。

明显优于：

其它测试方案。

满足：

Factory MVP。

---

### Impact

第四车间。

正式冻结：

renderer_gpt_image2.js。

renderer_cloud.js。

归档。

---

### Status

Accepted

---

# ADR-008

## Freeze Handbook V1

### Background

Handbook。

不断完善。

如果持续修改。

Architecture。

将始终不稳定。

---

### Decision

完成：

Handbook V1。

正式 Freeze。

未来。

新增能力。

首先进入：

Architecture Backlog。

---

### Reason

保持：

Architecture Stability（架构稳定）。

Innovation（创新）。

之间平衡。

---

### Impact

建立：

Architecture Review。

Architecture Backlog。

Version Evolution。

---

### Status

Accepted

---

# ADR-009

## Dual Workspace（双工作区）

### Background

Architecture。

主要在：

Obsidian。

Implementation。

主要在：

VS Code。

---

### Decision

正式建立：

Architecture Workspace

↓

Engineering Workspace

开发模式。

---

### Reason

Architecture。

与：

Implementation。

职责完全不同。

应分别管理。

---

### Impact

Obsidian。

成为：

Architecture Center。

VS Code。

成为：

Engineering Center。

---

### Status

Accepted

---

# ADR-010

## Architecture Review（架构评审）

### Background

过去。

很多想法。

直接进入：

代码。

导致：

频繁重构。

---

### Decision

所有重大 Architecture。

统一经过：

Architecture Review。

之后。

才能进入：

Handbook。

或：

Implementation。

---

### Reason

Architecture。

需要：

长期稳定。

避免：

短期冲动设计。

---

### Impact

建立：

Architecture Review Process。

Architecture Governance。

Architecture Evolution。

---

### Status

Accepted

---

# Summary（总结）

Architecture Decision Log。

不是：

开发日志。

也不是：

更新记录。

它记录的是：

AI Drama Factory 在长期演进过程中做出的重大架构决策。

这些决策。

共同构成：

Factory 的 Architecture History（架构历史）。

未来。

所有新的 Architecture Decision。

均应继续追加：

ADR-011。

ADR-012。

ADR-013。

……

保持：

编号永久有效。

历史永久保留。

确保：

每一个重要决策。

都能够回答：

为什么。

---

**End**