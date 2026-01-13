# Setup Now-Next Methodology

Initialize a project with the now-next methodology: NOW.md file for tracking status and a /next command for iterative development workflows.

## What This Does

1. Creates a `NOW.md` file with structured sections for tracking project state
2. Creates a local `/next` command that implements the now-next workflow
3. Initializes git repository if not already present
4. Creates initial commit with the setup

## Workflow

### Phase 1: Analysis
- Check if NOW.md already exists (don't overwrite!)
- Check if git repo is initialized
- Check if .claude/commands/ directory exists
- Get project name from directory

### Phase 2: Create NOW.md

Download the template from:
https://raw.githubusercontent.com/soutone/now-next-methodology/main/templates/NOW.md

Replace placeholders:
- `[YYYY-MM-DD]` → Current date
- `[Status]` → "Initial Setup"
- Fill in initial accomplishment section documenting the setup

### Phase 3: Create /next Command

Create `.claude/commands/next.md` from template:
https://raw.githubusercontent.com/soutone/now-next-methodology/main/templates/next.md

### Phase 4: Git Initialization

If no git repo exists:
```bash
git init
git add NOW.md .claude/commands/next.md
git commit -m "Initialize now-next methodology"
```

If git repo exists:
```bash
git add NOW.md .claude/commands/next.md
git commit -m "Add now-next methodology"
```

### Phase 5: Completion

Report to user:
```
✅ NOW.md created
✅ /next command created  
✅ Git repo initialized/updated
📝 Next: Run `/next` to start your first development iteration
```

## Implementation Notes

- Don't overwrite NOW.md if it already exists (warn user instead)
- Create `.claude/commands/` directory if it doesn't exist
- Preserve any existing AGENTS.md or project-specific instruction files
- Use actual project directory name, not "[Project Name]"
- Use actual current date in YYYY-MM-DD format
