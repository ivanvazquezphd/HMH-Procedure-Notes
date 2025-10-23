# HMH Procedure Notes

Houston Methodist Hospital Medical Physics Procedure Documentation - Built with Jekyll for GitHub Pages

## 🌐 View the Site

**Live Site:** [https://ivanvazquezphd.github.io/HMH-Procedure-Notes/](https://ivanvazquezphd.github.io/HMH-Procedure-Notes/)

## 📋 What's Included

### Current Procedures
- ✅ **HDR Daily QA** - Complete daily quality assurance procedure with images

### Coming Soon
- HDR Prostate Planning
- HDR Cylinder Planning
- EPID IMRT QA
- TG-51 Protocol Study Notes
- And more...

## 🔄 Workflow: Obsidian → Jekyll

This site is designed to work with both:
- **Obsidian** (for editing with your existing setup)
- **Jekyll/GitHub Pages** (for web publishing)

### File Organization
```
HMH-Procedure-Notes/
├── source files/          ← Your original Obsidian files (keep editing here)
├── procedures/            ← Jekyll-converted procedures (for website)
├── notes/                 ← Jekyll-converted study notes (for website)
├── attachments/           ← Shared images (works for both!)
├── assets/css/            ← Custom styling (centers images, etc.)
└── _config.yml            ← Jekyll configuration
```

### Adding New Content

**Option 1: Quick Add (Start from Obsidian)**
1. Create/edit file in `source files/`
2. Convert to Jekyll format (see `CONVERSION-GUIDE.md`)
3. Save in `procedures/` or `notes/`
4. Update navigation in `procedures.md` or `notes.md`
5. Push to GitHub

**Option 2: Direct Jekyll**
1. Create `.md` file in `procedures/` or `notes/`
2. Add YAML frontmatter (see below)
3. Use HTML for centered images
4. Push to GitHub

### YAML Frontmatter Template
```yaml
---
layout: default
title: Procedure Name
---
```

### Image Syntax for Jekyll
```html
<p align="center">
  <img src="{{ site.baseurl }}/attachments/image-name.png" alt="Description" width="400">
</p>
```

**Note:** `{{ site.baseurl }}` ensures images work correctly with your repository name in the URL.

## 🎨 Features

✅ Professional medical documentation styling  
✅ Centered, responsive images  
✅ Clean navigation  
✅ Mobile-friendly design  
✅ Automatic deployment via GitHub Pages  
✅ Compatible with Obsidian workflow  

## 📝 Quick Reference

- **Conversion Guide:** See `CONVERSION-GUIDE.md`
- **Original Files:** `source files/` folder
- **Web Files:** `procedures/`, `notes/` folders
- **Images:** `attachments/` folder (shared)

## 🚀 Deployment

Push to GitHub → Automatic build → Live in 2-3 minutes!

No manual build steps required - Jekyll is built into GitHub Pages.

---

*Houston Methodist Medical Physics Team*