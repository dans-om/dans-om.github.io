# Quick Start Guide - DANS-OM Website

This is a quick reference for deploying and managing the DANS-OM Lab website.

## 🚀 Deploy to GitHub (First Time)

```bash
# 1. Navigate to the website directory
cd dans-om-website

# 2. Initialize git
git init

# 3. Add all files
git add .

# 4. Create initial commit
git commit -m "Initial commit: DANS-OM Lab website"

# 5. Connect to GitHub repository
git remote add origin https://github.com/dans-om/web.git

# 6. Set main branch
git branch -M main

# 7. Push to GitHub
git push -u origin main
```

## ⚙️ Enable GitHub Pages

1. Go to: `https://github.com/dans-om/web/settings/pages`
2. Under "Source": Select `main` branch and `/ (root)` folder
3. Click "Save"
4. Wait 2-5 minutes for deployment
5. Visit: `https://dans-om.github.io`

## 📝 Making Updates

### Update Team Members
Edit `_data/team.yml`:
```yaml
- name: New Member Name
  role: Position
  department: Department, Institution
  category: Lab Member  # or "Advisor"
```

### Add News Item
Edit `_data/news.yml`:
```yaml
- date: "Month Year"
  title: "News Title"
  description: "Description of the news."
```

### Add Publication
Edit `_data/publications.yml`:
```yaml
- authors: Author names
  year: "2026"
  title: "Paper title"
  venue: Conference/Journal name
  link: "https://..."
  pdf: "/pdfs/filename.pdf"
```

### Add Gallery Image
1. Place image in `/images/` folder
2. Edit `_data/gallery.yml`:
```yaml
- image: /images/filename.jpg
  title: "Image Title"
  description: "Image description"
```

## 🔄 Push Changes

```bash
# 1. Check what changed
git status

# 2. Add changes
git add .

# 3. Commit with message
git commit -m "Description of changes"

# 4. Push to GitHub
git push
```

Changes will be live in 1-2 minutes!

## 🧪 Test Locally

```bash
# Install dependencies (first time only)
bundle install

# Start local server
bundle exec jekyll serve

# Open browser to:
# http://localhost:4000
```

## 📧 Contact Information

Current site email: `ravisha3@msu.edu`

To update, change the `email` field in `_config.yml`

## 🎨 Color Scheme

Primary colors used:
- **Green**: `#18453B` (main brand color)
- **Orange**: `#ff6600` (accent/CTA color)
- **Gray**: `#f8f9fa` (backgrounds)

To change, edit `assets/css/style.css`

## 📂 Key Files

- **`_config.yml`** - Main site configuration
- **`index.md`** - Home page content
- **`_includes/navigation.html`** - Navigation menu
- **`_layouts/default.html`** - Page template
- **`_data/*.yml`** - Data files for team, news, publications, gallery

## ❓ Need Help?

See full documentation:
- **README.md** - Complete overview
- **DEPLOYMENT.md** - Detailed deployment guide
- **CHANGE_SUMMARY.md** - What was changed from NOME to DANS-OM

## ✅ Checklist After First Deployment

- [ ] Site loads at https://dans-om.github.io
- [ ] All navigation links work
- [ ] Team members display correctly
- [ ] Publications show with PDFs
- [ ] Images load in gallery
- [ ] Email links work
- [ ] Mobile view looks good

---

**Website**: https://dans-om.github.io  
**Repository**: https://github.com/dans-om/web  
**Lab**: DANS-OM Lab @ Michigan State University
