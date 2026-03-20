**[English](README.md)**

# CCBuddy 设计文档

**CCBuddy** 的设计文档 — 一个基于 TypeScript 的 monorepo 项目，将 Claude Code SDK/CLI 封装为一个常驻运行的个人 AI 助手，支持定时任务、多平台消息、记忆系统和可扩展技能。

## 仓库结构

```
├── plans/          # 实现计划（分步骤的构建指南）
├── specs/          # 设计规格（架构、API、配置模式）
```

### Plans（实现计划）

实现计划将每个功能拆分为有序的任务块，包含文件级别的详细指引。适用于 AI 编程助手或开发者按顺序执行。

| 文件 | 说明 |
|------|------|
| `plan1-core-agent.md` | 核心 monorepo 基础：共享类型、配置系统、事件总线、Agent 模块、编排器 |
| `plan2-skills.md` | 技能系统：加载器、注册表、执行引擎 |
| `plan3-memory.md` | 记忆模块：基于 SQLite 的存储、检索和上下文注入 |
| `plan4-gateway-platforms.md` | 网关和平台适配器（iMessage、Telegram 等） |
| `plan5-scheduler.md` | 定时任务、心跳监控、Webhook 接入 |
| `plan6-self-evolving-skills.md` | 可自主创建和优化其他技能的自进化技能 |
| `apple-calendar.md` | 通过 EventKit/AppleScript 集成 Apple 日历 |
| `media-handling.md` | 图片、文件和媒体附件处理 |
| `memory-consolidation-backup.md` | 记忆压缩、去重和备份 |
| `morning-briefings.md` | 定时早间简报推送 |
| `session-conflict-detection.md` | 并发会话冲突检测与解决 |
| `voice-messages.md` | 基于 OpenAI Whisper/TTS 的双向语音消息 |

### Specs（设计规格）

设计规格定义了每个功能的架构、数据模型、配置模式和 API 契约。实现计划会引用对应的设计规格。

| 文件 | 说明 |
|------|------|
| **`ccbuddy-design.md`** | **主设计规格 — 整体系统架构、模块划分和配置模式** |
| `scheduler-design.md` | 调度系统：定时任务、心跳监控、Webhook、主动推送 |
| `self-evolving-skills-design.md` | 自进化技能的创建和优化流程 |
| `apple-calendar-design.md` | Apple 日历读写集成 |
| `evening-briefing-design.md` | 晚间简报内容与推送 |
| `media-handling-design.md` | 媒体处理流水线与存储 |
| `memory-consolidation-backup-design.md` | 记忆生命周期管理 |
| `morning-briefings-design.md` | 早间简报聚合与格式化 |
| `session-conflict-detection-design.md` | 多会话冲突解决策略 |
| `voice-messages-design.md` | 语音消息的转录与合成 |
