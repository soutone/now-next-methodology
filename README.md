# Now-Next Methodology

**Simple workflow for AI coding assistants that maintains context across sessions**

Never lose track of what your AI was working on. Just a `NOW.md` file to track state and a `/next` command to continue development.

---

## 🚀 Setup (30 seconds)

Install the `/setup-now-next` command once:

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

That's it! Now just run `/next` whenever you want your AI to continue development.

---

## 💡 What This Does

Creates two files in your project:

**NOW.md** - Tracks your project state:
- Recent accomplishments (what got done)
- Current status (where you are)
- Open challenges (what's blocking you)
- Next steps (what to do next)

**/next command** - Tells your AI to:
1. Read NOW.md
2. Pick the next task
3. Implement it with tests
4. Update NOW.md
5. Commit changes

Your AI maintains context across sessions. No more "what were we working on?"

---

## 🎯 Real Projects Using This

- **[Documatic](https://documatic.fly.dev)** - AI documentation tool
- **[Credible](https://credible.fly.dev)** - Credential verification
- **[MailCheck](https://mailcheck-api.fly.dev)** - Email validation

---

## 📚 Learn More

- **[Getting Started](./docs/getting-started.md)** - Detailed walkthrough
- **[Why This Works](./docs/philosophy.md)** - The reasoning behind it
- **[Customization](./docs/customization.md)** - Adapt to your needs

---

## 🤝 Contributing

Found this useful? Contributions welcome!

- Share your experience in [Discussions](https://github.com/soutone/now-next-methodology/discussions)
- Report issues or suggest improvements
- See [CONTRIBUTING.md](./CONTRIBUTING.md)

---

## 📄 License

MIT - Use it however you want.

---

**Just a simple workflow that worked for me. Hope it helps you too.**

*If it does, ⭐ the repo!*
