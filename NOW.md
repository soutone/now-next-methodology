# Now-Next Methodology

**Last Updated:** 2026-01-13  
**Status:** Active - Promotion Phase

---

## Recent Accomplishments

### 2026-01-13 - Promotion Strategy Research
**Purpose:** Identify channels to promote the now-next methodology to Claude Code/OpenCode community

**What Was Done:**
- Researched AI-specific promotion channels (Reddit, awesome lists, marketplaces)
- Identified automation opportunities vs manual tasks
- Created NOW.md to track promotion efforts

**Impact:**
- Clear roadmap for reaching target audience
- Separated automated vs manual promotion tasks

---

## Current Status

Project has basic documentation (README, CONTRIBUTING, CUSTOMIZATION) and templates for both Claude Code and OpenCode. Ready to promote to the AI coding community.

**GitHub:** https://github.com/soutone/now-next-methodology

---

## Promotion Tasks

### Automated (AI can handle via APIs/CLI)

#### GitHub Awesome Lists (via gh CLI)
- [x] **PR to [awesome-claude-code-plugins](https://github.com/ccplugins/awesome-claude-code-plugins)**
  - Category: Workflow Orchestration
  - PR: https://github.com/ccplugins/awesome-claude-code-plugins/pull/12
  - Status: ✅ Submitted 2026-01-13
  
- [x] **PR to [awesome-claude-code](https://github.com/jmanhype/awesome-claude-code)**
  - Category: Documentation & Learning Resources
  - PR: https://github.com/jmanhype/awesome-claude-code/pull/7
  - Status: ✅ Submitted 2026-01-13

- [x] **PR to [claude-code-resources](https://github.com/jmckinley/claude-code-resources)**
  - Category: Templates
  - PR: https://github.com/jmckinley/claude-code-resources/pull/1
  - Status: ✅ Submitted 2026-01-13

#### Reddit Posts (Requires Manual Posting)
**Status:** No Reddit MCP available; automation requires PRAW setup with Reddit API credentials

- [ ] Post to r/ClaudeCode
- [ ] Post to r/opencodeCLI
- [ ] Post to r/ClaudeCoder
- [ ] Post to r/ClaudeCodeAgents
- [ ] Post to r/llmcoding
- [ ] Cross-post to r/CLine

**Automation Note:** Could automate via PRAW (Python Reddit API Wrapper) if user provides Reddit API credentials (client_id, client_secret, user_agent). For now, treating as manual task.

### Manual (User needs to handle)

#### Marketplace Submissions
- [ ] **[opencode.cafe](https://www.opencode.cafe/)** - Submit via their form
  - Requires: Public repo ✅, Description ✅, Installation instructions ✅
  - Follow [submission guidelines](https://www.opencode.cafe/guidelines)
  - Category: Slash Commands
  
- [ ] **[claudecodemarketplace.net](https://claudecodemarketplace.net/plugins)** - Submit via their process
  - Category: Skills or Tools
  
- [ ] **[claudecodeplugin.com](https://claudecodeplugin.com/)** - Create marketplace entry
  - Possibly automate if they have GitHub-based marketplace structure

#### Community Engagement
- [ ] Post detailed guide/tutorial on r/ClaudeCode with examples
- [ ] Share in MCP Discord channels (if not already done)
- [ ] Engage with comments and feedback on all platforms
- [ ] Create example NOW.md files for common project types

#### Content Creation
- [ ] Write Medium/Dev.to article explaining methodology
- [ ] Create video walkthrough (optional)
- [ ] Add real-world examples beyond the 3 WIP projects listed

---

## Open Challenges

### Technical
- None currently

### Promotion
- **Reddit API Access:** Need to verify if we can automate Reddit posts or if manual posting required
- **Marketplace Submission Process:** Some marketplaces may require manual review/approval
- **Community Engagement:** Need human touch for responding to feedback and questions

---

## Next Steps

### Immediate (AI completed)
1. ✅ **Created PRs to awesome lists**
   - awesome-claude-code-plugins PR #12
   - awesome-claude-code PR #7
   - claude-code-resources PR #1
   
2. ✅ **Researched Reddit automation**
   - No Reddit MCP available in OpenCode
   - Would require PRAW + Reddit API credentials for automation
   - Created Reddit post template at `.github/reddit-post-template.md`

3. **Prepare submission content** (Next priority)
   - Draft descriptions for marketplace submissions
   - Create screenshots/examples for visual appeal

### User Required
1. **Submit to marketplaces** (requires filling web forms)
2. **Post to Reddit communities** (if automation not available)
3. **Engage with community responses**

### Future Improvements
- Add more real-world example projects
- Create video tutorial
- Write blog post/article
- Set up GitHub Discussions for community
- Add "Projects Using This" badge for adopters
- Create templates for common frameworks (Next.js, Python, Rust, etc.)

---

## Quick Reference

| Command | Purpose |
|---------|---------|
| `/next` | Execute next development/promotion task |
| `gh pr create` | Submit PRs to awesome lists |
| `git log --oneline` | View recent commits |
