

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

> **AI Drama Factory 如何支持本地开发、云端部署和未来企业级扩展？**

Cloud Architecture 定义 Factory 的部署形态。

它关注：

- 系统如何部署
- 服务如何扩展
- AI 如何分布式运行
- 数据如何共享
- 如何从单机平滑演进到云端

本章不涉及具体云厂商。

Factory 不绑定任何云平台。

---

# 二、架构目标（Purpose）

AI Drama Factory 的云架构应满足以下目标：

- 本地开发简单
- 云端部署方便
- 支持水平扩展
- 支持 GPU Worker
- 支持对象存储
- 支持企业部署
- 支持 SaaS 化

同一套系统。

应能够运行在：

- 本地电脑
- 云服务器
- 企业私有云
- 公有云

---

# 三、部署模式（Deployment Modes）

Factory 支持四种部署模式。

## Local Mode（本地模式）

适用于：

开发。

调试。

个人创作。

特点：

- 单机运行
- 本地数据库
- 本地文件存储
- 本地 AI API

这是 V1 的默认模式。

---

## Studio Mode（工作室模式）

适用于：

小团队。

共享资源。

特点：

- 多人协作
- 共享数据库
- 共享素材
- 统一 Dashboard

支持多个创作者共同生产内容。

---

## Enterprise Mode（企业模式）

适用于：

公司级部署。

特点：

- 权限管理
- 多团队
- 多项目
- GPU 集群
- 企业知识库
- 企业监控

满足企业级内容生产需求。

---

## SaaS Mode（云平台模式）

适用于：

AI Drama Factory 平台化运营。

特点：

- 多租户
- 在线使用
- 自动扩容
- 在线计费
- API 开放

未来支持全球用户。

---

# 四、系统部署结构

推荐部署结构如下：

```
Browser
    │
    ▼
ADF-OS
    │
    ▼
Backend API
    │
    ▼
Core System
    │
    ├─────────────┐
    ▼             ▼
Workshops     AI Infrastructure
    │             │
    └──────┬──────┘
           ▼
Data Center
```

所有服务保持独立。

通过标准接口通信。

---

# 五、计算资源（Compute）

Factory 将计算资源划分为：

- CPU Worker
- GPU Worker

CPU Worker：

负责：

调度。

分析。

管理。

日志。

数据库。

GPU Worker：

负责：

图片。

视频。

模型推理。

GPU Worker 可以独立扩容。

无需影响其他模块。

---

# 六、存储架构（Storage）

Factory 不依赖本地磁盘。

所有存储统一抽象。

包括：

- Local Storage
- Object Storage
- Backup Storage
- Archive Storage

未来可根据部署环境选择具体实现。

例如：

本地文件系统。

MinIO。

云对象存储。

---

# 七、网络通信（Networking）

所有模块统一通过：

HTTP API。

WebSocket。

事件总线。

进行通信。

避免模块之间直接访问内部实现。

保证系统可扩展。

---

# 八、容器化（Containerization）

Factory 推荐：

所有服务支持容器化部署。

例如：

- Frontend
- Backend
- Worker
- Database
- Redis
- Object Storage

容器化保证：

开发环境。

测试环境。

生产环境。

保持一致。

---

# 九、监控（Monitoring）

云架构应支持统一监控。

包括：

- CPU
- GPU
- 内存
- 网络
- AI 调用
- API 响应
- Workshop 状态

所有状态最终汇聚至：

ADF-OS Dashboard。

---

# 十、扩展策略（Scalability）

Factory 支持：

水平扩展。

例如：

增加：

- Director Worker
- Renderer Worker
- Video Worker

无需修改系统架构。

新增节点即可参与生产。

---

# 十一、设计原则（Design Principles）

AI Drama Factory 云架构遵循：

## Cloud Ready

默认支持未来云部署。

---

## Local First

V1 优先保证本地可运行。

---

## Stateless

Worker 默认无状态。

方便扩容。

---

## Storage Decoupling

计算与存储分离。

---

## Elastic Scaling

计算能力按需扩展。

---

## Vendor Neutral

不绑定任何云厂商。

保持长期自主可控。

---

# 十二、未来演进（Future Evolution）

未来支持：

- Kubernetes
- 多地区部署
- 全球 CDN
- GPU 调度
- Serverless Worker
- 自动扩容
- 企业集群
- 全球 SaaS

当前阶段：

保持简单。

预留扩展能力。

---

# 十三、Development Mapping（开发映射）

对应未来目录：

```
docker/

deploy/

workers/

storage/

monitor/

gateway/

configs/
```

所有部署相关能力。

均应遵循本章设计。

---

# 十四、本章总结

Cloud Architecture 定义 AI Drama Factory 的部署能力。

Factory 不因部署环境不同而改变系统架构。

坚持：

**一次设计，多种部署。**

无论运行在个人电脑、工作室还是企业云端。

都应保持统一的软件架构。

---

**End**