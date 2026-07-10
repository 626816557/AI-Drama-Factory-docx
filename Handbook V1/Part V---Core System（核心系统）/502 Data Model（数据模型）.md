
> Version：V2.0
>
> Status：Draft
>
> Last Update：2026-07-07
>
> Owner：AI Drama Factory

---

# 一、本文档回答什么问题？（Purpose）

本文档回答一个核心问题：

> AI Drama Factory 的世界（Factory World）由什么组成？

虽然本章名称为 **Data Model（数据模型）**，但它定义的不仅仅是数据库结构。

更重要的是：

**AI Drama Factory 的领域模型（Domain Model）。**

未来：

- 数据库（Database）
- API
- ADF-OS（控制中心）
- Kernel（内核）
- Workshops（生产车间）
- AI Agents（AI 智能体）

全部应建立在本模型之上。

Data Model 是整个 Factory 唯一统一的业务语言（Ubiquitous Language）。

---

# 二、为什么需要 Data Model？（Why）

AI Drama Factory 不是一个脚本。

也不是多个 AI 工具的组合。

它是一个持续运行、持续学习、持续演进的生产系统。

如果没有统一的数据模型：

不同模块会产生不同理解。

例如：

Character（角色）

到底属于：

Director？

Project？

还是 Asset？

不同答案会导致：

数据库混乱。

API 混乱。

代码混乱。

因此：

Factory 必须先拥有统一世界观。

然后再开发代码。

---

# 三、Factory World（Factory 世界）

整个 AI Drama Factory 可以抽象为一个完整世界。

这个世界由两部分组成：

```text
Factory World

├── Static World（静态世界）

└── Dynamic World（动态世界）
```

静态世界代表长期存在的知识与资源。

动态世界代表持续发生的生产活动。

Factory 正是在这两个世界之间不断循环运行。

---

# 四、Static World（静态世界）

Static World 保存 Factory 长期积累的能力。

它们通常不会因为某一个 Project 而消失。

它们可以不断沉淀。

不断复用。

不断成长。

Static World 包括：

## Character（角色）

Factory 的角色库。

包括：

身份。

外观。

Face Anchor。

服装。

年龄。

性格。

关系。

角色属于 Factory。

不是某一个 Project。

未来同一角色可以参与多个故事。

---

## Location（场景）

统一维护所有场景。

例如：

医院。

教堂。

办公室。

豪宅。

森林。

机场。

未来所有 Project 共用。

---

## Prompt（提示词）

Prompt 属于 Factory 资产。

不是字符串。

未来支持：

版本管理。

评分。

A/B Test。

自动优化。

---

## Template（模板）

包括：

故事模板。

镜头模板。

角色模板。

封面模板。

未来任何可复用模板都属于此领域。

---

## Knowledge（知识）

Factory 长期积累：

爆款规律。

失败经验。

运营经验。

最佳实践。

Prompt Engineering。

知识不会因为某一次生产结束而消失。

它属于整个 Factory。

---

## Provider（服务提供商）

Factory 所有 AI Provider。

例如：

OpenAI。

DeepSeek。

Gemini。

Claude。

Flux。

Seedance。

未来可以自由替换。

Provider 属于 Factory 基础资源。

---

# 五、Dynamic World（动态世界）

Dynamic World 是 Factory 每天都在发生的生产活动。

每一次生产都会产生新的对象。

生产结束后。

对象进入历史。

Dynamic World 包括：

## Project（项目）

Factory 的最高业务对象。

每一个 Project 对应一次完整内容生产。

例如：

《The Billionaire's Secret》

Project 是所有生产活动的起点。

---

## Workflow（工作流）

描述 Project 如何生产。

例如：

Research

↓

Planning

↓

Director

↓

Image

↓

Video

↓

Publishing

Workflow 定义流程。

不负责执行。

---

## Task（任务）

Workflow 被拆分为多个 Task。

