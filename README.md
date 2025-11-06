# Tech-Tickets 🎫

**Central issue tracker for ALL Catalyst Partners projects**

One place for all tasks, bugs, features, and ideas across every repository.

**Project Board:** https://github.com/users/tisa-pixel/projects/4

---

## Why Centralize Issues?

- ✅ See all work across projects in one view
- ✅ No switching between repositories
- ✅ Easy filtering and organization
- ✅ Automatic sync to unified project board
- ✅ Simple workflow for both CLI and web

---

## Creating Issues

### Option 1: GitHub Web (Easiest)

1. Go to https://github.com/tisa-pixel/Tech-Tickets/issues/new/choose
2. Fill out the form:
   - **Project:** Select which project this belongs to (tech-stack, propertyradar, etc.)
   - **Type:** Bug, Feature, Task, etc.
   - **Priority:** How urgent is it?
   - **Description:** What needs to be done?
3. Submit - automatically adds to project board!

### Option 2: Command Line (Fastest)

```bash
# Basic issue
gh issue create -R tisa-pixel/Tech-Tickets \
  -t "Fix authentication bug" \
  -l "bug" \
  -b "Authentication failing for returning users"

# With priority
gh issue create -R tisa-pixel/Tech-Tickets \
  -t "Add dark mode" \
  -l "enhancement" \
  -b "Users requesting dark mode support"
```

**Note:** When creating via CLI, you'll need to manually set the **Project** field in the project board after creation.

---

## Labels

Use labels to categorize issues (not to specify which project - use the Project field for that!):

**Issue Types:**
- `bug` - Something broken
- `enhancement` - New feature or improvement
- `documentation` - Docs updates
- `task` - General todo
- `question` - Need help or clarification

**Priority (optional):**
- Set priority in the project board's Priority field

---

## Using the Project Board

View all issues: https://github.com/users/tisa-pixel/projects/4

**Custom Fields:**
- **Project:** Which repo/project this belongs to (tech-stack, propertyradar, etc.)
- **Priority:** 🔴 High, 🟡 Medium, 🟢 Low, ⚪ None
- **Effort:** 🟦 Small, 🟨 Medium, 🟧 Large, 🟥 XLarge
- **Status:** Todo, In Progress, Done

**Filtering:**
- Click "Project" column to filter by specific project
- Click "Priority" to see urgent items
- Use search bar for keywords
- Group by Project to see all issues organized by repository

---

## Workflow

### Adding New Work

1. Create issue (web form or CLI)
2. Issue automatically appears on project board
3. Set the **Project** field to indicate which repository it belongs to
4. Optionally set Priority and Effort

### Working on Issues

1. View project board
2. Filter by Project if working on specific repository
3. Move issue to "In Progress"
4. Do the work in the appropriate repository
5. Reference the issue in commits: `Fixes tisa-pixel/Tech-Tickets#42`
6. Move to "Done" when complete

---

## Examples

### Bug Report

```bash
gh issue create -R tisa-pixel/Tech-Tickets \
  -t "PropertyRadar API returns 500 error" \
  -l "bug" \
  -b "The distress scorer fails when processing properties with null values. Need to add null checks."
```

Then in project board: Set Project = "propertyradar"

### Feature Request

```bash
gh issue create -R tisa-pixel/Tech-Tickets \
  -t "Add newsletter signup to landing page" \
  -l "enhancement" \
  -b "Add email capture form in the footer"
```

Then in project board: Set Project = "tisa-portfolio"

### Task

```bash
gh issue create -R tisa-pixel/Tech-Tickets \
  -t "Update Google Workspace SDK docs" \
  -l "documentation,task" \
  -b "Add examples for Drive API integration"
```

Then in project board: Set Project = "tech-stack"

---

## Automation Setup

To automatically add new issues to the project board:

1. Go to your project board: https://github.com/users/tisa-pixel/projects/4
2. Click **⋯** (top right) → **Workflows**
3. Find **"Item added to project"** workflow
4. Enable auto-add for the Tech-Tickets repository
5. Save

**No GitHub Actions or tokens needed!** This uses GitHub's built-in project automation.

---

## Projects

Current projects tracked in this system:

- tech-stack
- cgm-lead-generation
- collective-genius-scraper
- hometrust-colorado
- propertyradar
- tisa-portfolio
- business-docs
- deal-desk
- voice-lead-bot
- email-authentication
- claude-performance-tracker
- other (cross-project or misc)

---

## Tips

- Use descriptive issue titles
- Add context in the description
- Set the Project field so you know which repo it belongs to
- Use Priority field for urgent items
- Close issues when done
- Reference issues in commits: `Fixes #42`

---

**Updated:** November 6, 2025
**Owner:** Tisa Daniels (Catalyst Partners LLC)
