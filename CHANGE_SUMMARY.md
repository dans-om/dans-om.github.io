# DANS-OM Website Update Summary

## Overview
This document summarizes all changes made to convert the NOME Lab website to the DANS-OM Lab website.

## Repository Information

### Old
- **Repository**: `https://github.com/sidc/nomelab`
- **URL**: `https://sidc.github.io/nomelab`
- **Lab Name**: NOME Lab (Neuroscience of Meditation Lab)

### New
- **Repository**: `https://github.com/dans-om/web.git`
- **URL**: `https://dans-om.github.io`
- **Lab Name**: DANS-OM Lab (Data-driven NeuroScience Of Meditation)

## Files Modified

### Configuration Files

#### `_config.yml`
- **Updated**: Site title from "NOME Lab" to "DANS-OM Lab"
- **Updated**: Site description from "Neuroscience of Meditation Lab" to "Data-driven NeuroScience Of Meditation Lab"
- **Updated**: `baseurl` from "/nomelab" to "" (empty string for root domain)
- **Updated**: `url` from "https://sidc.github.io" to "https://dans-om.github.io"
- **Cleaned up**: Removed duplicate configuration entries
- **Result**: Clean, single configuration without redundancy

### Layout Files

#### `_layouts/default.html`
- **Line 16**: Footer text updated from "NOME Lab - Neuroscience of Meditation Lab" to "DANS-OM Lab - Data-driven NeuroScience Of Meditation"
- **Line 17**: Updated tagline from "rigorous neuroscience research" to "data-driven neuroscience research"

#### `_includes/navigation.html`
- **Line 5**: Navigation brand updated from "NOME Lab" to "DANS-OM Lab"

### Content Pages

#### `index.md` (Home Page)
- **Line 8**: Header title changed from "NOME Lab" to "DANS-OM Lab"
- **Line 9**: Header subtitle changed from "Neuroscience of Meditation Lab" to "Data-driven NeuroScience Of Meditation"
- **Line 17**: About section updated - "NOME Lab (Neuroscience of Meditation Lab)" → "DANS-OM Lab (Data-driven NeuroScience Of Meditation)"
- **Line 21**: Leadership section updated - "The NOME Lab is directed by" → "The DANS-OM Lab is directed by"
- **Line 129**: Opportunities section updated - "join the NOME Lab" → "join the DANS-OM Lab"

#### `news.md`
- **Line 9**: Page description updated from "Latest developments from the NOME Lab" to "Latest developments from the DANS-OM Lab"

#### `collaborators.md`
- **Line 16**: Updated from "The NOME Lab collaborates" to "The DANS-OM Lab collaborates"

#### `dunes.md`
- **Line 16**: Updated webinar description from "hosted by the NOME Lab" to "hosted by the DANS-OM Lab"

#### `outreach.md`
- **Line 16**: Updated from "The NOME Lab is committed" to "The DANS-OM Lab is committed"
- **Line 72**: Updated from "collaborating with the NOME Lab" to "collaborating with the DANS-OM Lab"

### Data Files

#### `_data/news.yml`
- **Line 6**: News item title updated from "NOME Lab Website Launched" to "DANS-OM Lab Website Launched"

## Files Added

1. **README.md** - New repository documentation with setup instructions
2. **DEPLOYMENT.md** - Detailed deployment guide for GitHub Pages
3. **CHANGE_SUMMARY.md** - This file documenting all changes

## Technical Notes

### Line Ending Fixes
- Converted all files from Windows line endings (CRLF) to Unix line endings (LF)
- This prevents potential issues with Jekyll builds on GitHub Pages

### Verification
- Performed comprehensive search for remaining "NOME" references
- ✅ Zero remaining "NOME Lab" references found in:
  - Markdown files (.md)
  - HTML files (.html)
  - YAML files (.yml)
  - CSS files (.css)
  - JavaScript files (.js)

## Content Preserved

The following content was **NOT** changed:
- Team member information (`_data/team.yml`)
- Publication data (`_data/publications.yml`)
- Gallery data (`_data/gallery.yml`)
- All CSS styling and color schemes
- All JavaScript functionality
- All images in `/images` directory
- All PDFs in `/pdfs` directory
- Jekyll configuration structure
- Page layouts and navigation structure

## Next Steps

1. Review the updated website files
2. Initialize git repository
3. Push to `https://github.com/dans-om/web.git`
4. Enable GitHub Pages in repository settings
5. Verify site loads at `https://dans-om.github.io`

## Verification Checklist

Before going live:
- [ ] All pages display correctly with new lab name
- [ ] Navigation menu works on all pages
- [ ] Footer displays correct lab name and description
- [ ] All internal links function properly
- [ ] PDFs and images load correctly
- [ ] External links (DUNES, SLIM lab, etc.) work
- [ ] Responsive design works on mobile/tablet
- [ ] No console errors in browser developer tools

---

**Date**: February 6, 2026  
**Updated by**: Claude (AI Assistant)  
**Status**: Ready for deployment ✅
