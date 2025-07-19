# 🚀 Claude Code Assistant

## 🖥️ Environment: Claude Code CLI
**Important:** This project uses Claude Code CLI in the terminal (Warp), NOT the Claude Desktop app.  
All commands and automation are designed for CLI usage. Desktop-specific features are optional.

## 1. 🎯 QUICK START

### System Status Display
```
=== 🚀 Claude Code System Status ===
[🧠 Memory] Graphiti: ✅ Active | [X] memories stored
[📚 Knowledge] facts.json ✅ | patterns.json ✅ | constraints.json ✅  
[🤖 MCPs] Sequential Thinking ✅ | Graphiti ✅ | Gemini ✅ | GitHub ✅ | n8n ✅
[🎯 Mode] Auto Mode 🚀 | Project: anobel.nl | Git: main
[📝 Todos] [X] active tasks | [📂 Session] [name] | Age: [X]h
=====================================
```

### Essential Commands (Just 3!)
```bash
/memory [search|manual|auto]  # Knowledge management
/save [new|list|search|stats] # Session management  
/logic [help|hooks|emergency] # System control & help

# Everything else runs automatically via hooks!
```

**Get detailed help:** `/logic help [topic]`  
**See what's automated:** `/logic hooks status`

---

## 2. 🛠️ CORE PRINCIPLES

### Development Philosophy
1. **Elite JavaScript & CSS specialist** - Fix root causes, not symptoms
2. **Production-grade code** - DRY, KISS, secure, performant
3. **Webflow enhancement** - Work with platform, never against it
4. **Full ownership** - Complete solutions, not patches

### Technical Constraints
| Category | ❌ Never | ✅ Always |
|----------|----------|-----------|
| **DOM** | Modify structure | Use existing elements |
| **CSS** | Pixels | REM units + data attributes |
| **JS** | console.log, globals | Namespaces, element checks |
| **Files** | >500 lines | Module pattern |

**Platform Limits:** JS <50KB | CSS <20KB | Load <3s | Assets 30MB/file

---

## 3. 📋 TASK MANAGEMENT

### Task Lifecycle
Tasks automatically flow through stages:
```
/to-do → /active → /completed → /z__archive (after 30 days)
```

### Before System Changes
**IMPORTANT:** Create a spec folder before any major system changes:
```
.claude/project/tasks/specs/
└── [feature-name]/
    ├── requirements.md     # What needs to be done
    ├── design.md          # How it will be implemented
    ├── test-plan.md       # How to verify it works
    └── rollback-plan.md   # How to undo if needed
```

### Task Commands
- Tasks are managed automatically via TodoWrite integration
- Active task limit: 1 (enforced by system)
- Progress tracked in real-time
- Completion suggestions when all todos done

---

## 4. 🤖 AUTOMATION & HOOKS

### What Runs Automatically
| Old Command | Triggers | Manual Override |
|-------------|----------|-----------------|
| `/workflow` | Complex tasks (3+ steps) | Sequential Thinking tool |
| `/test` | 3+ files changed | Run tests manually |
| `/security` | Sensitive patterns | `/logic emergency` |
| `/notebook` | Session saves | `/logic notebook` |
| `/mode` | Task complexity | Respond to suggestions |

### Memory Automation Levels
```bash
/memory auto off     # No automation
/memory auto manual  # Explicit capture only
/memory auto semi    # Critical auto, others prompt (default)
/memory auto full    # Capture everything
```

**Patterns captured:** DECISION, SECURITY, BREAKING, RESOLVED, PATTERN, client preferences, API limits

---

## 5. 📂 PROJECT STRUCTURE

```
.claude/
├── docs/                   # All documentation
│   ├── logic/             # Logic system docs
│   ├── graphiti/          # Memory system docs
│   ├── technical/         # Implementation details
│   └── mcp/               # MCP server docs
├── logic/                  # Hooks and automation
│   ├── session/           # Session management
│   ├── memory/            # Memory context
│   ├── tasks/             # Task lifecycle
│   └── quality/           # Code quality
├── project/
│   ├── knowledge/         # facts.json, patterns.json, constraints.json
│   ├── sessions/          # Work history
│   ├── tasks/             # Task organization
│   │   ├── to-do/        # Pending tasks
│   │   ├── active/       # Current task (max 1)
│   │   ├── completed/    # Finished tasks
│   │   └── z__archive/   # Old tasks (excluded)
│   └── state/             # System state
└── settings.json          # Configuration
```

### Key Files
- **facts.json** - Project requirements, client preferences
- **patterns.json** - Code conventions, established patterns
- **constraints.json** - Technical limits, platform rules
- **settings.json** - Hook configuration, automation levels

---

## 6. 🆘 HELP & TROUBLESHOOTING

### Get Help
```bash
/logic help              # List all help topics
/logic help automation   # How automation works
/logic help hooks        # Understanding hooks
/logic help migration    # Migrate from old commands
/logic help troubleshooting  # Fix common issues
```

### Quick Fixes
- **Hooks not running?** `/logic hooks status`
- **Too much automation?** `/memory auto manual`
- **Emergency disable:** `/logic emergency disable`
- **Session issues?** `/save new recovery-session`

### Production Checklist
- [ ] No console.log statements
- [ ] No hardcoded API keys  
- [ ] All tests passing
- [ ] Performance budgets met
- [ ] Security scan clean

---

**Remember:** Focus on coding, not commands. The system handles the rest! 🚀