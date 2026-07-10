# 

> Version：V1.0
>
> Status：Freeze
>
> Last Update：2026-07-01
>
> Owner：AI Drama Factory

---

# 一、Handbook 是什么？

AI Drama Factory Handbook 是整个 AI Drama Factory 项目的官方知识库（Official Handbook）。

它不是聊天记录。

不是临时笔记。

不是 Word 文档。

也不是需求文档（PRD）。

Handbook 是整个项目唯一可信来源（Single Source of Truth，SSOT）。

所有产品设计、软件架构、开发规范、数据库设计、AI 工作流、运营策略以及重大决策，都记录于此。

任何开发工作，都必须以 Handbook 为准。

---

# 二、为什么需要 Handbook？

AI Drama Factory 将持续迭代多年。

未来将包含：

- 软件开发
- AI 模型
- 云 GPU
- 数据库
- 可视化系统
- 内容运营
- 商业模式
- 团队协作

随着项目不断扩大，仅依靠聊天记录或个人记忆，最终一定会产生理解偏差。

Handbook 的存在，就是为了保证：

- 所有人理解一致
- 所有设计都有依据
- 所有决策都可以追溯
- 所有开发都有统一标准

Handbook 永远先于代码。

---

# 三、Handbook 的使用原则

Handbook 是整个项目最高级别文档。

遵循以下原则：

## 1、唯一可信来源（Single Source of Truth）

任何架构设计。

以 Handbook 为准。

而不是聊天记录。

---

## 2、先更新文档，再修改代码

任何重大修改。

必须：

Handbook

↓

代码

而不是：

代码

↓

补文档

---

## 3、持续演进

Handbook 不断更新。

但任何重大修改，都必须经过 Review。

---

## 4、保持一致

所有文档。

统一：

格式。

编号。

命名。

章节结构。

阅读体验。

---

# 四、如何阅读 Handbook？

第一次阅读建议按照编号顺序阅读。

```
000
↓

001

↓

002

↓

003

......

```

不要跳跃阅读。

每一章都会建立在上一章的基础之上。

---

# 五、Handbook 的整体结构

整个 Handbook 分为十个部分。

```
Preface（前言）

↓

Business（商业）

↓

Architecture（软件架构）

↓

Project Convention（项目规范）

↓

Core System（核心系统）

↓

Workshop Design（车间设计）

↓

ADF-OS（可视化控制中心）

↓

AI Infrastructure（AI基础设施）

↓

Operations（运营）

↓

Appendix（附录）
```

每一个部分，只回答一类问题。

共同组成完整的 AI Drama Factory。

---

# 六、Handbook 与 Project 的关系

AI Drama Factory 包含两个部分。

```
AI Drama Factory

├── Project（软件工程）
│
└── Handbook（项目知识库）
```

Project 负责：

软件开发。

Handbook 负责：

软件设计。

Handbook 决定：

Project 如何开发。

Project 实现：

Handbook 的设计。

两者共同组成 AI Drama Factory。

---

# 七、当前项目阶段

当前项目正在进行：

**Foundation（基础设计阶段）**

当前目标：

建立整个 AI Drama Factory 的基础设计体系。

包括：

- 商业设计
- 软件架构
- 项目规范
- 数据结构
- 工厂设计

Foundation 完成后。

正式进入软件开发阶段。

---

# 八、文档状态说明

每一份文档都会标记当前状态。

| 状态 | 含义 |
|------|------|
| Draft | 草稿，允许修改 |
| Review | 评审中 |
| Freeze Candidate | 冻结候选 |
| Freeze | 已冻结，不再随意修改 |
| Deprecated | 已废弃，仅供历史参考 |

---

# 九、版本管理

Handbook 采用版本管理。

例如：

V1.0

V1.1

V2.0

所有重大架构调整。

必须记录版本。

并保留历史修改记录。

---

# 十、本章总结

Handbook 是 AI Drama Factory 最重要的资产之一。

它不仅记录系统如何设计。

更决定系统未来如何发展。

以后：

任何新的设计。

任何新的架构。

任何新的模块。

都应首先更新 Handbook。

然后再开始开发。

---

**End**