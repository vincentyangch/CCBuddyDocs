# CCBuddy Design Docs

Design documents for **CCBuddy** — a TypeScript monorepo that wraps the Claude Code SDK/CLI into an always-on personal AI agent with scheduled tasks, multi-platform messaging, memory, and extensible skills.

## Repository Structure

```
├── plans/          # Implementation plans (step-by-step build guides)
├── specs/          # Design specs (architecture, APIs, config schemas)
```

### Plans

Implementation plans break each feature into ordered chunks and tasks with file-level instructions. They are intended to be executed sequentially by an agentic coding assistant or a developer.

| File | Description |
|------|-------------|
| `plan1-core-agent.md` | Core monorepo foundation: shared types, config, event bus, agent module, orchestrator |
| `plan2-skills.md` | Skill system: loader, registry, execution engine |
| `plan3-memory.md` | Memory module: SQLite-backed storage, retrieval, context injection |
| `plan4-gateway-platforms.md` | Gateway and platform adapters (iMessage, Telegram, etc.) |
| `plan5-scheduler.md` | Cron jobs, heartbeat monitoring, webhook ingestion |
| `plan6-self-evolving-skills.md` | Skills that can create and refine other skills autonomously |
| `apple-calendar.md` | Apple Calendar integration via EventKit/AppleScript |
| `media-handling.md` | Image, file, and media attachment processing |
| `memory-consolidation-backup.md` | Memory compaction, deduplication, and backup |
| `morning-briefings.md` | Scheduled morning briefing delivery |
| `session-conflict-detection.md` | Detecting and resolving concurrent session conflicts |
| `voice-messages.md` | Bidirectional voice messages via OpenAI Whisper/TTS |

### Specs

Design specs define the architecture, data models, config schemas, and API contracts for each feature. Plans reference their corresponding spec.

| File | Description |
|------|-------------|
| `scheduler-design.md` | Scheduler system: cron, heartbeat, webhooks, proactive delivery |
| `self-evolving-skills-design.md` | Self-evolving skill creation and refinement pipeline |
| `apple-calendar-design.md` | Apple Calendar read/write integration |
| `evening-briefing-design.md` | Evening briefing content and delivery |
| `media-handling-design.md` | Media processing pipeline and storage |
| `memory-consolidation-backup-design.md` | Memory lifecycle management |
| `morning-briefings-design.md` | Morning briefing aggregation and formatting |
| `session-conflict-detection-design.md` | Multi-session conflict resolution strategy |
| `voice-messages-design.md` | Voice message transcription and synthesis |
