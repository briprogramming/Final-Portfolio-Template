# GitHub Pages Deployment Guide

This portfolio is configured to deploy to GitHub Pages using Jekyll.

## Quick Setup

### 1. Initialize Git Repository (if not already done)
```bash
git init
git add .
git commit -m "Initial portfolio commit"
```

### 2. Create GitHub Repository
1. Go to GitHub and create a new repository named `Final-Portfolio` (or your preferred name)
2. Do NOT initialize with README (we already have one)

### 3. Push to GitHub
```bash
git remote add origin https://github.com/YOUR-USERNAME/Final-Portfolio.git
git branch -M main
git push -u origin main
```

### 4. Enable GitHub Pages
1. Go to your repository on GitHub
2. Click on **Settings**
3. Scroll down to **Pages** in the left sidebar
4. Under **Source**, select:
   - **Branch**: main
   - **Folder**: / (root)
5. Click **Save**

### 5. Wait for Deployment
- GitHub will automatically build and deploy your site
- This usually takes 1-3 minutes
- Your site will be available at: `https://YOUR-USERNAME.github.io/Final-Portfolio/`

## Custom Domain (Optional)

If you want to use a custom domain like `brianadaniels.dev`:

1. In repository Settings → Pages
2. Enter your custom domain in the "Custom domain" field
3. Configure your DNS provider:
   - Add a CNAME record pointing to `YOUR-USERNAME.github.io`
   - Or add A records pointing to GitHub's IPs

## Updating Your Portfolio

Whenever you make changes:

```bash
git add .
git commit -m "Update portfolio content"
git push origin main
```

GitHub Pages will automatically rebuild and deploy your changes.

## Customization

### Change Theme
Edit `_config.yml` and change the theme:
```yaml
theme: jekyll-theme-cayman  # or minimal, slate, modernist, etc.
```

### Update Site Information
Edit `_config.yml`:
- `title`: Your site title
- `description`: Site description for SEO
- `linkedin_username`: Your LinkedIn username
- `url`: Will be auto-set by GitHub Pages

## Troubleshooting

### Site Not Showing Up
- Check Settings → Pages to ensure it's enabled
- Make sure the branch and folder are set correctly
- Wait a few minutes for the first build

### Build Errors
- Check the Actions tab for build logs
- Ensure `_config.yml` is valid YAML syntax
- Make sure all required plugins are in the `github-pages` gem

### Links Not Working
- Use relative links in markdown: `[text](page.md)` not `[text](/page.md)`
- Ensure README.md is in the root directory

## Advanced: Local Testing

To test your site locally before deploying:

### Prerequisites
- Install Ruby (version 2.7 or higher)
- Install Bundler: `gem install bundler`

### Local Setup
```bash
# Install dependencies
bundle install

# Run local server
bundle exec jekyll serve

# View at http://localhost:4000
```

## Repository Structure

```
Final-Portfolio/
├── README.md              # Main portfolio page (deployed as index.html)
├── _config.yml            # Jekyll configuration
├── Gemfile                # Ruby dependencies
├── .gitignore             # Git ignore rules
├── DEPLOYMENT.md          # This file
├── Backend Project/       # Project folders
├── Frontend Project/
├── Deployment Project/
├── Hackathon Project/
└── Inventory Project/
```

## Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Jekyll Themes](https://pages.github.com/themes/)
- [Markdown Guide](https://www.markdownguide.org/)
