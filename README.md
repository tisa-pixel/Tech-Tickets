# Tech-Tickets 🎫

**Central issue tracker for ALL Catalyst Partners repositories**

Track bugs, features, tasks, and ideas from all your projects in one place. Automatically syncs to your unified project board.

---

## 🎯 Purpose

**This is your ONE PLACE for all issues across ALL repositories:**

- ✅ tech-stack issues
- ✅ cgm-lead-generation issues
- ✅ hometrust-colorado issues
- ✅ propertyradar issues
- ✅ tisa-portfolio issues
- ✅ business-docs issues
- ✅ Any other repository issues

**Why centralize?**
- 📊 See all work in one place
- 🔍 Easy to search and filter
- 📋 Unified project board
- 🤖 Automatic organization
- 🚀 No switching between repos

---

## 📝 How to Create Issues

### From Command Line (Recommended)

```bash
# Create an issue for any project
gh issue create --repo tisa-pixel/Tech-Tickets \
  --title "Fix authentication bug in cgm-lead-generation" \
  --label "repo:cgm-lead-generation,bug" \
  --body "Description of the issue..."

# Quick issue
gh issue create -R tisa-pixel/Tech-Tickets \
  -t "Add dark mode to landing page" \
  -l "repo:tisa-portfolio,enhancement"
```

### From Slack

Issues created from Slack automatically appear here and on the project board.

### From GitHub Web

1. Go to https://github.com/tisa-pixel/Tech-Tickets/issues
2. Click **"New issue"**
3. Add title and description
4. **Important:** Add a repo label (e.g., `repo:tech-stack`)
5. Submit

---

## 🏷️ Label System

### Repository Labels (Required)

Tag each issue with the project it belongs to:

- `repo:tech-stack` - Tech infrastructure and integrations
- `repo:cgm-lead-generation` - CGM lead gen project
- `repo:hometrust-colorado` - HomeTrust website
- `repo:propertyradar` - PropertyRadar tools
- `repo:tisa-portfolio` - Personal portfolio
- `repo:business-docs` - Business documentation
- `repo:deal-desk` - Deal desk automation
- `repo:voice-lead-bot` - Voice lead bot
- `repo:other` - Misc or cross-project

### Type Labels (Optional but recommended)

- `bug` - Something isn't working
- `enhancement` - New feature or improvement
- `documentation` - Documentation updates
- `question` - Questions or help needed
- `task` - General task or todo

### Priority Labels (Optional)

- `priority:high` - Urgent, blocking work
- `priority:medium` - Important but not blocking
- `priority:low` - Nice to have

---

## 🤖 Automation

All new issues are **automatically added** to your unified project board:

**Project Board:** https://github.com/users/tisa-pixel/projects/4

### How It Works

1. Create issue in Tech-Tickets (from anywhere)
2. GitHub Action triggers automatically
3. Issue appears on project board instantly
4. No manual work required!

### Setup Required (One-time)

The automation needs a Personal Access Token (PAT) to function.

**Steps:**

1. **Create PAT:**
   - Go to: https://github.com/settings/tokens?type=beta
   - Click **"Generate new token (fine-grained)"**
   - Name: `Tech-Tickets Project Automation`
   - Expiration: 90 days
   - Repository access: **Only select repositories** → `Tech-Tickets`
   - Permissions:
     - Repository: **Issues** → Read and write
     - Organization: **Projects** → Read and write
   - Generate and copy token

2. **Add to repository:**
   - Go to: https://github.com/tisa-pixel/Tech-Tickets/settings/secrets/actions
   - New repository secret
   - Name: `ADD_TO_PROJECT_PAT`
   - Paste token
   - Save

3. **Done!** Automation active for all new issues.

---

## 📊 Filtering & Searching

### View Issues by Repository

