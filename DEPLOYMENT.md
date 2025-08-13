# GitHub Pages Deployment Manual for Centro-Aceros

## Overview

This manual provides step-by-step instructions for deploying the Agricultural Market Pulse Dashboard to GitHub Pages for seamless hosting and sharing.

## Prerequisites

- GitHub account with repository access
- Repository: `araceaeofcol/Centro-Aceros`
- Basic understanding of Git and GitHub

## Deployment Options

### Option 1: Automatic Deployment (Recommended)

#### Step 1: Enable GitHub Pages

1. **Navigate to Repository Settings**
   - Go to https://github.com/araceaeofcol/Centro-Aceros
   - Click on the "Settings" tab (requires admin/write access)

2. **Configure GitHub Pages**
   - Scroll down to the "Pages" section in the left sidebar
   - Under "Source", select "Deploy from a branch"
   - Choose your branch (typically `main` or `master`)
   - Select "/ (root)" as the folder
   - Click "Save"

3. **Verify Deployment**
   - GitHub will show a green checkmark when deployment is successful
   - Your site will be available at: `https://araceaeofcol.github.io/Centro-Aceros/`
   - Initial deployment may take 5-10 minutes

#### Step 2: Access Your Live Site

Visit: **https://araceaeofcol.github.io/Centro-Aceros/**

### Option 2: GitHub Actions Workflow (Advanced)

For automated deployments with every code change:

1. **Create Workflow Directory**
   ```bash
   mkdir -p .github/workflows
   ```

2. **Create Deployment Workflow**
   - File: `.github/workflows/deploy.yml`
   - This enables automatic deployment on every push to main branch

3. **Push Changes**
   ```bash
   git add .
   git commit -m "Add GitHub Actions deployment workflow"
   git push origin main
   ```

## File Structure Requirements

For GitHub Pages to work correctly, ensure:

```
Centro-Aceros/
├── index.html          # ✅ Main entry point (required)
├── README.md          # ✅ Documentation
└── .github/           # Optional: GitHub Actions
    └── workflows/
        └── deploy.yml
```

## Verification Steps

### 1. Check File Naming
- ✅ Main file is named `index.html` (not `app.html`)
- ✅ File is in the root directory

### 2. Test Locally (Optional)

**Using Python:**
```bash
cd Centro-Aceros
python -m http.server 8000
# Visit: http://localhost:8000
```

**Using Node.js:**
```bash
cd Centro-Aceros
npx serve .
# Visit: http://localhost:5000
```

### 3. Verify GitHub Pages Status

1. Go to repository Settings → Pages
2. Look for green checkmark: "Your site is published at..."
3. Check deployment status in the "Actions" tab

## Troubleshooting Guide

### Common Issues and Solutions

#### Issue: "404 - Page Not Found"
**Solution:**
- Verify `index.html` exists in root directory
- Check GitHub Pages is enabled in Settings
- Ensure repository is public (for free GitHub Pages)

#### Issue: "Site not updating"
**Solution:**
- GitHub Pages cache: Wait 5-10 minutes for changes
- Hard refresh browser: Ctrl+F5 (Windows) or Cmd+Shift+R (Mac)
- Check Actions tab for deployment failures

#### Issue: "Charts not loading"
**Solution:**
- The app includes fallback SVG charts for offline use
- Enable JavaScript in your browser
- Check browser console for errors

#### Issue: "HTTPS certificate errors"
**Solution:**
- GitHub Pages automatically provides HTTPS
- Wait for certificate provisioning (up to 24 hours for new domains)

## Advanced Configuration

### Custom Domain (Optional)

1. **Add CNAME file**
   ```bash
   echo "yourdomain.com" > CNAME
   git add CNAME
   git commit -m "Add custom domain"
   git push
   ```

2. **Configure DNS**
   - Point your domain's A record to GitHub Pages IPs
   - Or use CNAME record pointing to: `araceaeofcol.github.io`

3. **Enable in Settings**
   - Go to Settings → Pages
   - Enter your custom domain
   - Enable "Enforce HTTPS"

### Security Headers (Optional)

Add security headers by creating `.github/workflows/deploy.yml` with custom configurations.

## Monitoring and Maintenance

### Check Site Status
- **Live Site**: https://araceaeofcol.github.io/Centro-Aceros/
- **Repository**: https://github.com/araceaeofcol/Centro-Aceros
- **Actions**: https://github.com/araceaeofcol/Centro-Aceros/actions

### Performance Optimization
- The app is already optimized with:
  - CDN-loaded dependencies
  - Responsive design
  - Efficient chart rendering
  - Offline fallbacks

### Analytics (Optional)
Add Google Analytics or other tracking by modifying the HTML head section.

## Quick Reference Commands

```bash
# Clone repository
git clone https://github.com/araceaeofcol/Centro-Aceros.git

# Navigate to project
cd Centro-Aceros

# Test locally
python -m http.server 8000

# Make changes and deploy
git add .
git commit -m "Update dashboard"
git push origin main
```

## Support and Resources

- **GitHub Pages Documentation**: https://docs.github.com/en/pages
- **Repository Issues**: https://github.com/araceaeofcol/Centro-Aceros/issues
- **GitHub Community**: https://github.community/

## Success Checklist

- [ ] Repository contains `index.html` in root directory
- [ ] GitHub Pages enabled in repository settings
- [ ] Site accessible at `https://araceaeofcol.github.io/Centro-Aceros/`
- [ ] Charts and interactions working correctly
- [ ] Data tables filtering properly
- [ ] Download functionality operational
- [ ] Responsive design working on mobile devices

---

**🎉 Congratulations! Your Agricultural Market Pulse Dashboard is now live on GitHub Pages!**