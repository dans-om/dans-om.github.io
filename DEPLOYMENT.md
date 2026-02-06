# Deployment Instructions for DANS-OM Website

This document provides step-by-step instructions for deploying the updated DANS-OM Lab website to the new GitHub repository.

## Changes Made

### Name Changes
- **Old Name**: NOME Lab (Neuroscience of Meditation Lab)
- **New Name**: DANS-OM Lab (Data-driven NeuroScience Of Meditation)

### Repository Changes
- **Old Repository**: `sidc/nomelab`
- **New Repository**: `dans-om/web`
- **Old URL**: `https://sidc.github.io/nomelab`
- **New URL**: `https://dans-om.github.io`

### Files Updated
All references to "NOME Lab" have been updated to "DANS-OM Lab" in:
- `_config.yml` - Site configuration (also cleaned up duplicate entries)
- `_layouts/default.html` - Footer text
- `_includes/navigation.html` - Navigation menu
- `index.md` - Home page content
- `news.md` - News page header
- `collaborators.md` - Collaborators page
- `dunes.md` - DUNES webinar page
- `outreach.md` - Outreach page
- `_data/news.yml` - News data file

## Deployment Steps

### 1. Initialize Git Repository

```bash
cd dans-om-website
git init
git add .
git commit -m "Initial commit: DANS-OM Lab website"
```

### 2. Connect to GitHub Repository

```bash
git remote add origin https://github.com/dans-om/web.git
git branch -M main
```

### 3. Push to GitHub

```bash
git push -u origin main
```

### 4. Enable GitHub Pages

1. Go to repository settings: `https://github.com/dans-om/web/settings`
2. Navigate to "Pages" in the left sidebar
3. Under "Source", select:
   - **Branch**: `main`
   - **Folder**: `/ (root)`
4. Click "Save"

### 5. Verify Deployment

After a few minutes, your site should be live at:
- **URL**: `https://dans-om.github.io`

You can check deployment status in the "Actions" tab of your repository.

## Post-Deployment Checklist

- [ ] Verify all pages load correctly
- [ ] Check that all navigation links work
- [ ] Test PDF downloads for publications
- [ ] Verify images display properly in gallery
- [ ] Check responsive design on mobile devices
- [ ] Test all external links (DUNES website, SLIM lab, etc.)
- [ ] Verify email links work correctly
- [ ] Confirm all NOME references have been replaced with DANS-OM

## Troubleshooting

### Site not loading after deployment
- Check that GitHub Pages is enabled in repository settings
- Verify the branch is set to `main` and folder to `/ (root)`
- Wait 5-10 minutes for initial deployment to complete

### CSS/Images not loading
- Ensure `baseurl: ""` in `_config.yml` (empty string)
- Verify `url: "https://dans-om.github.io"` in `_config.yml`
- Clear browser cache

### 404 errors on page navigation
- Confirm `permalink: pretty` is set in `_config.yml`
- Check that all `.md` files have proper front matter with `layout: default`

## Custom Domain (Optional)

If you want to use a custom domain:

1. Add a `CNAME` file to the root directory with your domain name
2. Configure DNS records with your domain provider:
   - Add an `A` record pointing to GitHub's IP addresses
   - Or add a `CNAME` record pointing to `dans-om.github.io`
3. Update `url` in `_config.yml` to your custom domain

## Contact

For technical issues with deployment, contact the lab at:
- **Email**: ravisha3@msu.edu
