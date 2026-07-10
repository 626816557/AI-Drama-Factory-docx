

---

# 文档说明（Document Description）

本文件用于规范 AI Drama Factory 项目中，人类开发者与 AI 助手之间的协作方式。

所有参与本项目开发的 AI，都应首先阅读本文件，并严格遵循其中的规则。

本规则适用于：

- ChatGPT
- Claude
- Gemini
- Cursor
- GitHub Copilot
- 未来接入的其它 AI 助手

---

# 第一原则：Handbook 优先（Handbook First）

Handbook 是整个 AI Drama Factory 的最高设计文档。

任何开发工作，都不得违反 Handbook 已确认的内容。

若发现 Handbook 存在问题，应先提出建议。

未经确认，不允许直接修改 Handbook。

---

# 第二原则：Architecture First（架构优先）

任何重要功能，应遵循：

需求分析

↓

架构设计

↓

Handbook 更新

↓

代码开发

↓

测试验证

↓

正式发布

禁止直接进入编码。

---

# 第三原则：Freeze 优先（Freeze First）

已经确认（Freeze）的设计原则上不再修改。

若发现新的更优方案：

先进入 Backlog。

待阶段结束统一评审。

不得频繁推翻已经确认的设计。

保持整个 Factory 架构稳定演进。

---

# 第四原则：职责单一（Single Responsibility）

每一个模块只负责一件事情。

例如：

Workshop

负责生命周期。

Service

负责业务协调。

Provider

负责第三方能力。

任何模块都应避免承担多个职责。

---

# 第五原则：代码服从架构（Code Follows Architecture）

代码不是项目的最高标准。

架构才是。

如果代码与架构冲突，应优先调整代码，而不是修改架构。

保持整个 Factory 长期一致性。

---

# 第六原则：避免一次性重构（Incremental Refactoring）

任何较大的系统迁移，应采用渐进式重构。

推荐方式：

建立新架构。

↓

逐步迁移职责。

↓

每完成一步立即验证。

↓

确认稳定后继续下一步。

避免一次性复制大量旧代码。

---

# 第七原则：及时发现重复（Avoid Duplication）

开发过程中，应主动识别：

重复代码。

重复设计。

重复文档。

重复职责。

如果发现重复，应及时提出优化建议。

保持整个 Factory 简洁、统一。

---

# 第八原则：统一数据来源（Single Source of Truth）

同一种信息，只允许维护一个正式来源。

例如：

项目设计：

Handbook。

当前开发状态：

PROJECT_STATE。

架构决策：

ARCHITECTURE_DECISIONS。

未来规划：

BACKLOG。

禁止多个文档维护相同内容。

---

# 第九原则：开发与设计分离（Separate Design and Development）

Handbook 负责设计。

Development 负责开发。

代码仓库负责实现。

三者职责清晰，不相互混用。

---

# 第十原则：长期主义（Long-term Thinking）

AI Drama Factory 是一个长期工程。

任何设计，都应优先考虑：

可维护性。

可扩展性。

可替换性。

可测试性。

避免为了短期效率破坏整体架构。

---

# AI 工作方式（Working Style）

AI 应主动发现问题。

AI 应提出合理建议。

AI 可以质疑当前设计。

但不应频繁推翻已经确认的架构。

对于新的架构设想，应优先进入 Backlog。

只有经过确认，才能进入正式开发。

---

# 最终目标（Final Goal）

AI 的职责，不只是帮助编写代码。

更重要的是协助建设一套能够持续演进、长期维护、具备工业化能力的 AI Drama Factory。

所有建议，都应服务于这一最终目标。