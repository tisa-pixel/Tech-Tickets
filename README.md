# Tech-Tickets

Automated issue tracking from Slack integrated with the main Tech Roadmap project board.

## 🤖 Automation

This repository has a GitHub Action that **automatically adds all new issues to the "Tech Roadmap - All Projects" board**.

### How It Works

When a new issue is created (from Slack, CLI, or web):
1. GitHub Action triggers automatically
2. Issue is added to: https://github.com/users/tisa-pixel/projects/4
3. Appears on your unified project board instantly

### Setup Required

The automation needs a Personal Access Token (PAT) to add issues to your project board.

**One-time setup:**

1. **Create a Personal Access Token:**
   - Go to: https://github.com/settings/tokens?type=beta
   - Click **"Generate new token (fine-grained)"**
   - Name: `Tech-Tickets Project Automation`
   - Expiration: 90 days (or longer)
   - Repository access: **Only select repositories** → `Tech-Tickets`
   - Permissions:
     - Repository: **Issues** → Read and write
     - Organization: **Projects** → Read and write
   - Click **"Generate token"**
   - **Copy the token** (you won't see it again!)

2. **Add token to repository secrets:**
   - Go to: https://github.com/tisa-pixel/Tech-Tickets/settings/secrets/actions
   - Click **"New repository secret"**
   - Name: `ADD_TO_PROJECT_PAT`
   - Value: Paste your token
   - Click **"Add secret"**

3. **Done!** The automation will now work for all new issues.

### Testing

After setup, test it:
```bash
gh issue create \
  --repo tisa-pixel/Tech-Tickets \
  --title "Test automation" \
  --body "This should auto-add to project board"
```

Check your project board - it should appear automatically!

## 🔗 Integration with Slack

Issues can be created from Slack and will automatically appear on your project board.

See the main project documentation: https://github.com/tisa-pixel/tech-roadmap

---

**Project Board:** https://github.com/users/tisa-pixel/projects/4

Created: October 31, 2025
