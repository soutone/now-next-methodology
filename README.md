# Now-Next Methodology

**Keep your AI on track across sessions with two simple files: NOW.md + /next command**

---

## Setup (30 seconds)

**Claude Code:**
```bash
curl -o ~/.claude/commands/setup-now-next.md https://raw.githubusercontent.com/soutone/now-next-methodology/main/templates/claude-code/setup-now-next.md
```

**OpenCode:**
```bash
curl -o ~/.config/opencode/commands/setup-now-next.md https://raw.githubusercontent.com/soutone/now-next-methodology/main/templates/opencode/setup-now-next.md
```

Then in any project:
```
/setup-now-next
```

---

## How It Works

**NOW.md** tracks your project state:
- Recent accomplishments (what got done)
- Current status (where you are)
- Next steps (what to do next)

**/next** tells your AI to:
1. Read NOW.md
2. Pick the next task
3. Implement + test it
4. Update NOW.md
5. Commit changes

Your AI maintains context across sessions. No more "what were we working on?"

---

## Daily Workflow

```
You: /next
AI: [reads NOW.md, implements feature, updates state, commits]
AI: ✅ Done! Added user authentication. Next: password reset

You: /next
AI: [continues from where it left off...]
```

That's it. Just run `/next` whenever you want to continue development.

---

## Real Projects Using This

- **[Documatic](https://documatic.fly.dev)** - AI documentation tool
- **[Credible](https://credible.fly.dev)** - Credential verification
- **[MailCheck](https://mailcheck-api.fly.dev)** - Email validation

---

## Customization

The templates are starting points. Edit NOW.md sections to fit your needs:

- Add metrics, dependencies, architecture decisions
- Remove sections you don't need
- Change commit formats in /next command
- Adapt to your tech stack

See [templates/](./templates/) for the files that get created.

---

## Why This Works

AI assistants are great at executing but can't remember state between sessions.

NOW.md externalizes that state into a markdown file both you and the AI can read.

Simple pattern that works.

---

## Contributing

Found this useful? 

- Share your experience in [Discussions](https://github.com/soutone/now-next-methodology/discussions)
- Report issues or improvements
- See [CONTRIBUTING.md](./CONTRIBUTING.md)

---

## License

MIT - Use it however you want.

---

**Just a workflow that worked for me. Hope it helps you too.**

*If it does, ⭐ the repo!*
