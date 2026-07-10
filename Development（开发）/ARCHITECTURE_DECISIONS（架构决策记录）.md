

---

# 文档说明（Document Description）

本文件用于记录 AI Drama Factory 项目中已经确认并正式生效的架构决策。

所有记录在本文件中的内容，均视为项目已经达成一致的设计方案（Freeze）。

后续开发过程中，所有代码实现、Workshop 设计以及系统演进，都必须遵循本文件记录的架构原则。

若未来需要调整已经确认的架构，不允许直接修改代码，而应先提出新的 Architecture Proposal（架构提案），经过评估后再更新本文件。

因此，本文件是整个 AI Drama Factory 的工程架构依据。

---

# Decision 001

## Directory Architecture（项目目录架构）

确认时间：

2026-07-07

---

项目目录正式采用模块化结构。

整个工程划分为：

- Foundation（基础层）
- Persistence（持久化层）
- Kernel（内核）
- Workshops（生产车间）
- Centers（中心模块）
- Operations（运营模块）

所有新功能均按照所属职责进入对应目录。

不得继续使用大量脚本堆积在 src 根目录的开发方式。

当前状态：

**Freeze（已确认）**

---

# Decision 002

## Workshop Architecture（生产车间架构）

确认时间：

2026-07-07

---

所有业务能力统一采用 Workshop 架构。

每一个 Workshop 都必须遵循统一结构：

Workshop

↓

Service（协调层）

↓

多个职责 Service

↓

Provider（外部能力）

Workshop 只负责生命周期管理。

Service 负责业务协调。

Provider 负责调用第三方能力。

任何 Workshop 不允许直接耦合第三方 SDK。

当前状态：

**Freeze（已确认）**

---

# Decision 003

## Browser Provider Pattern（浏览器提供者模式）

确认时间：

2026-07-07

---

Spider Workshop 不直接依赖 Playwright。

统一采用 Browser Service + Browser Provider 架构。

Browser Service 作为统一入口。

具体浏览器实现由不同 Provider 完成。

目前已经规划：

- Playwright Provider
- Puppeteer Provider
- Remote Browser Provider
- Browserless Provider

未来新增浏览器能力时，不修改 Spider Service，仅增加新的 Provider。

当前状态：

**Freeze（已确认）**

---

# Decision 004

## Database Architecture（数据库架构）

确认时间：

2026-07-07

---

SQLite 被确定为 AI Drama Factory 的正式数据源（Source of Truth）。

所有 Workshop 的正式数据均存入 SQLite。

JSON 文件仅承担：

- 调试输出
- 快照备份
- 数据回放
- 开发排查

任何正式业务流程均不再依赖 JSON 文件进行数据交换。

当前状态：

**Freeze（已确认）**

---

# Decision 005

## Data Flow（数据流架构）

确认时间：

2026-07-07

---

Factory 内部统一采用流水线数据流。

数据依次经过：

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

↓

Analytics

所有 Workshop 均通过统一数据结构进行协作。

避免不同 Workshop 之间直接耦合。

当前状态：

**Freeze（已确认）**

---

# Decision 006

## Architecture First（架构优先原则）

确认时间：

2026-07-07

---

AI Drama Factory 始终坚持：

Architecture First。

任何较大的功能开发，应遵循：

Idea

↓

Architecture Design

↓

Handbook

↓

Development

↓

Testing

↓

Release

禁止先写代码，再补设计。

当前状态：

**Freeze（已确认）**

---

# 后续维护规则（Maintenance Rules）

新增架构决策时：

按 Decision 编号顺序继续追加。

例如：

Decision 007

Decision 008

……

已经确认的 Decision 原则上不修改。

若确需调整，应记录新的 Decision，并说明替代关系，而不是直接覆盖历史记录。

---

# Decision 007

## Platform Adapter Architecture（平台适配器架构）

确认时间：

2026-07-10

---

Spider Workshop 正式采用 Platform Adapter Architecture。

Spider Service 不再直接依赖任何平台。

统一通过 Adapter 接口完成平台采集。

目前已实现：

- Douyin Adapter

未来规划：

- TikTok Adapter
- YouTube Adapter
- Instagram Adapter
- Facebook Adapter
- Kwai Adapter

Spider Service 仅负责统一调度。

每个平台独立实现：

- API 获取
- Parser
- 平台特性

新增平台时，不修改 Spider 核心逻辑，仅新增 Adapter。

当前状态：

**Freeze（已确认）**
---

# Decision 008

## Repository Pattern（仓储模式）

确认时间：

2026-07-10

---

Spider Workshop 正式采用 Repository Pattern。

所有数据库读写统一进入 Repository。

目前：

Seed Repository

负责：

- Insert
- Update
- Upsert
- Query

Spider Service 不允许直接操作 SQLite。

未来：

所有 Workshop 均采用 Repository Pattern。

例如：

Mapper Repository

Validator Repository

Director Repository

Image Repository

Publisher Repository

统一保持数据访问层一致。

当前状态：

**Freeze（已确认）**
---

# Decision 009

## Production Collection Mode（生产采集模式）

确认时间：

2026-07-10

---

Spider Workshop 正式区分：

Development Mode

用于开发验证。

Production Mode

用于正式生产。

Production Mode 支持：

- 多页采集
- 最大采集数量限制
- 自动停止
- 去重
- 排名修正
- 数据验证

不同平台可以拥有各自默认配置。

Spider Service 仅负责执行。

采集策略由配置决定。

当前状态：

**Freeze（已确认）**
---

# Decision 010

## Spider Production Pipeline（Spider生产流水线）

确认时间：

2026-07-10

---

Spider Workshop 正式确定统一生产流水线。

所有平台统一遵循：

Browser

↓

Platform Adapter

↓

Parser

↓

Validator

↓

Repository

↓

SQLite

任何平台均不得绕过其中任意步骤。

未来新增平台，仅替换：

Platform Adapter

Parser

其余流程保持一致。

当前状态：

**Freeze（已确认）**