

---

# 文档说明（Document Description）

本文件用于记录 AI Drama Factory 在开发过程中产生的未来规划、优化建议以及架构设想。

所有记录在本文件中的内容，并不代表立即开发。

Backlog 的存在，是为了避免开发过程中频繁推翻已经确认的设计。

任何新的想法，应先进入 Backlog，待当前阶段结束后统一评估。

只有经过确认的内容，才允许进入 Handbook 或正式开发。

因此，本文件是整个项目的「未来规划池」。

---

# 当前原则（Current Principle）

AI Drama Factory 当前遵循：

**先完成，再优化。**

开发过程中，若发现新的设计思路，应记录到 Backlog，而不是立即修改当前架构。

保持项目稳定推进，避免因频繁调整导致开发节奏混乱。

---

# Backlog 001

## Collector Provider（采集提供者架构）

当前 Spider Workshop 已规划 Browser Provider。

未来 Collector 也建议采用 Provider 模式。

例如：

- Douyin Provider
- TikTok Provider
- YouTube Provider
- Instagram Provider

通过统一接口支持多个内容平台。

当前状态：

待评估。

---

# Backlog 002

## DramaSeed Standard（统一种子数据结构）

Spider 输出的数据建议统一定义为 DramaSeed。

所有后续 Workshop 均围绕 DramaSeed 工作。

未来需要设计完整的数据模型以及数据库表结构。

当前状态：

待设计。

---

# Backlog 003

## Event Bus（事件总线）

未来所有 Workshop 可以通过统一事件总线通信。

例如：

Spider 完成采集。

↓

发送 Spider.Completed。

↓

Mapper 自动开始。

减少不同 Workshop 之间直接调用。

当前状态：

待评估。

---

# Backlog 004

## Workflow Engine（工作流引擎）

未来 Factory 不再依赖固定流程。

由 Workflow Engine 统一调度：

Spider

↓

Mapper

↓

Validator

↓

Director

↓

Image

↓

Video

↓

Publisher

支持自由组合不同生产流程。

当前状态：

长期规划。

---

# Backlog 005

## ADF OS（可视化控制中心）

未来建设 AI Drama Factory Operating System。

提供统一控制界面。

包括：

- Factory Dashboard
- Workshop Monitor
- Task Queue
- Production Status
- Project Management
- Database Viewer
- Log Center
- Cost Analysis
- AI Provider Monitor

当前状态：

M3 开始规划。

---

# Backlog 006

## Cloud Runtime（云端运行环境）

未来支持：

本地开发。

↓

云服务器运行。

↓

GPU 集群。

↓

多节点生产。

支持不同 Runtime 自动切换。

当前状态：

长期规划。

---

# Backlog 007

## AI Provider Center（AI 服务中心）

未来所有 AI 能力统一管理。

包括：

- LLM
- Image
- Video
- TTS
- STT
- Translation

支持：

OpenAI

DeepSeek

Gemini

Claude

ComfyUI

本地模型。

避免各个 Workshop 直接依赖第三方 API。

当前状态：

待规划。

---

# Backlog 008

## Asset Center（资产中心）

未来统一管理：

图片。

视频。

音频。

字幕。

角色。

服装。

Prompt。

Reference。

实现整个 Factory 的生产资产管理。

当前状态：

长期规划。

---

# Backlog 009

## Knowledge Center（知识中心）

未来建立 Factory Knowledge Base。

包括：

爆款分析。

Prompt 模板。

角色模板。

运镜模板。

海外短剧规律。

实现 AI 持续学习与知识积累。

当前状态：

长期规划。

---

# Backlog 维护规则（Maintenance Rules）

新的想法统一追加到本文件。

不允许直接修改已完成架构。

每完成一个 Milestone（阶段里程碑），统一评审一次 Backlog。

评审通过后，可进入：

Architecture Decisions

↓

Handbook

↓

Development

形成正式开发计划。

未评审前，Backlog 中所有内容均视为未来规划，不参与当前开发。