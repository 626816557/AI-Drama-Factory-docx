

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

> **AI Drama Factory 应如何统一接入 ComfyUI，并将其作为 Factory 的图像生成能力提供者（Image Capability Provider）？**

ComfyUI Adapter（ComfyUI 适配器）。

负责统一管理：

Factory 与 ComfyUI 之间的能力集成。

包括：

- Workflow
- Image Generation
- LoRA
- ControlNet
- IPAdapter
- Upscale
- Inpainting
- Custom Nodes

ComfyUI。

属于：

Factory Image Capability Layer。

而不是：

Factory 本身。

---

# 二、ComfyUI Adapter 定位（Position）

ComfyUI Adapter。

不是：

ComfyUI Launcher。

也不是：

Workflow 编辑器。

ComfyUI Adapter。

是整个 Factory 的 Image Capability Adapter。

负责：

统一接入。

统一调用。

统一管理。

全部 ComfyUI 图像能力。

---

# 三、设计目标（Purpose）

ComfyUI Adapter 的目标不是：

执行某一个 Workflow。

而是：

建立统一。

稳定。

可扩展。

可维护。

的 Image Capability Integration Layer。

让 Factory。

能够灵活调用：

不同 Workflow。

不同模型。

不同节点。

而无需修改业务逻辑。

---

# 四、输入（Input）

ComfyUI Adapter 输入：

- Capability Request
- Workflow Template
- Prompt
- Reference Assets
- Parameters
- Model Configuration

统一称为：

Image Request。

---

# 五、输出（Output）

ComfyUI Adapter 输出：

Image Response。

包括：

- Generated Assets
- Metadata
- Workflow Information
- Generation Time
- Resource Usage
- Status

所有结果。

统一转换为：

Factory Standard Response。

---

# 六、核心职责（Responsibilities）

ComfyUI Adapter 负责：

## Workflow Translation

将 Factory Request。

转换为：

ComfyUI Workflow。

---

## Workflow Execution

统一执行：

ComfyUI Workflow。

---

## Resource Management

统一管理：

Checkpoint。

LoRA。

ControlNet。

IPAdapter。

Custom Nodes。

---

## Response Normalization

统一返回：

Factory Response。

避免业务依赖：

ComfyUI 返回格式。

---

## Error Handling

统一处理：

- Workflow Error
- Missing Node
- Missing Model
- Timeout
- GPU Failure
- Invalid Workflow

统一错误格式。

统一恢复策略。

---

# 七、标准流程（Workflow）

Factory 推荐统一流程：

Receive Image Request

↓

Select Workflow

↓

Prepare Resources

↓

Execute Workflow

↓

Generate Assets

↓

Normalize Response

↓

Return Factory Response

---

# 八、设计原则（Design Principles）

Factory 坚持：

## Workflow Independent

Workflow 可自由替换。

---

## Provider Independent

ComfyUI。

只是 Image Provider。

---

## Asset Driven

围绕：

Factory Assets。

组织图像生成。

---

## Unified Interface

统一接口。

---

## Extensible

支持未来：

Custom Nodes。

新模型。

新 Workflow。

持续扩展。

---

# 九、Non-Goals（非目标）

本章不负责：

- Prompt Design
- Story Logic
- Character Design
- Asset Management

这些能力。

将在其它章节定义。

---

# 十、Dependencies（依赖关系）

Depends On：

- 800 Model Adapter
- 703 Asset Center
- 708 Model Center

Affects：

- 604 Asset Generation Workshop
- 903 Asset Database

ComfyUI Adapter。

负责 Factory 的 ComfyUI 图像能力接入。

---

# 十一、本章总结

ComfyUI Adapter。

不是：

ComfyUI 软件。

也不是：

Workflow 编辑器。

它负责：

统一接入。

统一调度。

统一管理。

ComfyUI 全部图像生成能力。

确保 Factory。

能够持续利用 ComfyUI 的生态能力。

同时保持整个业务系统与具体 Workflow 解耦。

---

**End**