# Contributing to Now-Next Methodology

Thank you for your interest in contributing! This project aims to make AI-assisted development more effective through simple, proven workflows.

## How to Contribute

### 1. Share Your Experience

The most valuable contribution is **using the methodology and sharing what works (or doesn't)**.

**How to help:**
- Open an issue describing your use case and results
- Share before/after examples of productivity improvements
- Document challenges you encountered
- Suggest improvements based on real usage

### 2. Add Examples

Show how you've adapted the methodology for your domain.

**What we're looking for:**
- Real projects using now-next (sanitized for privacy)
- Tech stack-specific adaptations (Python/Django, React, Rust, etc.)
- Workflow variations (solo dev, team, open source)
- Custom sections or processes that worked well

**How to contribute:**
```bash
# 1. Fork the repo
# 2. Add your example
examples/your-project-name/
├── README.md (overview of project and how now-next helped)
├── NOW.md.example (sanitized snapshot)
└── next.md (if you customized it)

# 3. Open a pull request
```

### 3. Improve Documentation

Help others get started faster.

**Areas to improve:**
- Clarify confusing parts of guides
- Add more real-world examples
- Translate to other languages
- Create video tutorials or walkthroughs
- Write blog posts or case studies

### 4. Create Templates

Build ready-to-use templates for specific scenarios.

**Ideas:**
- Templates for different tech stacks
- Industry-specific templates (fintech, e-commerce, etc.)
- Team vs solo workflows
- Research/experimental projects

### 5. Build Tools

Create tools that make the methodology easier to use.

**Ideas:**
- NOW.md linter/validator
- GitHub Action to verify NOW.md structure
- CLI tool to initialize projects
- VSCode extension for NOW.md management
- Analytics dashboard for progress tracking

## Contribution Guidelines

### For Documentation

- **Clear and concise** - Developers are busy
- **Examples over explanation** - Show, don't just tell
- **Tested** - Make sure instructions actually work
- **Formatted** - Follow existing markdown style

### For Code/Templates

- **Simplicity** - Prefer simple over clever
- **Comments** - Explain non-obvious decisions
- **Tested** - Verify it works before submitting
- **Minimal** - Don't add unnecessary complexity

### For Examples

- **Real** - Based on actual usage, not hypothetical
- **Sanitized** - Remove sensitive information
- **Context** - Explain your use case and results
- **Honest** - Include what didn't work, not just successes

## Pull Request Process

1. **Open an issue first** (for non-trivial changes)
   - Describe what you want to add/change
   - Get feedback before investing time
   - Ensures alignment with project goals

2. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

3. **Make your changes**
   - Follow existing structure and style
   - Add/update documentation as needed
   - Test thoroughly

4. **Write a clear PR description**
   ```markdown
   ## What
   Brief description of changes

   ## Why
   Problem this solves or value it adds

   ## Testing
   How you verified it works
   ```

5. **Respond to feedback**
   - Be open to suggestions
   - Iterate based on review comments
   - Ask questions if something's unclear

## What We're NOT Looking For

### ❌ Framework Dependencies
- The methodology should stay tool-agnostic
- No npm packages, Python libraries, etc.
- Keep it as simple markdown files

### ❌ Over-Engineering
- Don't add complexity for edge cases
- Prefer convention over configuration
- Keep the barrier to entry low

### ❌ Platform Lock-In
- Should work with any AI coding assistant
- Not just Claude Code or OpenCode
- Avoid proprietary integrations

### ❌ Feature Bloat
- Focus on the core workflow
- Additional features should be optional add-ons
- When in doubt, keep it simple

## Getting Help

- **Questions:** Open a [GitHub Discussion](https://github.com/soutone/now-next-methodology/discussions)
- **Bugs:** Open an [Issue](https://github.com/soutone/now-next-methodology/issues)
- **Ideas:** Start a Discussion or open an Issue

## Code of Conduct

### Be Respectful
- Constructive criticism is welcome
- Personal attacks are not
- Assume good intent

### Be Helpful
- Help newcomers get started
- Share knowledge generously
- Celebrate others' contributions

### Be Collaborative
- Give credit where it's due
- Build on others' ideas
- Work together toward better workflows

## Recognition

Contributors will be:
- Listed in project README
- Credited in release notes
- Acknowledged in documentation

Significant contributions may lead to:
- Maintainer status
- Co-authorship on articles/talks
- Collaboration on related projects

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

## Current Priorities

**We especially need:**

1. **Real-world examples** - Show this working in production
2. **Tech stack templates** - Python, Rust, mobile, etc.
3. **Integration guides** - GitHub, Linear, Notion, etc.
4. **Video walkthroughs** - Visual learning for new users
5. **Translations** - Make this accessible globally

**See [open issues](https://github.com/soutone/now-next-methodology/issues) for specific tasks.**

---

**Thank you for helping make AI-assisted development better for everyone!** 🚀
