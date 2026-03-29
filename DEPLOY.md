# Deploy to GitHub Pages

## Quick Setup (Run these commands)

```bash
# Step 1: Authenticate with GitHub
gh auth login --web

# Step 2: Create a new public repo (replace with your preferred name)
gh repo create openclaw-multiagent-report --public --source=. --remote=origin --push

# Step 3: Rename branch to gh-pages (required for GitHub Pages)
git branch -M master gh-pages
git push -u origin gh-pages --force

# Step 4: Enable GitHub Pages (via web UI or CLI)
# Go to: https://github.com/blurboy1985/openclaw-multiagent-report/settings/pages
# Or use: gh api -X POST /repos/blurboy1985/openclaw-multiagent-report/pages -f source='{"branch":"gh-pages","path":"/"}'
```

## Your Site URL

After deployment, your report will be live at:

```
https://blurboy1985.github.io/openclaw-multiagent-report/
```

## Alternative: Manual Steps

If you prefer to do it manually:

1. **Create a new repo on GitHub:**
   - Go to https://github.com/new
   - Name: `openclaw-multiagent-report`
   - Public repo
   - Don't initialize with README

2. **Push the code:**
   ```bash
   cd /home/danielquek/.openclaw/workspace/github-pages
   git remote add origin git@github.com:blurboy1985/openclaw-multiagent-report.git
   git branch -M master gh-pages
   git push -u origin gh-pages
   ```

3. **Enable GitHub Pages:**
   - Go to repo Settings → Pages
   - Source: Deploy from branch
   - Branch: gh-pages
   - Folder: / (root)
   - Save

4. **Wait 1-2 minutes** for GitHub to build and deploy

## Verify Deployment

Check status at: `https://github.com/blurboy1985/openclaw-multiagent-report/deployments`

Your site will be live at: `https://blurboy1985.github.io/openclaw-multiagent-report/`

---

**Note:** The HTML file is self-contained (no external dependencies), so it will work perfectly on GitHub Pages!