Task 是最小执行单位。

例如：

生成第三幕图片。

生成标题。

上传 TikTok。

Task 可以：

暂停。

失败。

重试。

取消。

---

## Workshop（生产车间）

Workshop 负责执行 Task。

例如：

Director Workshop。

Image Workshop。

Video Workshop。

Workshop 不保存长期业务状态。

完成任务后立即返回。

---

## Asset（资产）

Factory 生产出来的一切成果。

包括：

图片。

视频。

音频。

字幕。

Prompt。

封面。

脚本。

参考图。

Asset 是生产结果。

未来可以进入 Static World 成为长期资产。

---

## Evaluation（评估）

保存质量评价。

包括：

一致性。

商业价值。

视觉质量。

剧情质量。

情绪强度。

Evaluation 为 Learning 提供依据。

---

## Publishing（发布）

记录：

发布时间。

平台。

账号。

状态。

URL。

收益。

播放数据。

Publishing 属于运营行为。

---

## Analytics（分析）

记录：

CTR。

Retention。

RPM。

ROI。

Watch Time。

Analytics 是 Factory 持续优化的重要依据。

---

# 六、世界之间的关系（World Relationship）

Static World 与 Dynamic World 持续相互作用。

```text
Static World

↓

Knowledge

Character

Prompt

Template

↓

Project

↓

Workflow

↓

Workshop

↓

Asset

↓

Evaluation

↓

Analytics

↓

Knowledge
```

Factory 的运行过程本质上是：

**利用静态能力。**

完成动态生产。

再把生产经验沉淀回静态知识。

形成持续进化闭环。

---

# 七、Factory Domains（核心领域）

Factory 按职责划分为五个领域：

## Production Domain（生产领域）

负责内容生产。

包括：

Project

Workflow

Task

Workshop

---

## Asset Domain（资产领域）

负责长期资产。

包括：

Character。

Location。

Prompt。

Template。

Asset。

---

## Knowledge Domain（知识领域）

负责知识积累。

包括：

Knowledge。

Rules。

Patterns。

Best Practices。

---

## Operation Domain（运营领域）

负责商业运营。

包括：

Publishing。

Analytics。

Revenue。

Account。

Channel。

---

## Infrastructure Domain（基础设施领域）

负责底层资源。

包括：

Provider。

Database。

Storage。

GPU。

Model。

Infrastructure 不属于业务。

而属于 Factory 的运行环境。

---

# 八、设计原则（Design Principles）

所有实体必须遵循以下原则。

## Business First（业务优先）

实体来源于业务。

不是数据库。

---

## Factory Ownership（Factory 拥有）

所有实体首先属于 Factory。

其次才属于某个 Project。

---

## Reusable（可复用）

长期资源必须能够跨 Project 复用。

---

## Stable（稳定）

Data Model 是长期稳定结构。

数据库可以变化。

实现可以变化。

Data Model 不应频繁变化。

---

## Model Agnostic（模型无关）

任何实体不得依赖某一个 AI Provider。

Factory 可以自由替换模型。

---

# 九、Persistence Mapping（持久化映射）

Persistence（持久化层）负责保存 Data Model。

当前实现：

SQLite。

未来：

PostgreSQL。

MySQL。

Cloud Database。

都必须遵循本模型。

数据库不是业务。

数据库只是 Data Model 的一种实现方式。

---

# 十、本章总结（Summary）

Data Model 定义了 AI Drama Factory 的世界。

Factory 世界由：

Static World（静态世界）

与

Dynamic World（动态世界）

共同组成。

Factory 通过：

静态能力。

驱动动态生产。

再将生产经验沉淀回静态知识。

形成持续学习与持续优化的闭环。

未来所有：

数据库。

API。

Kernel。

Centers。

Workshops。

ADF-OS。

都必须建立在本模型之上。

本章是整个 AI Drama Factory 最重要的基础设计之一。

---

**End**