```bash
# View all tech-stack issues
gh issue list -R tisa-pixel/Tech-Tickets -l "repo:tech-stack"

# View all bugs
gh issue list -R tisa-pixel/Tech-Tickets -l "bug"

# View high priority items
gh issue list -R tisa-pixel/Tech-Tickets -l "priority:high"

# Combine filters
gh issue list -R tisa-pixel/Tech-Tickets -l "repo:propertyradar,bug"
```

### On GitHub Web

Use the label filters on the issues page:
https://github.com/tisa-pixel/Tech-Tickets/issues

Click any label to filter, or use the search bar:
- `label:repo:tech-stack`
- `label:bug label:priority:high`
- `is:open label:repo:cgm-lead-generation`

---

## 💡 Examples

### Bug Report

```bash
gh issue create -R tisa-pixel/Tech-Tickets \
  -t "PropertyRadar API returns 500 error" \
  -l "repo:propertyradar,bug,priority:high" \
  -b "The distress scorer fails when processing properties with null values."
```

### Feature Request

```bash
gh issue create -R tisa-pixel/Tech-Tickets \
  -t "Add email capture to landing page" \
  -l "repo:tisa-portfolio,enhancement" \
  -b "Need a newsletter signup form on the landing page footer."
```

### Task/Todo

```bash
gh issue create -R tisa-pixel/Tech-Tickets \
  -t "Update Google Workspace SDK documentation" \
  -l "repo:tech-stack,documentation,task" \
  -b "Add examples for Drive API integration."
```

### Cross-Project Issue

```bash
gh issue create -R tisa-pixel/Tech-Tickets \
  -t "Standardize .gitignore across all projects" \
  -l "repo:other,task" \
  -b "Create a standard .gitignore template for all repos."
```

---

## 🔗 Related Resources

- **Project Board:** https://github.com/users/tisa-pixel/projects/4
- **Tech Roadmap:** https://github.com/tisa-pixel/tech-roadmap
- **Main Tech Stack:** https://github.com/tisa-pixel/tech-stack

---

## 🎨 Issue Templates (Coming Soon)

Planned templates for common issue types:
- Bug report template
- Feature request template
- Task template
- Question template

---

## 📋 Best Practices

1. **Always add a repo label** - Know which project it belongs to
2. **Use descriptive titles** - Make it easy to understand at a glance
3. **Add context in the body** - Explain the issue clearly
4. **Use priority labels** - Help sort what's urgent
5. **Close when done** - Keep the list clean
6. **Link related issues** - Use `#issue-number` to reference

---

## 🔄 Workflow

### Creating Issues

1. Identify which repository the issue belongs to
2. Create issue in Tech-Tickets with proper labels
3. Issue auto-adds to project board
4. Work on it when ready

### Working on Issues

1. View project board or filter by repo
2. Pick an issue to work on
3. Do the work in the appropriate repository
4. Close the issue when complete

### Cross-Referencing

When committing code, reference the issue:
```bash
git commit -m "Fix authentication bug

Fixes tisa-pixel/Tech-Tickets#42"
```

GitHub will automatically link the commit to the issue!

---

## ❓ FAQ

**Q: Why not use issues in each repository?**
A: Centralization makes it easier to see all work, prioritize across projects, and avoid context switching.

**Q: Can I still use individual repo issues?**
A: Yes, but using Tech-Tickets gives you the unified view and project board automation.

**Q: What if an issue spans multiple repos?**
A: Perfect use case! Use `repo:other` label or tag multiple repos.

**Q: How do I migrate existing issues?**
A: You can manually recreate important ones here, or link to them in the issue body.

---

## 📞 Support

Having trouble with the automation? Check:
1. PAT token is set correctly in repository secrets
2. Token has not expired
3. Token has correct permissions
4. GitHub Actions are enabled for the repo

---

**Created:** October 31, 2025
**Updated:** November 1, 2025

**Owner:** Tisa Daniels (Catalyst Partners LLC)

---

Created with ❤️ by Claude Code
