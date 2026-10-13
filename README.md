# 电商系统 MFQ 测试计划

本提交严格按 **M（Models）- F（Functional）- Q（Quality）** 结构组织，并包含库存同步一致性专章、异常处理与补偿策略、发布准入/准出标准。

## 文件说明

- [mfq-mindmap.md](mfq-mindmap.md)：MFQ 分层思维导图，可直接导入 XMind。
- [test-cases.md](test-cases.md)：按模块组织的测试用例（编号、优先级、前置条件、步骤、预期结果），含关键 API 字段与错误码表、用例到模型的追溯。
- [strategy-note.md](strategy-note.md)：一页测试策略，说明优先级、设计取舍与准入/准出。

## 与题目要求的对应关系

| 题目要求 | 位置 |
|---|---|
| M：端到端流程、订单状态机、库存状态、外部交互、一致性边界 | mindmap M-1 ~ M-5 |
| F：核心正向流程 | mindmap F-2；test-cases 第 2 节 |
| F：库存同步（预占/扣减/取消恢复/幂等/乱序） | mindmap F-4；test-cases 第 4 节 |
| F：边界场景（零库存/秒杀/拆单/退货恢复） | mindmap F-5；test-cases 第 5 节 |
| F：关键 API（字段、错误码、回写字段） | mindmap F-6；test-cases 第 6 节 |
| Q：性能、可靠性、可观测性、安全性、可恢复性 | mindmap Q-1 ~ Q-5；test-cases 第 7 节 |
| 库存同步一致性专章 | mindmap F-4；test-cases 第 4 节 |
| 异常处理与补偿策略 | mindmap M-6、Q-2 |
| 发布准入/准出标准 | mindmap Q-6；strategy-note |

> 说明：性能、告警阈值、卡单时长和错误码均为假设定义，实际项目应在评审时结合生产基线与接口规范确认。
