
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

> **AI Drama Factory 项目目录应如何组织，才能支持长期维护与持续扩展？**

Directory Convention 定义整个项目的目录结构。

它不是某一次开发的目录。

而是整个 Factory 的长期组织方式。

---

# 二、设计目标（Purpose）

目录不仅用于存放文件。

更用于表达整个系统结构。

优秀目录应满足：

- 易理解
- 易查找
- 易维护
- 易扩展
- 易协作

任何开发人员。

打开目录后。

都应能够快速理解整个 Factory。

---

# 三、设计原则（Core Principles）

Directory Convention 遵循以下原则。

## Business Oriented

目录围绕业务组织。

而不是围绕技术组织。

例如：

使用：

Project

Workshop

Asset

而不是：

Utils

Helpers

Misc

---

## Single Responsibility

每个目录只负责一种职责。

避免：

一个目录承担多个功能。

---

## Layer Separation

不同层级严格隔离。

例如：

Frontend

Backend

Workers

Database

不得互相混放。

---

## Scalability

新增模块时。

无需修改已有目录。

保持长期稳定。

---

## Predictability

任何开发人员。

都能够预测：

一个文件应该放在哪里。

而不是靠经验寻找。

---

# 四、推荐目录结构

```
AI-Drama-Factory/

│

├── handbook/                # ADF Handbook（最高设计文档）

├── frontend/                # ADF-OS（Vue 前端）

├── backend/                 # Backend API

├── core/                    # Core System

├── workshops/               # 全部生产车间

├── adapters/                # AI Adapter

├── database/                # 数据层

├── storage/                 # 文件存储

├── configs/                 # 配置中心

├── scripts/                 # 开发脚本

├── deploy/                  # 部署配置

├── tests/                   # 测试

├── docs/                    # 补充文档

└── tools/                   # 开发工具
```

以上目录作为 V1 标准目录。

---

# 五、Handbook

handbook/

用于保存：

整个 AI Drama Factory 的设计文档。

包括：

- Business
- Architecture
- Convention
- Workshop
- Data
- Operations

Handbook 是整个项目最高规范。

---

# 六、Frontend

frontend/

负责：

ADF-OS。

包括：

- Dashboard
- Project Center
- Workshop Center
- Asset Center
- Analytics
- Settings

Frontend 不包含业务逻辑。

仅负责用户交互。

---

# 七、Backend

backend/

负责：

统一 API。

包括：

- REST API
- WebSocket
- SSE
- Authentication
- Authorization

Backend 是系统统一入口。

---

# 八、Core

core/

负责：

整个 Factory 的核心能力。

例如：

- Scheduler
- Event Bus
- Plugin
- Workflow
- Configuration
- Logging

Core 不包含具体业务。

---

# 九、Workshops

workshops/

负责：

所有内容生产车间。

例如：

- Market Intelligence
- Story Intelligence
- Validation
- Director
- Asset Generation
- Video Generation
- Publishing
- Learning

每个 Workshop 拥有独立目录。

互不依赖实现。

---

# 十、Adapters

adapters/

负责：

所有第三方能力适配。

例如：

- OpenAI
- Claude
- Gemini
- DeepSeek
- GPT Image
- Seedance
- TTS
- Storage

业务层不得直接调用第三方 SDK。

统一通过 Adapter。

---

# 十一、Database

database/

负责：

数据访问层。

包括：

- Schema
- Entity
- Repository
- Migration
- Seed

Database 不保存业务逻辑。

---

# 十二、Storage

storage/

负责：

Factory 所有文件资产。

包括：

- Images
- Videos
- Audio
- Subtitle
- Cache
- Temp

Storage 统一管理。

支持未来切换对象存储。

---

# 十三、Configs

configs/

负责：

所有配置。

包括：

- Environment
- AI Provider
- Database
- Worker
- Deployment

配置与代码严格分离。

---

# 十四、Scripts

scripts/

负责：

开发辅助脚本。

例如：

- Build
- Dev
- Migration
- Backup
- Clean

Scripts 不属于业务系统。

---

# 十五、Deploy

deploy/

负责：

部署能力。

包括：

- Docker
- Compose
- Kubernetes
- CI
- Release

统一管理部署资源。

---

# 十六、Tests

tests/

负责：

测试。

包括：

- Unit Test
- Integration Test
- E2E Test

所有测试统一管理。

---

# 十七、Docs

docs/

负责：

补充说明。

例如：

教程。

设计记录。

RFC。

ADR。

注意：

最高设计文档始终位于 handbook/。

---

# 十八、Tools

tools/

负责：

开发辅助工具。

例如：

CLI。

数据转换。

日志分析。

图片处理。

Tools 不参与正式业务运行。

---

# 十九、目录管理原则

任何新增目录。

都必须：

- 有明确职责。
- 有 Owner。
- 有文档。
- 不与已有目录重复。

禁止出现：

```
misc/

other/

new/

temp2/

最终版/

最新版/
```

这类无法表达职责的目录名称。

---

# 二十、Non-Goals（非目标）

本章不负责：

- 文件命名（见 402）
- Git 规范（见 404）
- Prompt 规范（见 407）
- 数据库设计（见 409）

---

# 二十一、Dependencies（依赖关系）

Depends On：

- 300 Overall Architecture
- 301 Product Architecture
- 302 Technical Architecture

Affects：

- 全部代码目录
- 全部开发规范
- 全部 Workshop
- ADF-OS
- 部署系统

---

# 二十二、本章总结

Directory Convention 定义了 AI Drama Factory 的目录组织方式。

目录不是简单的文件夹。

而是整个软件架构的映射。

未来。

任何新增模块。

都应首先考虑：

> **它属于哪个目录？**

而不是：

> **放在哪里方便。**

---

**End**