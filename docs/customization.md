# Customization Guide

The templates are just starting points. Adapt them to your needs.

## Customizing NOW.md

### Add Sections

**Metrics:**
```markdown
## Metrics
- Test Coverage: 78%
- Build Time: 12s
- Bundle Size: 234KB
```

**Dependencies:**
```markdown
## Dependencies
| Service | Status | Notes |
|---------|--------|-------|
| Stripe API | ✅ Connected | Test mode |
| PostgreSQL | ✅ Running | Local dev |
```

**Architecture Decisions:**
```markdown
## Architecture Decisions

### 2026-01-12: Chose PostgreSQL over MongoDB
**Reasoning:** Need strong consistency for financial data.
```

### Remove Sections

Don't need something? Delete it. The minimum viable NOW.md is:

```markdown
# Project Name

## Current Status
[What's happening now]

## Next Steps
1. [Priority 1]
2. [Priority 2]
```

## Customizing /next Command

### Change Decision Framework

Edit the "Strategic Analysis" section in your local `next.md`:

```markdown
**Decision framework:**
- Quick wins first (build momentum)
- Then high-impact items
- Then long-term work
```

### Add Custom Phases

```markdown
### Phase 3.5: Security Check
Before committing:
- Run security linter
- Check for exposed secrets
```

### Change Commit Format

```markdown
git commit -m "feat: [description]"  # Conventional Commits
git commit -m "[TICKET-123] [description]"  # Ticket-based
```

## Tech Stack Examples

### Python/Django
```markdown
## Quick Reference
| Command | Purpose |
|---------|---------|
| `/next` | Continue development |
| `pytest` | Run tests |
| `python manage.py migrate` | Run migrations |
```

### React/Next.js
```markdown
## Metrics
- Bundle Size: 234KB
- Lighthouse Score: 92/100
```

## Integration with Existing Tools

### GitHub Issues
```markdown
## Next Steps
1. **Implement auth** ([#123](github-link))
2. **Add payments** ([#124](github-link))
```

### CI/CD Validation
```yaml
# Validate NOW.md exists and has required sections
- name: Check NOW.md
  run: |
    test -f NOW.md
    grep -q "## Current Status" NOW.md
```

---

**The best customization is the one that makes you actually use the methodology.**

Start simple, add what you need, remove what you don't.
