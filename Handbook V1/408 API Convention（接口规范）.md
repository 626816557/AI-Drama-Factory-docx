
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

> **AI Drama Factory 应如何设计统一、稳定、可扩展的 API？**

API Convention 定义整个系统的接口规范。

包括：

- REST API
- Internal API
- Workshop API
- AI Adapter API

统一接口。

是整个 Factory 解耦的重要基础。

---

# 二、设计目标（Purpose）

优秀 API 应满足：

- 简单
- 一致
- 稳定
- 可扩展
- 可测试
- 可维护

API 是系统之间沟通的契约。

而不是实现细节。

---

# 三、核心原则（Core Principles）

Factory 坚持：

## API First

模块之间。

优先定义接口。

再实现功能。

---

## Contract First

接口一旦发布。

即成为契约。

任何修改。

都应保证兼容性。

---

## Resource Oriented

API 应围绕资源设计。

而不是围绕动作设计。

例如：

```
/projects

/workshops

/assets

/videos
```

避免：

```
/createProject

/getVideo

/runWorkshop
```

---

## Stateless

API 默认无状态。

请求应包含完成当前操作所需信息。

避免依赖服务器会话状态。

---

# 四、API 分类（API Categories）

Factory 定义四类 API。

## Public API

提供给：

ADF-OS。

CLI。

未来开放平台。

---

## Internal API

系统内部模块通信。

例如：

Core System。

Workshop。

Data Center。

---

## Adapter API

统一访问：

LLM。

图片。

视频。

TTS。

ASR。

第三方能力。

---

## Event API

用于事件驱动通信。

例如：

ProjectCreated。

WorkshopCompleted。

VideoGenerated。

---

# 五、统一响应格式（Response）

所有 API 建议保持统一响应结构。

```
{
    success,
    code,
    message,
    data,
    timestamp
}
```

保持一致。

方便：

前端。

日志。

调试。

---

# 六、错误规范（Error Handling）

错误响应应包含：

- 错误码
- 错误信息
- 可恢复建议（如适用）

禁止：

直接暴露：

数据库错误。

系统堆栈。

第三方异常。

---

# 七、版本管理（Versioning）

API 应支持版本。

例如：

```
/api/v1

/api/v2
```

重大升级。

不得直接破坏旧接口。

---

# 八、接口设计原则（API Design）

接口应满足：

- 单一职责
- 输入明确
- 输出稳定
- 易于测试
- 易于 Mock

避免：

一个接口完成多个业务。

---

# 九、安全要求（Security）

所有 API 应支持：

- 身份认证
- 权限验证
- 参数校验
- 请求日志
- 限流（未来支持）

任何公开接口。

都必须经过统一安全检查。

---

# 十、文档要求（Documentation）

所有 API。

均应拥有：

- 功能说明
- 输入参数
- 输出参数
- 示例
- 错误码

API 文档应与代码同步维护。

---

# 十一、设计原则（Design Principles）

Factory 坚持：

## Stable Contract

接口稳定。

---

## Backward Compatibility

保持兼容。

---

## Explicit Input

输入明确。

---

## Explicit Output

输出明确。

---

## Documentation Driven

接口文档先于实现。

---

# 十二、Non-Goals（非目标）

本章不负责：

- 数据库设计（409）
- SDK 实现
- HTTP 框架选型

---

# 十三、Dependencies（依赖关系）

Depends On：

- 302 Technical Architecture
- 305 Security Architecture

Affects：

- Backend
- Frontend
- Workshop
- AI Adapter
- ADF-OS

---

# 十四、本章总结

API Convention 定义了 AI Drama Factory 的统一通信规范。

接口不是代码细节。

而是模块之间的长期契约。

未来。

任何系统通信。

都应遵循统一 API 规范。

---

**End**