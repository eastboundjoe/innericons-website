# InnerIcons Website - Deployment Guide

## GitHub Setup (Do This First)

### 1. Create GitHub Repository

1. Go to https://github.com/new
2. Repository name: `innericons-website`
3. Visibility: **Public** (or Private if you prefer)
4. **DON'T** check "Initialize with README"
5. Click "Create repository"

### 2. Push Code to GitHub

After creating the repository, run these commands in your terminal:

```bash
cd "/mnt/c/Users/Ramen Bomb/Desktop/Code/innericons-website"

# Add your GitHub repository as remote (REPLACE with your username!)
git remote add origin https://github.com/YOUR-USERNAME/innericons-website.git

# Push your code
git push -u origin main
```

**Replace `YOUR-USERNAME`** with your actual GitHub username!

Example:
```bash
git remote add origin https://github.com/eastboundjoe/innericons-website.git
git push -u origin main
```

## Vercel Deployment (Do This After GitHub Setup)

### Method 1: Connect via Vercel Dashboard (Recommended)

1. Go to https://vercel.com
2. Click **"New Project"**
3. Click **"Import Git Repository"**
4. Find `innericons-website` in your repository list
5. Click **"Import"**
6. Settings:
   - **Framework Preset**: Other
   - **Root Directory**: `./`
   - **Build Command**: (leave empty)
   - **Output Directory**: (leave empty)
7. Click **"Deploy"**

🎉 Your site will be live at `https://innericons-website.vercel.app`

### What Happens Next?

**Automatic Deployments Enabled!** 🚀

Every time you push to GitHub:
```bash
# Make changes to index.html
git add .
git commit -m "Updated hero section"
git push

# Vercel automatically detects the push and redeploys! ✅
```

You'll get:
- ✅ Automatic deployments on every push
- ✅ Preview deployments for branches
- ✅ HTTPS by default
- ✅ Global CDN (fast everywhere)
- ✅ Free hosting forever

### Add Custom Domain (Optional)

1. In Vercel project settings, go to **Domains**
2. Add `innericons.com`
3. Update your domain's DNS records as instructed
4. Wait for SSL certificate (usually < 1 hour)

## Your Workflow Going Forward

```
1. Edit code locally (VS Code, Claude Code, etc.)
   ↓
2. Test locally (open index.html in browser)
   ↓
3. Commit changes:
   git add .
   git commit -m "Description of changes"
   ↓
4. Push to GitHub:
   git push
   ↓
5. Vercel automatically rebuilds and deploys!
   (Check vercel.com for deployment status)
   ↓
6. Live site updated in ~30 seconds! ✅
```

## Useful Commands

```bash
# Check git status
git status

# See what changed
git diff

# View commit history
git log --oneline

# Push changes to GitHub (triggers Vercel deployment)
git push

# Pull latest changes from GitHub
git pull
```

## Troubleshooting

### "Permission denied" when pushing to GitHub

Use SSH instead:
```bash
git remote set-url origin git@github.com:YOUR-USERNAME/innericons-website.git
```

### Vercel deployment failed

- Check the build logs in Vercel dashboard
- Make sure `index.html` is in the root directory
- Verify `vercel.json` is valid JSON

### Changes not showing on live site

- Wait 30-60 seconds for deployment to complete
- Check Vercel dashboard for deployment status
- Hard refresh browser (Ctrl+Shift+R or Cmd+Shift+R)
- Check if deployment succeeded on Vercel

---

**Need Help?**
- GitHub Docs: https://docs.github.com
- Vercel Docs: https://vercel.com/docs
