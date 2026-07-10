
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

> **AI Drama Factory 应遵循什么样的统一编码规范？**

Coding Convention 定义整个项目的编码原则。

包括：

- 代码组织
- 模块设计
- 可维护性
- 可测试性
- AI 可读性
- 长期演进能力

本规范适用于整个 Factory。

---

# 二、设计目标（Purpose）

优秀代码不仅能够运行。

更应该：

- 易理解
- 易修改
- 易扩展
- 易测试
- 易 Review

代码首先是写给人看的。

其次才是给计算机执行。

---

# 三、核心原则（Core Principles）

Factory 遵循以下编码原则。

## Readability First（可读性优先）

任何代码。

都应优先保证可读性。

不要为了减少几行代码。

降低整体理解成本。

---

## Simplicity（简单优先）

优先选择：

最简单。

最容易理解。

最容易维护。

的实现方式。

避免过度设计。

---

## Single Responsibility（单一职责）

每个：

Class

Module

Function

只负责一个职责。

避免：

一个函数完成多个业务。

---

## Explicit（明确优于隐含）

代码应表达真实意图。

避免：

复杂隐式逻辑。

例如：

优先：

```
calculateScore()
```

而不是：

```
process()
```

---

## Consistency（一致性）

同一种问题。

采用统一解决方案。

避免：

多个模块。

多种编码风格。

---

# 四、模块设计（Module Design）

每个模块应满足：

- 职责单一
- 可独立测试
- 可独立替换
- 不依赖内部实现

模块之间通过接口通信。

避免直接引用内部对象。

---

# 五、函数设计（Function Design）

优秀函数应满足：

- 功能单一
- 参数明确
- 返回值明确
- 无副作用（能避免时尽量避免）

函数长度不是唯一标准。

但应避免承担多个职责。

---

# 六、类设计（Class Design）

类应代表：

一个明确概念。

例如：

```
ProjectService

DirectorWorkshop

AssetRepository
```

避免：

万能类。

例如：

```
Utils

CommonService

Helper
```

---

# 七、错误处理（Error Handling）

任何异常。

都必须：

- 明确捕获
- 明确记录
- 明确恢复策略

禁止：

```
catch {}

```

或者：

```
catch (e) {
    console.log(e)
}
```

后直接继续运行。

异常必须被正确处理。

---

# 八、日志规范（Logging）

日志应具有价值。

至少包含：

- 时间
- 模块
- Task
- Project
- Level
- Message

禁止：

大量无意义输出。

例如：

```
console.log("111")
```

---

# 九、配置管理（Configuration）

任何：

URL

Key

Magic Number

超时时间

路径

均不得硬编码。

统一放入配置中心。

代码只读取配置。

---

# 十、注释原则（Comments）

注释解释：

为什么。

而不是：

代码做了什么。

例如：

推荐：

```ts
// 为避免重复生成，对已完成项目直接跳过
```

不推荐：

```ts
// 创建一个数组
const arr = [];
```

代码本身已经表达了含义。

---

# 十一、代码复用（Reusability）

重复逻辑。

应抽象为：

- Function
- Module
- Component
- Adapter

禁止：

复制粘贴。

形成多个版本。

---

# 十二、可测试性（Testability）

所有业务逻辑。

应尽可能：

支持单元测试。

支持集成测试。

支持 Mock。

避免：

无法验证。

无法复现。

---

# 十三、AI Friendly（AI 可理解性）

AI Drama Factory 是 AI 原生项目。

因此代码应：

- 命名清晰
- 模块明确
- 注释规范
- 类型完整

方便：

AI 阅读。

AI 修改。

AI 自动生成。

---

# 十四、设计原则（Design Principles）

Factory 坚持：

## Clean Code

代码保持整洁。

---

## Maintainability

长期维护优先。

---

## Low Coupling

低耦合。

---

## High Cohesion

高内聚。

---

## Documentation Friendly

代码与文档保持一致。

---

## AI Friendly

方便 AI 理解。

---

# 十五、Non-Goals（非目标）

本章不负责：

- 命名规范（402）
- Git 工作流（404）
- Prompt 规范（407）
- 数据库规范（409）

---

# 十六、Dependencies（依赖关系）

Depends On：

- 302 Technical Architecture
- 401 Directory Convention
- 402 Naming Convention

Affects：

- 全部源码
- 全部 Workshop
- 全部 Adapter
- 全部 API

---

# 十七、本章总结

Coding Convention 定义了 AI Drama Factory 的统一编码方式。

Factory 不追求炫技。

不追求复杂设计。

而坚持：

**简单。**

**清晰。**

**长期可维护。**

未来。

任何开发人员。

任何 AI。

都应按照统一编码规范开发整个 Factory。

---

**End**