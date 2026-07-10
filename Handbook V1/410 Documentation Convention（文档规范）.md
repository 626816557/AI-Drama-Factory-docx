

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

> **AI Drama Factory 应如何设计、组织和维护整个项目文档体系？**

Documentation Convention 定义整个 Factory 的文档规范。

包括：

- Handbook
- README
- ADR
- RFC
- API Documentation
- Developer Guide

文档是 Factory 的长期知识资产。

---

# 二、设计目标（Purpose）

优秀文档应满足：

- 唯一来源
- 长期维护
- 易阅读
- 易搜索
- 易更新
- 易协作

文档不是开发结束后的补充。

而是开发工作的组成部分。

---

# 三、核心原则（Core Principles）

Factory 坚持：

## Documentation First

任何重要设计。

先有文档。

后有代码。

---

## Single Source of Truth

同一知识。

只能存在一个权威文档。

避免：

多个地方描述同一件事情。

---

## Documentation Is Product

Handbook 本身。

就是 Factory 的产品资产。

而不是开发记录。

---

## Continuous Maintenance

文档应持续维护。

代码修改。

文档同步更新。

避免：

文档长期失效。

---

# 四、文档分类（Document Categories）

Factory 定义以下文档类型。

---

## Handbook

整个 Factory 的最高设计文档。

负责：

Business

Architecture

Convention

Workshop

Core System

Operations

Handbook 是整个项目最高规范。

---

## README

负责：

快速介绍项目。

包括：

- 项目简介
- 环境安装
- 快速启动
- 常见命令

README 不负责设计说明。

---

## ADR（Architecture Decision Record）

用于记录：

重要架构决策。

例如：

为什么选择 PostgreSQL？

为什么采用 Workshop？

为什么不用微服务？

ADR 保存：

设计原因。

而不是最终规范。

---

## RFC（Request for Comments）

用于：

讨论未来设计。

尚未 Freeze。

允许修改。

RFC 不属于正式规范。

---

## API Documentation

负责：

所有 API。

包括：

输入。

输出。

错误码。

示例。

API 文档应自动生成或统一维护。

---

## Developer Guide

负责：

帮助开发者快速参与项目。

例如：

目录说明。

开发流程。

调试方法。

部署方式。

---

# 五、文档生命周期（Document Lifecycle）

所有正式文档。

遵循：

```
Draft

↓

Review

↓

Freeze

↓

Version

↓

Maintain
```

只有 Freeze 后。

才能作为正式规范。

---

# 六、文档版本（Document Version）

重要文档。

应具有：

- Version
- Status
- Owner
- Last Update

保持统一格式。

方便长期维护。

---

# 七、Handbook 的地位（Handbook Priority）

Factory 明确规定：

```
Handbook

>

Code

>

Comments

>

Chat Record
```

当出现冲突时。

应优先检查 Handbook。

聊天记录。

不是正式规范。

---

# 八、Obsidian 的定位（Obsidian Position）

Obsidian 是：

知识管理工具。

不是项目资产。

正式项目资产。

始终保存在：

```
handbook/
```

Obsidian 可用于：

阅读。

编辑。

整理。

但不是最终来源。

---

# 九、Git 与文档

所有正式文档。

均进入 Git。

文档与代码。

保持同步版本管理。

任何重要设计。

均应拥有历史记录。

---

# 十、文档 Review

任何重要文档。

进入 Freeze 前。

均应经过：

Review。

确保：

准确。

完整。

一致。

---

# 十一、设计原则（Design Principles）

Factory 坚持：

## Documentation Before Development

先设计。

后开发。

---

## Documentation As Asset

文档属于长期资产。

---

## One Truth

唯一事实来源。

---

## Version Controlled

文档版本化。

---

## Long-term Maintainability

支持长期维护。

---

# 十二、Non-Goals（非目标）

本章不负责：

- Git 规范（404）
- Prompt 规范（407）
- API 实现（408）
- 数据库实现（409）

---

# 十三、Dependencies（依赖关系）

Depends On：

- 400 Project Convention

Affects：

- Handbook
- README
- ADR
- RFC
- Developer Guide
- 全部开发流程

---

# 十四、本章总结

Documentation Convention 定义了 AI Drama Factory 的文档体系。

Factory 不把文档当作附属品。

而把文档视为：

整个项目最重要的知识资产。

未来。

任何设计。

任何规范。

任何长期决策。

都应首先进入文档。

再进入代码。

---

**End**