# Why This Works

## The Problem

AI assistants have no memory across sessions. Every conversation starts fresh.

You waste time:
- Explaining what you were working on
- Catching the AI up to speed
- Remembering what's done vs what's next

## The Solution

Externalize project state into a markdown file (`NOW.md`) that both you and the AI can read.

## Why Markdown?

- **Human-readable** - You can scan it quickly
- **AI-friendly** - LLMs parse it naturally
- **Version-controlled** - Git tracks changes
- **Universal** - Works with any AI tool
- **Simple** - No dependencies, no tools

## Core Insight

AI assistants are great at executing when given clear context. They just can't maintain state between sessions.

NOW.md provides that missing context layer.

## How It Works

```
NOW.md defines current state
        ↓
AI reads it, picks next work
        ↓
AI implements and tests
        ↓
AI updates NOW.md
        ↓
AI commits changes
        ↓
(Loop repeats)
```

Each iteration builds on the last. State is never lost.

## When This Works Best

✅ **Great for:**
- Solo development
- Rapid iteration
- AI-assisted workflows
- Projects with evolving goals

⚠️ **Less ideal for:**
- Large teams needing PM tools
- Compliance-heavy processes
- Work requiring constant human decisions

## Key Principles

1. **Single source of truth** - NOW.md is definitive
2. **Date-stamped history** - Track progress over time
3. **Autonomous execution** - AI makes decisions and implements
4. **Test everything** - Validate before committing
5. **Commit atomically** - Each iteration creates a rollback point

## The Meta-Principle

**The methodology should be simpler than the work it enables.**

If maintaining NOW.md takes more effort than the value it provides, something's wrong.

When it works well, you barely notice it. You just notice your AI seems smarter and more reliable.

---

That's the whole philosophy. Nothing fancy, just a simple pattern that works.
