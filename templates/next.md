# Next Development Iteration

Execute the next development iteration using the now-next methodology.

## Workflow

### Phase 1: Context Gathering
1. Read NOW.md to understand current project state
2. Read project-specific instruction files (AGENTS.md, etc.) if they exist
3. Review recent git commits to understand what changed
4. Check for any blocking issues or unresolved challenges

### Phase 2: Strategic Analysis

Analyze the current state and determine the most impactful next steps:

**Questions to answer:**
- What's the current priority based on NOW.md?
- What open challenges need addressing?
- What's blocking progress?
- What would provide the most value right now?
- Are there any quick wins available?

**Decision framework:**
- Unblock > High Impact > Low Effort > Long Term
- Fix breaking issues before adding features
- Complete in-progress work before starting new work
- Prioritize user-facing value when possible

### Phase 3: Implementation

Execute the chosen next steps:

**Implementation requirements:**
- Write clean, well-documented code following project patterns
- Add/update tests as appropriate
- Validate changes work correctly (run tests, manual testing)
- Use appropriate tools and agents as needed
- Handle errors gracefully

**Key principles:**
- Make atomic, focused changes
- Test thoroughly before moving on
- Document non-obvious decisions
- Follow existing code style and conventions

### Phase 4: User Actions Check

Identify any actions the user needs to take:

**Common requirements:**
- API keys to configure
- Services to set up or authenticate
- External dependencies to install
- Environment variables to set
- Configuration files to create
- Database migrations to run

**Format:**
```
⚠️ USER ACTION REQUIRED:
1. [Specific action with exact commands]
2. [Another action]
```

### Phase 5: Update & Commit

1. **Update NOW.md:**
   - Add new accomplishment section with today's date
   - Include Purpose, What Was Done, Impact, and Commit hashes
   - Update Current Status section
   - Update Open Challenges (remove resolved, add new)
   - Update Next Steps based on new state
   - Update Quick Reference if new commands were added

2. **Commit all changes:**
   ```bash
   git add -A
   git commit -m "Descriptive message of what was accomplished"
   ```

3. **Report to user:**
   - ✅ Summary of what was accomplished
   - 📊 Impact on project progress
   - ⚠️ Any user actions needed (if applicable)
   - 📝 What's next (preview of upcoming work)

---

## Key Principles

- **Autonomous:** Make decisions and implement without asking for permission unless major architectural changes
- **Validated:** Test and verify all changes work before updating NOW.md
- **Documented:** Keep NOW.md accurate, detailed, and up-to-date
- **Committed:** Always commit successful changes with clear messages
- **Transparent:** Clearly communicate what was done and what's needed from user
- **Focused:** Complete one meaningful unit of work per iteration
- **Progressive:** Each iteration should move the project measurably forward

---

## Anti-Patterns to Avoid

- ❌ Starting work without reading NOW.md first
- ❌ Making changes without testing them
- ❌ Forgetting to update NOW.md after completing work
- ❌ Committing broken or untested code
- ❌ Working on low-priority tasks when high-priority ones exist
- ❌ Asking for permission on routine implementation decisions
- ❌ Leaving the project in a broken state
