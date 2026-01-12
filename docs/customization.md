# Customization Guide

The now-next methodology is designed to be flexible. Adapt it to match your workflow.

## Customizing NOW.md

### Adding Sections

Common additions:

#### Dependencies
Track external dependencies and their status:
```markdown
## Dependencies

| Service | Status | Notes |
|---------|--------|-------|
| Stripe API | ✅ Connected | Test mode |
| SendGrid | ⚠️ Needs key | For email notifications |
| PostgreSQL | ✅ Running | Local dev |
```

#### Metrics
Track key project metrics:
```markdown
## Metrics

- **Test Coverage:** 78% (+5% this week)
- **Build Time:** 12s (down from 18s)
- **Bundle Size:** 234KB (target: <200KB)
- **API Response Time:** 120ms avg
```

#### Team Context
For multi-person projects:
```markdown
## Team Context

- **Alice:** Working on authentication refactor
- **Bob:** Blocked on design review for dashboard
- **AI:** Implementing payment integration
```

#### Architecture Decisions
Record important technical decisions:
```markdown
## Architecture Decisions

### 2026-01-12: Chose PostgreSQL over MongoDB
**Reasoning:** Need strong consistency for financial data, relational schema fits our domain model better.
```

### Removing Sections

If you don't need certain sections, remove them:
- **Open Challenges** - If you prefer to track issues in GitHub
- **Quick Reference** - If commands are documented elsewhere
- **Recent Accomplishments** - If git commits are sufficient

**Minimum viable NOW.md:**
```markdown
# Project Name

## Current Status
[What's happening now]

## Next Steps
1. [Priority 1]
2. [Priority 2]
```

### Section Ordering

Reorder sections to match your priorities:

**Default order:**
1. Recent Accomplishments
2. Current Status
3. Open Challenges
4. Next Steps

**Alternative (focus on future):**
1. Current Status
2. Next Steps
3. Open Challenges
4. Recent Accomplishments

**Alternative (focus on blockers):**
1. Current Status
2. Open Challenges
3. Next Steps
4. Recent Accomplishments

## Customizing /next Command

### Changing the Decision Framework

Edit the "Strategic Analysis" section in `next.md`:

**Default:**
```markdown
**Decision framework:**
- Unblock > High Impact > Low Effort > Long Term
```

**Alternative (speed focus):**
```markdown
**Decision framework:**
- Quick wins first (build momentum)
- Then high-impact items
- Then long-term work
```

**Alternative (quality focus):**
```markdown
**Decision framework:**
- Fix bugs/tech debt first
- Then implement features
- Always include tests
```

### Adding Custom Phases

Add project-specific phases to the workflow:

```markdown
### Phase 3.5: Security Check
Before committing:
- Run security linter
- Check for exposed secrets
- Validate input sanitization
```

### Changing Commit Message Format

Modify Phase 5 to use your preferred format:

**Conventional Commits:**
```markdown
git commit -m "feat: [description]"
git commit -m "fix: [description]"
git commit -m "docs: [description]"
```

**Ticket-based:**
```markdown
git commit -m "[TICKET-123] [description]"
```

### Adding Integrations

Extend `/next` to interact with external tools:

**Notion integration:**
```markdown
### Phase 5.5: Update Notion
- Post summary to project Notion page
- Update progress tracker
```

**Slack integration:**
```markdown
### Phase 5.5: Notify Team
- Post completion message to #dev-updates
- Tag relevant team members if user action required
```

**Linear/Jira integration:**
```markdown
### Phase 5.5: Update Ticket
- Move ticket to "Done" status
- Add comment with commit hash
```

## Tech Stack-Specific Customizations

### Python/Django Projects

Add to Quick Reference:
```markdown
| Command | Purpose |
|---------|---------|
| `/next` | Continue development |
| `pytest` | Run test suite |
| `python manage.py migrate` | Run migrations |
| `black .` | Format code |
```

