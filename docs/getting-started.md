# Getting Started with Now-Next Methodology

This guide will walk you through setting up and using the now-next methodology in your project.

## Setup (< 1 minute)

### Option 1: One-Prompt Setup (Easiest)

Copy this prompt to your AI coding assistant:

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

### Option 2: Manual Setup

1. **Copy templates to your project:**
   ```bash
   # Download NOW.md template
   curl -o NOW.md https://raw.githubusercontent.com/soutone/now-next-methodology/main/templates/NOW.md
   
   # For Claude Code:
   mkdir -p .claude/commands
   curl -o .claude/commands/next.md https://raw.githubusercontent.com/soutone/now-next-methodology/main/templates/next.md
   
   # For OpenCode:
   mkdir -p .config/opencode/commands
   curl -o .config/opencode/commands/next.md https://raw.githubusercontent.com/soutone/now-next-methodology/main/templates/next.md
   ```

2. **Fill in NOW.md placeholders:**
   - Replace `[YYYY-MM-DD]` with today's date
   - Replace `[Status]` with "Initial Setup"
   - Add your project name at the top
   - Fill in initial state

3. **Commit the setup:**
   ```bash
   git add NOW.md .claude/commands/next.md  # or .config/opencode/commands/next.md
   git commit -m "Initialize now-next methodology"
   ```

## First Use

### Running /next

Simply type `/next` in your AI coding assistant. The AI will:

1. Read your NOW.md file
2. Analyze what to work on next
3. Implement the work with testing
4. Update NOW.md
5. Commit changes
6. Report what was done

### What to Expect

**First iteration:**
- AI will likely ask you to define project scope and goals
- It might set up basic project structure
- NOW.md will be updated with initial accomplishments

**Subsequent iterations:**
- AI continues from where it left off
- Each session adds to "Recent Accomplishments"
- Clear progression visible in NOW.md

## Daily Workflow

```
┌─────────────────────────────────────┐
│  You: /next                         │
└─────────────────────────────────────┘
              ↓
┌─────────────────────────────────────┐
│  AI reads NOW.md                    │
│  AI analyzes next steps             │
│  AI implements feature/fix          │
│  AI tests changes                   │
│  AI updates NOW.md                  │
│  AI commits changes                 │
└─────────────────────────────────────┘
              ↓
┌─────────────────────────────────────┐
│  AI reports:                        │
│  ✅ What was done                   │
│  ⚠️  User actions needed (if any)   │
│  📝 What's next                     │
└─────────────────────────────────────┘
```

## Tips for Success

### 1. Keep NOW.md Updated
- Don't manually edit it often—let `/next` update it
- If you make changes outside `/next`, update NOW.md manually
- Keep "Next Steps" prioritized (most important first)

### 2. Trust the AI
- The `/next` command is designed to work autonomously
- Let it make implementation decisions
- Only provide input when it asks for business/product decisions

### 3. Review Accomplishments
- Regularly scan "Recent Accomplishments" section
- Verify the AI is working on the right priorities
- Adjust "Next Steps" if priorities change

### 4. Handle User Actions Promptly
- When AI reports "⚠️ USER ACTION REQUIRED"
- Complete those actions before next `/next` run
- Update NOW.md if you completed them manually

### 5. Use for All Work
- Even small fixes should go through `/next`
- Maintains consistent history
- Prevents context drift

## Common Patterns

### Starting a New Feature
```
You: /next

AI: [Reads NOW.md, sees "Add user authentication" in Next Steps]
AI: [Implements JWT auth with tests]
AI: [Updates NOW.md with accomplishment]
AI: [Commits changes]
AI: ✅ Implemented user authentication
    ⚠️ USER ACTION REQUIRED:
    1. Set JWT_SECRET environment variable
    📝 Next: Add password reset functionality
```

### Debugging an Issue
Update NOW.md manually:
```markdown
## Open Challenges

### Technical
- Login endpoint returning 500 error on production
```

Then:
```
You: /next

AI: [Sees the challenge, investigates]
AI: [Fixes the bug]
AI: [Updates NOW.md, removes from challenges]
AI: [Commits fix]
```

### Changing Direction
Edit "Next Steps" in NOW.md to reprioritize, then run `/next`.

## Troubleshooting

### "AI isn't working on what I want"
- Check "Next Steps" in NOW.md—is your priority listed first?
- Update "Next Steps" to be more specific
- Add context to "Open Challenges" if needed

### "AI forgot what we were doing"
- This shouldn't happen if NOW.md is up-to-date
- If it does, manually add context to "Current Status"
- Consider breaking down "Next Steps" into smaller tasks

### "/next command not found"
- Ensure `.claude/commands/next.md` (or `.config/opencode/commands/next.md`) exists
- Restart your AI coding assistant
- Try manual setup again

## Next Steps

- Read [Philosophy & Principles](./philosophy.md) to understand why this works
- Check [Customization Guide](./customization.md) to adapt to your workflow

**Ready to start?** Run `/next` and let your AI take the wheel! 🚀
