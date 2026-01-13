# Now-Next Methodology

**Context-aware development workflow for AI coding assistants**

Never lose track of what your AI assistant was working on. The now-next methodology provides systematic state management for AI pair programming through a simple `NOW.md` file and `/next` command.

---

## 🚀 Quick Start

**Copy this prompt to your AI coding assistant (Claude Code, OpenCode, Cursor, etc.):**

```
Set up the now-next methodology in this project:

1. Create a NOW.md file to track project state with these sections:
   - Recent Accomplishments (date-stamped with Purpose/What Was Done/Impact/Commits)
   - Current Status
   - Open Challenges (Technical & Business/Product)
   - Next Steps
   - Quick Reference table

2. Create a local /next command (in .claude/commands/ or .config/opencode/commands/) that:
   - Reads NOW.md and project context files
   - Analyzes what to work on next based on current state
   - Implements the chosen work autonomously with testing
   - Updates NOW.md with accomplishments and new state
   - Commits all changes
   - Reports any user actions needed (API keys, etc.)

3. Initialize git if needed, then commit the setup

Use this template for NOW.md: https://github.com/soutone/now-next-methodology/blob/main/templates/NOW.md
Use this template for /next: https://github.com/soutone/now-next-methodology/blob/main/templates/next.md
```

That's it! After setup, just run `/next` whenever you want your AI to continue development.

---

## 💡 What Problem Does This Solve?

When working with AI coding assistants across multiple sessions, you often face:

- ❌ **Lost context** - "What were we working on last time?"
- ❌ **Unclear progress** - "What actually got done?"
- ❌ **Manual tracking** - Keeping notes in your head or separate docs
- ❌ **Interrupted flow** - Spending time catching the AI up to speed

The now-next methodology solves this with:

- ✅ **Persistent state** - NOW.md captures current project status
- ✅ **Clear history** - Date-stamped accomplishments with impact
- ✅ **Autonomous iterations** - `/next` command drives development forward
- ✅ **Instant resume** - Start each session where you left off

---

## 📖 How It Works

### The NOW.md File

A structured markdown file that tracks:

```markdown
# Project Name

## Recent Accomplishments
### 2026-01-12 - Implemented User Authentication
**Purpose:** Secure user accounts with JWT
**What Was Done:**
- Added bcrypt password hashing
- Created JWT middleware
- Built login/register endpoints
**Impact:**
- Users can now securely sign up and log in
- Foundation for role-based access control
**Commits:** abc123f, def456a

## Current Status
Authentication system working. Ready for role management.

## Open Challenges
### Technical
- Need to implement refresh token rotation
### Business/Product
- Decide on user roles and permissions structure

## Next Steps
1. Implement refresh token mechanism
2. Add role-based access control
3. Create admin dashboard

## Quick Reference
| Command | Purpose |
|---------|---------|
| `/next` | Continue development |
| `npm test` | Run test suite |
```

### The /next Command

A local slash command that:

1. **Reads** NOW.md and project context
2. **Analyzes** what's most impactful to work on next
3. **Implements** the chosen work with testing
4. **Updates** NOW.md with new accomplishments
5. **Commits** all changes
6. **Reports** what was done and any user actions needed

---

## 🎯 Real-World Examples

**Projects built using this methodology:**
- **[Documatic](https://documatic.fly.dev)** - AI documentation tool with autonomous feature development
- **[Credible](https://credible.fly.dev)** - Credential verification platform
- **[MailCheck](https://mailcheck-api.fly.dev)** - Email validation service
- And several others...

**Results across projects:**
- Multiple autonomous development sessions
- Clear progression from MVP to production-ready applications
- `/next` maintains context perfectly across sessions
- Used successfully for: AI documentation tools, verification platforms, validation services, APIs

---

## 🛠️ Installation

### Option 1: One-Prompt Setup (Recommended)
Use the prompt from [Quick Start](#-quick-start) above.

### Option 2: Global Commands (Reusable)

Install a global `/setup-now-next` command once, use in any project:

#### For Claude Code:
```bash
curl -o ~/.claude/commands/setup-now-next.md https://raw.githubusercontent.com/soutone/now-next-methodology/main/templates/claude-code/setup-now-next.md
```

#### For OpenCode:
```bash
curl -o ~/.config/opencode/commands/setup-now-next.md https://raw.githubusercontent.com/soutone/now-next-methodology/main/templates/opencode/setup-now-next.md
```

Then in any project directory:
```
/setup-now-next
```

### Option 3: Manual Setup

Download templates directly to your project:

```bash
# Download templates
mkdir -p .claude/commands
curl -o NOW.md https://raw.githubusercontent.com/soutone/now-next-methodology/main/templates/NOW.md
curl -o .claude/commands/next.md https://raw.githubusercontent.com/soutone/now-next-methodology/main/templates/next.md

# Edit NOW.md to fill in your project details
# Then commit: git add NOW.md .claude/commands/next.md && git commit -m "Add now-next methodology"
```

#### For OpenCode:
```bash
# Download templates  
mkdir -p .config/opencode/commands
curl -o NOW.md https://raw.githubusercontent.com/soutone/now-next-methodology/main/templates/NOW.md
curl -o .config/opencode/commands/next.md https://raw.githubusercontent.com/soutone/now-next-methodology/main/templates/next.md

# Edit NOW.md to fill in your project details
# Then commit: git add NOW.md .config/opencode/commands/next.md && git commit -m "Add now-next methodology"
```

---

## 📚 Documentation

- [Getting Started Guide](./docs/getting-started.md) - Detailed walkthrough
- [Philosophy & Principles](./docs/philosophy.md) - Why this works
- [Customization Guide](./docs/customization.md) - Adapt to your workflow

---

## 🤝 Contributing

Contributions are welcome! See [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines.

**Ideas for contributions:**
- Templates for specific tech stacks (Python/Django, React/Next.js, etc.)
- Integrations with other AI coding tools
- Example projects showcasing the methodology
- Documentation improvements

---

## 📄 License

MIT License - see [LICENSE](./LICENSE) for details.

---

## 🌟 Why This Works

The now-next methodology succeeds because it:

1. **Matches AI capabilities** - Structured state is perfect for LLM consumption
2. **Reduces cognitive load** - Both human and AI know exactly where things stand
3. **Enables autonomy** - Clear state → AI can make good decisions independently
4. **Creates accountability** - Date-stamped accomplishments show real progress
5. **Stays simple** - Just markdown files, no tools or dependencies

**Core insight:** AI assistants are excellent at executing when given clear context, but struggle with remembering state across sessions. NOW.md provides that missing context layer.

---

## 🔗 Links

- [GitHub Repository](https://github.com/soutone/now-next-methodology)
- [Issue Tracker](https://github.com/soutone/now-next-methodology/issues)
- [Discussions](https://github.com/soutone/now-next-methodology/discussions)

---

**Built by developers frustrated with context loss in AI coding sessions.**

*If this methodology helps you, consider ⭐ starring the repo and sharing it with others!*
