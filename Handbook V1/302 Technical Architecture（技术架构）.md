

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

> **AI Drama Factory 应采用什么样的技术架构来支撑长期发展？**

Technical Architecture 定义系统的技术实现方式。

它描述：

- 系统如何拆分
- 服务如何通信
- 数据如何流动
- AI 如何接入
- 如何保证系统能够持续扩展

本章不涉及具体业务逻辑。

业务设计由 Product Architecture 和 Workshop Design 定义。

---

# 二、架构目标（Purpose）

AI Drama Factory 的技术架构应满足以下目标：

- 长期可维护
- 模块化设计
- 高扩展性
- 高可替换性
- 本地开发友好
- 云端部署友好
- AI 模型无绑定
- 数据长期沉淀

Factory 的生命周期应远大于任何一个 AI 模型。

---

# 三、总体技术架构

AI Drama Factory 采用分层技术架构。

```
┌────────────────────────────────────────────┐
│                 ADF-OS                     │
│         (Vue Desktop / Web UI)             │
└────────────────────────────────────────────┘
                    │
                    ▼
┌────────────────────────────────────────────┐
│                Backend API                 │
│      REST API / WebSocket / SSE            │
└────────────────────────────────────────────┘
                    │
                    ▼
┌────────────────────────────────────────────┐
│              Core System                   │
│ Scheduler │ Event │ Plugin │ Config │ Log  │
└────────────────────────────────────────────┘
                    │
        ┌───────────┴───────────┐
        ▼                       ▼
┌──────────────────┐   ┌────────────────────┐
│    Workshops      │   │ AI Infrastructure │
└──────────────────┘   └────────────────────┘
        │                       │
        └───────────┬───────────┘
                    ▼
┌────────────────────────────────────────────┐
│              Data Center                   │
└────────────────────────────────────────────┘
```

各层职责独立。

通过标准接口进行通信。

---

# 四、技术分层（Technical Layers）

Factory 划分为六层。

## 1、Presentation Layer（表现层）

负责：

用户交互。

包括：

- Dashboard
- Project Center
- Workshop Center
- Analytics
- System Settings

推荐技术：

Vue 3

TypeScript

Vite

Tailwind CSS

---

## 2、Application Layer（应用层）

负责：

API。

权限。

任务编排。

状态管理。

提供统一业务入口。

推荐技术：

Node.js

Express（初期）

后期可演进为 NestJS（根据项目规模评估）

---

## 3、Core Layer（核心层）

负责：

Factory 的核心能力。

包括：

- 生命周期管理
- Scheduler
- Event Bus
- Plugin
- Workflow
- Configuration

Core Layer 不包含具体业务。

只负责系统运行。

---

## 4、Workshop Layer（车间层）

负责：

所有 AI 内容生产。

例如：

- Market
- Story
- Director
- Asset
- Video
- Publishing
- Learning

每个 Workshop 应独立开发。

独立运行。

独立升级。

---

## 5、AI Infrastructure Layer（AI 基础设施层）

负责：

统一管理所有 AI 能力。

包括：

LLM

Image

Video

TTS

ASR

Translation

Embedding

任何模型。

都必须通过 Adapter 接入。

禁止业务直接调用第三方 API。

---

## 6、Data Layer（数据层）

负责：

所有长期数据。

包括：

Project

Character

IP

Asset

Analytics

Knowledge

Prompt

Data Layer 是整个 Factory 的长期资产。

---

# 五、通信方式（Communication）

不同层之间。

只能通过标准接口通信。

推荐：

```
UI

↓

REST API

↓

Core System

↓

Workshop

↓

AI Adapter

↓

Model
```

禁止：

UI 直接访问数据库。

Workshop 直接调用第三方模型。

保持系统解耦。

---

# 六、状态管理（State Management）

Factory 中所有任务都必须拥有统一状态。

建议状态如下：

```
Pending

↓

Queued

↓

Running

↓

Completed
```

异常状态：

```
Failed

Cancelled

Paused

Retrying
```

任何 Task。

Project。

Workshop。

都必须遵循统一状态机。

---

# 七、异步任务（Async Task）

AI 内容生产属于长任务。

因此：

所有耗时操作必须异步执行。

例如：

- GPT
- GPT-Image
- Seedance
- 视频渲染
- FFmpeg
- 上传平台

UI 不应等待任务完成。

而应实时接收状态更新。

---

# 八、日志系统（Logging）

所有模块。

统一输出日志。

日志至少包含：

- Time
- Project ID
- Workshop
- Task
- Level
- Message

所有日志统一管理。

便于调试和监控。

---

# 九、错误处理（Error Handling）

任何模块发生异常。

不得导致整个 Factory 停止运行。

应支持：

- Retry（重试）
- Skip（跳过）
- Resume（恢复）
- Manual Retry（人工重试）

保证生产流程具备容错能力。

---

# 十、设计原则（Design Principles）

Factory 技术架构遵循：

## 模块独立

模块之间保持低耦合。

---

## 接口优先

所有通信通过接口完成。

禁止直接依赖实现。

---

## Adapter 优先

任何第三方能力。

都必须经过 Adapter。

方便未来替换。

---

## 数据长期保存

所有重要数据。

默认长期保存。

支持分析。

支持学习。

支持复用。

---

## 云本地一致

本地开发。

云端部署。

保持统一架构。

避免维护两套系统。

---

# 十一、未来演进（Future Evolution）

未来技术架构支持：

- 微服务
- GPU Worker
- Kubernetes
- Serverless
- 多地区部署
- 多租户
- SaaS
- 企业私有化部署

当前阶段：

保持单体架构。

优先保证开发效率。

随着业务增长。

逐步演进。

---

# 十二、Development Mapping（开发映射）

本章对应未来项目目录：

```
frontend/
    Vue
    UI

backend/
    API
    Core

workers/
    Workshops

adapters/
    AI Adapter

database/
    Data Layer

shared/
    Types
    Config
    Utils
```

所有代码。

都应遵循本章定义的技术架构。

---

# 十三、本章总结

Technical Architecture 定义了 AI Drama Factory 的软件实现方式。

它不是某一种技术栈的说明书。

而是一套长期稳定的软件架构规范。

未来。

无论技术如何升级。

模型如何变化。

Factory 的整体技术架构都应保持稳定。

做到：

**技术可升级，架构不混乱；模型可替换，系统可持续。**

---

**End**