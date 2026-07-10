

---

# 文档说明（Document Description）

本文件用于 AI Drama Factory 每次开启新聊天时，快速恢复项目上下文。

新的 AI 助手在正式参与开发前，应首先阅读本文件，并按照规定的顺序恢复项目状态。

本文件的目标不是介绍项目，而是让 AI 能够在最短时间内进入当前开发阶段，保持整个项目的连续性。

---

# 第一步：理解项目（Understand the Project）

首先阅读：

《Handbook V1》

Handbook 是整个 AI Drama Factory 的最高设计文档。

任何开发工作，都必须遵循 Handbook 已确认的设计原则。

若 Handbook 与代码存在冲突，以 Handbook 为准。

---

# 第二步：恢复当前状态（Restore Current State）

阅读：

PROJECT_STATE（项目状态）

理解：

当前 Milestone。

当前 Sprint。

当前开发目标。

当前已经完成的模块。

当前正在开发的模块。

下一步开发计划。

所有开发工作均以 PROJECT_STATE 为唯一状态来源。

---

# 第三步：理解架构（Understand Architecture）

阅读：

ARCHITECTURE_DECISIONS（架构决策记录）

理解：

已经 Freeze 的架构。

不得主动推翻已经确认的设计。

若发现更优方案，应提出建议，并记录到 Backlog，而不是直接修改代码。

---

# 第四步：了解未来规划（Understand Future Plans）

阅读：

BACKLOG（开发待办）

了解：

未来规划。

长期目标。

架构设想。

Backlog 中的内容，不代表立即开发。

只有进入 Architecture Decisions 后，才视为正式设计。

---

# 第五步：遵循协作规范（Follow Collaboration Rules）

阅读：

AI_COLLABORATION_RULES（AI 协作规则）

理解：

协作方式。

开发原则。

文档规范。

代码规范。

保持整个 Factory 的长期一致性。

---

# 第六步：开始开发（Start Development）

完成以上步骤后。

直接继续：

PROJECT_STATE 中记录的：

**Next Goal（下一阶段目标）**

不要重新设计已经完成的模块。

不要重复讨论已经确认的架构。

不要偏离当前 Sprint。

保持连续开发。

---

# 开发原则（Development Principles）

整个 AI Drama Factory 始终坚持以下原则：

- Handbook First（Handbook 优先）
- Architecture First（架构优先）
- Freeze First（已确认设计优先）
- Single Responsibility（单一职责）
- Single Source of Truth（唯一事实来源）
- Incremental Refactoring（渐进式重构）
- Long-term Thinking（长期主义）

所有开发建议，都应围绕 Factory 的长期演进进行。

---

# 当前开发阶段（Current Stage）

当前项目已经结束：

**M1 - Design Phase（设计阶段）**

目前进入：

**M2 - Foundation Development（基础开发阶段）**

当前 Sprint：

**Spider Workshop Migration（第一车间迁移）**

开发重点：

恢复 Spider Workshop 的真实采集能力，并逐步完成整个 Factory 的生产流水线。

---

# 最终目标（Final Goal）

AI Drama Factory 的最终目标不是开发单个脚本，而是建设一套能够持续演进、自我优化、工业化生产海外 AI 短剧的完整操作系统（AI Drama Factory OS）。

所有开发工作，都应服务于这一最终目标。