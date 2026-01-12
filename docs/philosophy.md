# Philosophy & Principles

## The Core Problem

AI coding assistants are incredibly powerful, but they have a fundamental limitation: **no persistent memory across sessions**.

Every conversation starts fresh. The AI doesn't know:
- What you worked on yesterday
- What's already been implemented
- What's currently broken
- What the priorities are
- What decisions were made and why

This creates friction:
- You spend the first 5-10 minutes of every session catching the AI up to speed
- Context gets lost between sessions
- Work gets repeated or forgotten
- Progress is hard to track
- You can't confidently leave the AI to work autonomously

## The Insight

**AI assistants excel at executing when given clear context, but struggle with maintaining state across sessions.**

The now-next methodology solves this by externalizing project state into a structured markdown file that both humans and AI can read, understand, and update.

## Why Markdown?

Markdown is perfect for this because:

1. **Human-readable** - You can quickly scan and understand project state
2. **AI-friendly** - LLMs are trained on markdown and parse it naturally
3. **Version-controlled** - Git tracks changes to NOW.md, creating an audit trail
4. **Universal** - Works with any AI tool, no dependencies or plugins
5. **Flexible** - Easy to customize for your needs

## Core Principles

### 1. Single Source of Truth

NOW.md is the definitive source for project state. Not in your head, not in Slack, not in comments—in NOW.md.

**Why this matters:**
- Eliminates ambiguity about what's happening
- Enables autonomous AI work without constant supervision
- Creates accountability (everything is documented)

### 2. Date-Stamped History

Every accomplishment is tagged with a date and structured with Purpose/What/Impact.

**Why this matters:**
- Shows real progress over time
- Enables pattern recognition (velocity, blockers, etc.)
- Creates a narrative of the project's evolution
- Helps with debugging ("when did this break?")

### 3. Autonomous Execution

The `/next` command makes decisions and implements without asking permission.

**Why this matters:**
- Reduces human-in-the-loop overhead
- Enables flow state (AI works while you sleep/focus elsewhere)
- Forces clear prioritization (AI needs to know what's most important)

### 4. Test Everything

Changes are validated before being committed and documented.

**Why this matters:**
- Prevents broken states from being recorded as "accomplished"
- Builds trust in autonomous execution
- Catches regressions early

### 5. Commit Atomically

Each `/next` iteration commits its changes with clear messages.

**Why this matters:**
- Creates rollback points if something breaks
- Provides audit trail aligned with NOW.md accomplishments
- Enables parallel work (branches can merge cleanly)

## The Workflow Loop

```
┌──────────────────────────────────────┐
│  NOW.md defines current state        │
└──────────────────────────────────────┘
              ↓
┌──────────────────────────────────────┐
│  AI reads state, chooses next work   │
└──────────────────────────────────────┘
              ↓
┌──────────────────────────────────────┐
│  AI implements and tests             │
└──────────────────────────────────────┘
              ↓
┌──────────────────────────────────────┐
│  AI updates NOW.md with outcome      │
└──────────────────────────────────────┘
              ↓
┌──────────────────────────────────────┐
│  AI commits changes                  │
└──────────────────────────────────────┘
              ↓
       (Loop back to top)
```

This creates a **self-reinforcing feedback loop**:
- Clear state → Good decisions → Successful work → Updated state → Better next decisions

## What Makes This Different

### vs. TODO.md / Task Lists
- **Now-Next:** Living document with context and history
- **TODO:** Static list, no context, no history

### vs. Git Commit Messages
- **Now-Next:** Strategic view of progress and priorities
- **Git:** Tactical view of individual changes

### vs. Project Management Tools
- **Now-Next:** Embedded in codebase, AI-readable, zero overhead
- **PM Tools:** External, human-only, require manual updates

### vs. Documentation
- **Now-Next:** Current state + recent history + next steps
- **Docs:** How things work, not what's happening now

## When This Works Best

✅ **Great for:**
- Solo development or small teams
- AI-assisted coding workflows
- Projects with clear, evolving goals
- Rapid iteration and experimentation
- Context-heavy work that's hard to remember

⚠️ **Less ideal for:**
- Large teams needing detailed coordination (use PM tools)
- Projects with complex dependencies across many repos
- Work that requires human decision-making at every step
- Compliance-heavy environments with strict process requirements

## Design Decisions

### Why "Recent Accomplishments" not "Full History"?
- Keeps NOW.md focused on current context
- Prevents file from growing unbounded
- Old accomplishments can be archived if needed
- Git history provides full detail anyway

### Why "Open Challenges" separated by Technical/Business?
- Different decision-makers (AI vs human)
- AI can solve technical challenges autonomously
- Business decisions require human judgment
- Clear separation prevents AI from overstepping

### Why "Next Steps" as ordered list?
- Forces prioritization (no "all equally important")
- AI knows exactly what to work on first
- Easy to reorder when priorities change
- Creates accountability (top item should get done)

### Why commit every iteration?
- Creates rollback points
- Prevents losing work if something goes wrong
- Aligns git history with NOW.md narrative
- Enables branching and parallel work

## The Meta-Principle

**The methodology should be simpler than the work it enables.**

If maintaining NOW.md takes more effort than the value it provides, you're doing it wrong. The system should feel effortless:

- `/next` should "just work" most of the time
- NOW.md should stay current without manual effort
- You should rarely think about the methodology itself

When this works well, you'll barely notice it. You'll just notice that your AI assistant seems smarter, more reliable, and more autonomous than before.

## Evolution Over Time

This methodology emerged from real frustration and evolved through usage:

1. **Problem:** AI kept losing context between sessions
2. **First attempt:** Manually wrote status updates in comments
3. **Improvement:** Structured as NOW.md with sections
4. **Breakthrough:** Created `/next` command to automate the loop
5. **Refinement:** Added date-stamping, impact tracking, commit hashes
6. **Current:** Battle-tested across multiple real projects

It will continue evolving. Your contributions and adaptations will shape what comes next.

---

**The goal isn't perfect process—it's shipping working code faster with less friction.**

If NOW.md helps you do that, use it. If it doesn't, don't.
