# Reddit Post Template for Now-Next Methodology

## Title Options

### Option 1 (Simple)
```
[slash-command] Now-Next Methodology - Two-file task management for Claude Code/OpenCode
```

### Option 2 (Benefit-focused)
```
Simple task management for AI-assisted coding: NOW.md + NEXT.md + /next command
```

### Option 3 (Problem-solution)
```
Losing context between Claude Code sessions? Try the Now-Next methodology
```

## Post Body

```markdown
So I came across this repo -- https://github.com/lout33/claude_life_assistant -- where they use a NOW.md file to track stuff, and I thought it would work great for tracking project status too.

Started using it in one project, then added a `/next` command to move between tasks. Worked so well that every time I started a new project, I'd tell my agent: "import the NOW.md + /next concept from project X and adapt it here."

After doing that like 5 times, I figured I should just package it up properly.

**What it is:**
- NOW.md tracks what you're working on right now
- NEXT.md queues what's coming up
- `/next` command to move between tasks

Just two markdown files in your repo. The AI reads them to keep context across sessions, and they evolve with your code in git.

Packaged it here: https://github.com/soutone/now-next-methodology

Works with both Claude Code and OpenCode. The `/setup-now-next` command creates both files if you want to try it.

Would love feedback if anyone gives it a shot :)
```

## Target Subreddits

| Subreddit | Focus | Post Strategy |
|-----------|-------|---------------|
| r/ClaudeCode | Main Claude Code community | Lead with practical example, emphasize Claude Code integration |
| r/opencodeCLI | OpenCode specific | Highlight OpenCode slash command, show examples |
| r/ClaudeCoder | Claude development | Technical depth, workflow optimization angle |
| r/ClaudeCodeAgents | Agent-focused | How it helps agents maintain context |
| r/llmcoding | Broader LLM coding | Emphasize universal applicability beyond Claude |
| r/CLine | Cline community | Cross-post with note about Cline compatibility |

## Engagement Tips

1. **Respond promptly** to questions and feedback
2. **Share real examples** from your own projects
3. **Be helpful**, not promotional
4. **Ask for feedback** - community input improves the methodology
5. **Cross-link** discussions between related subreddits

## Timing

- Post to r/ClaudeCode first (main community)
- Wait 24-48 hours for initial feedback
- Use insights to refine posts for other subreddits
- Space posts 1-2 days apart to avoid spam appearance
