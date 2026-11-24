# Current Tasks

本文档记录当前由主 Agent 管理的正式开发任务。

主 Agent 是唯一维护者。Worker 的内部子任务、执行过程和临时分工不记录在此文件中。

---

## 20261123-1430-000 - [Task Name]

- **Status:** READY
- **Priority:** HIGH
- **Requirements:**
  - FR-001
  - FR-002
- **Dependencies:** None

**Description:**

简要说明任务的开发目标和预期交付结果。

---

## 20261123-1430-001 - [Task Name]

- **Status:** WAITING
- **Priority:** MEDIUM
- **Requirements:**
  - FR-003
- **Dependencies:**
  - 20261123-1430-000

**Waiting Reason:**

说明当前任务为什么需要等待，以及恢复执行所需要满足的条件。

**Description:**

简要说明任务的开发目标。

---

# Task Management Rules

## Task Identifiers

使用格式：

`YYYYMMDD-HHmm-NNN`

同一项目由主 Agent 统一分配任务编号。

同一创建批次从 `000` 开始递增。不同批次允许重新编号。

历史记录使用完整任务编号和任务名称，避免编号复用造成混淆。

## Task Status

- READY: 已具备执行条件，等待安排。
- WORKING: 正在执行。
- WAITING: 等待依赖、用户确认、外部条件或问题处理。
- FINISH: 已由主 Agent 完成验收，等待移除。

WAITING 必须填写等待原因。

FINISH 不长期保留。完成必要验收和记录后，从当前任务清单移除。

## Priority

- HIGH: 重要、紧急或阻塞其他工作的任务。
- MEDIUM: 正常开发任务。
- LOW: 非紧急优化或可延后工作。

优先级由主 Agent 根据项目目标、任务依赖和风险判断。

## Task Completion

主 Agent 根据实际代码、测试结果、必要的 PR 审查和集成验证判断任务是否完成。

Worker 的完成报告或 PR Approved 不代表正式任务已经完成。

用户尚未授权合并时，任务保持 WAITING。

完成验收后，移除对应任务。

重要开发记录按需保存到 `dev/records/`，不重要的任务不要求创建独立报告。

## Task Scope

- 只记录主 Agent 管理的正式开发任务。
- 不记录 Worker 的内部子任务和分配情况。
- 不强制填写独立的验收标准。
- 功能任务应关联 requirements.md 中的需求编号。
- 工程维护任务可以没有 FR 编号，但必须具有明确的工程目标。
- 只保留当前未完成的正式任务。

## Dependency Management

Dependencies 只记录正式任务之间真实存在的前置关系。

没有前置依赖时填写 `None`。

任务完成并移除后，主 Agent 应重新检查相关下游任务的依赖条件，并更新其状态。