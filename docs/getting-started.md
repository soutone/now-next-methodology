# Getting Started

## Install the Command

**Claude Code:**
```bash
curl -o ~/.claude/commands/setup-now-next.md https://raw.githubusercontent.com/soutone/now-next-methodology/main/templates/claude-code/setup-now-next.md
```

**OpenCode:**
```bash
curl -o ~/.config/opencode/commands/setup-now-next.md https://raw.githubusercontent.com/soutone/now-next-methodology/main/templates/opencode/setup-now-next.md
```

## Use It

In any project directory:
```
/setup-now-next
```

This creates:
- `NOW.md` - Your project state tracker
- `.claude/commands/next.md` (or `.config/opencode/commands/next.md`) - The /next command

## Start Developing

Just run:
```
/next
```

Your AI will:
1. Read NOW.md to understand current state
2. Decide what to work on next
3. Implement it
4. Update NOW.md
5. Commit the changes

## Daily Workflow

```
You: /next
AI: [reads NOW.md, implements feature, updates state, commits]
AI: ✅ Done! Added user authentication. Next: password reset

You: /next
AI: [continues from where it left off...]
```

## Tips

- **Trust it** - Let the AI work autonomously
- **Review NOW.md** - Scan recent accomplishments to stay in sync
- **Update priorities** - Edit "Next Steps" if direction changes
- **Use for everything** - Even small fixes, to maintain history

## That's It

No complex setup, no dependencies, just markdown files that keep your AI on track.

---

For more details: [Why This Works](./philosophy.md) | [Customization](./customization.md)
