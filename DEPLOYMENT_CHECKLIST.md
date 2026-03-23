# Portfolio Deployment Checklist

Follow these steps to deploy your portfolio to GitHub Pages.

## ✅ Pre-Deployment Checklist

- [x] README.md updated with all project details
- [x] Jekyll configuration files created (_config.yml, Gemfile)
- [x] .gitignore configured for Jekyll
- [x] All project links included
- [x] Contributions clearly described in each project section

## 🚀 Deployment Steps

### Step 1: Initialize Git (if not already done)
```powershell
cd "c:\Users\DaBr583\Documents\Personal development\Portfolio\Final-Portfolio"
git init
```

### Step 2: Add and Commit Files
```powershell
git add .
git commit -m "Initial portfolio deployment with Jekyll configuration"
```

### Step 3: Create GitHub Repository
1. Go to https://github.com/new
2. Repository name: `Final-Portfolio` (or your preferred name)
3. Description: "Software Engineering Portfolio showcasing apprenticeship projects"
4. **Public** repository (required for free GitHub Pages)
5. Do NOT initialize with README, .gitignore, or license
6. Click "Create repository"

### Step 4: Connect and Push to GitHub
Replace `YOUR-USERNAME` with your GitHub username:

```powershell
git remote add origin https://github.com/YOUR-USERNAME/Final-Portfolio.git
git branch -M main
git push -u origin main
```

### Step 5: Enable GitHub Pages
1. Go to your repository: `https://github.com/YOUR-USERNAME/Final-Portfolio`
2. Click **Settings** (top right)
3. Click **Pages** in the left sidebar
4. Under "Build and deployment":
   - **Source**: Deploy from a branch
   - **Branch**: main
   - **Folder**: / (root)
5. Click **Save**

### Step 6: Wait for Deployment
- Check the **Actions** tab to see the deployment progress
- First deployment takes 1-3 minutes
- Once complete, your site will be at: `https://YOUR-USERNAME.github.io/Final-Portfolio/`

### Step 7: Verify Deployment
- Visit your GitHub Pages URL
- Check that all projects are displayed correctly
- Verify all links work properly
- Test responsiveness on mobile

## 📝 Update Instructions

Whenever you make changes to your portfolio:

```powershell
git add .
git commit -m "Description of changes"
git push origin main
```

GitHub Pages will automatically rebuild (takes ~1 minute).

## 🎨 Customization Options

### Change Theme
Edit `_config.yml` and choose from these GitHub Pages themes:
- `jekyll-theme-cayman` (current - clean, modern)
- `jekyll-theme-minimal` (simple, sidebar)
- `jekyll-theme-slate` (dark theme)
- `jekyll-theme-midnight` (dark with hero)
- `jekyll-theme-architect` (professional)

### Update Personal Information
In `_config.yml`, update:
- `title`: Your name and title
- `description`: Brief bio
- `linkedin_username`: Your LinkedIn username

## 🔧 Troubleshooting

### Site Not Appearing
- Ensure repository is **public**
- Check Settings → Pages is enabled
- Wait 2-3 minutes for first build
- Check Actions tab for errors

### Build Failures
- Validate `_config.yml` syntax at https://www.yamllint.com/
- Check that README.md has proper markdown
- Review Actions tab for specific error messages

### Links Not Working
- Use relative paths: `./project/README.md` not `/project/README.md`
- GitHub Pages automatically converts README.md links

## 📞 Need Help?
- GitHub Pages Docs: https://docs.github.com/en/pages
- Jekyll Docs: https://jekyllrb.com/docs/
- Theme Showcase: https://pages.github.com/themes/

## ✨ Next Steps After Deployment

1. **Update README.md** with your actual GitHub Pages URL
2. **Add to LinkedIn**: Share your portfolio URL on LinkedIn
3. **Continue Building**: Add new projects as you complete them
4. **Monitor Traffic**: Enable Google Analytics in `_config.yml` (optional)
5. **Custom Domain** (optional): Purchase domain and configure DNS

---

**Current Status**: Ready to deploy! ✅

Follow Steps 1-7 above to get your portfolio live on GitHub Pages.