Add to Open Challenges:
```markdown
### Technical
- Need to add migration for [feature]

### DevOps
- PostgreSQL setup needed for production
```

### React/Next.js Projects

Add to Quick Reference:
```markdown
| Command | Purpose |
|---------|---------|
| `/next` | Continue development |
| `npm test` | Run tests |
| `npm run build` | Production build |
| `npm run lint` | Check code quality |
```

Add metrics section:
```markdown
## Metrics

- **Bundle Size:** 234KB
- **Lighthouse Score:** 92/100
- **Core Web Vitals:** All green
```

### Rust Projects

Add to /next Phase 3:
```markdown
**Rust-specific requirements:**
- Run `cargo clippy` for lints
- Run `cargo test` for all tests
- Ensure no unsafe code without justification
- Update Cargo.toml if dependencies added
```

### Mobile Apps (React Native, Flutter)

Add device testing to Phase 3:
```markdown
**Mobile-specific requirements:**
- Test on iOS simulator
- Test on Android emulator
- Verify responsive layouts
- Check performance on low-end devices
```

## Workflow Variations

### Multi-Repo Projects

Create NOW.md at the root with references:
```markdown
## Current Status

Main API: Feature-complete, pending security review
Frontend: In progress, see `frontend/NOW.md`
Mobile App: Blocked on API endpoints, see `mobile/NOW.md`

## Quick Reference

| Repo | NOW.md | Status |
|------|--------|--------|
| API | `api/NOW.md` | ✅ Stable |
| Frontend | `frontend/NOW.md` | 🚧 Active |
| Mobile | `mobile/NOW.md` | ⏸️ Blocked |
```

### Sprint-Based Work

Add sprint tracking:
```markdown
## Current Sprint

**Sprint 5 (Jan 8-22)**
**Goal:** Launch MVP to beta users

**Progress:** 7/12 stories complete

| Story | Status | Owner |
|-------|--------|-------|
| User auth | ✅ Done | AI |
| Dashboard | 🚧 In Progress | AI |
| Payments | ⏸️ Blocked | Needs Stripe key |
```

### Experimental/Research Projects

Adjust sections for exploration:
```markdown
## Hypotheses

1. **Caching will reduce API calls by >50%**
   - Status: Testing
   - Result: TBD

2. **WebAssembly faster than pure JS for [task]**
   - Status: Implemented
   - Result: ❌ Actually slower, reverting

## Experiments

### Current
- Testing different embedding models for semantic search

### Completed
- Compared PostgreSQL vs MongoDB (chose PostgreSQL)
```

## Integration with Existing Tools

### GitHub Projects
Keep NOW.md synced with GitHub issues:
```markdown
## Next Steps

1. **Implement user authentication** ([#123](github-issue-link))
2. **Add payment integration** ([#124](github-issue-link))
```

### Claude Projects / OpenCode Context
Add NOW.md to project knowledge:
- Claude: Add NOW.md to project files
- OpenCode: Reference NOW.md in AGENTS.md

### CI/CD Pipelines
Add NOW.md validation:
```yaml
# .github/workflows/validate-now.yml
name: Validate NOW.md
on: [push]
jobs:
  validate:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Check NOW.md exists
        run: test -f NOW.md
      - name: Validate structure
        run: |
          grep -q "## Current Status" NOW.md
          grep -q "## Next Steps" NOW.md
```

## Tips for Customization

### Start Minimal
Begin with the basic template, then add sections as you find the need.

### Be Consistent
If you customize, keep the same structure across all projects for muscle memory.

### Document Your Customizations
Add a section to NOW.md explaining project-specific conventions:
```markdown
## Notes

**NOW.md Customizations:**
- Using "Sprint Goals" instead of "Next Steps"
- Metrics updated automatically by CI
- Architecture decisions tracked in separate ADR.md
```

### Evolve Over Time
The methodology should adapt to your needs. If something isn't working, change it.

---

**The best customization is the one that makes you want to use the methodology.**

Don't optimize for perfection—optimize for what actually helps you ship code.
