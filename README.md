# HMH Procedure Notes Documentation

This repository contains the Houston Methodist Hospital Medical Physics Procedure Documentation, built with MkDocs and Material theme for GitHub Pages.

## 🚀 Quick Start

### Local Development

1. **Install Python dependencies:**
   ```bash
   pip install mkdocs-material
   ```

2. **Start the local development server:**
   ```bash
   mkdocs serve
   ```

3. **View the documentation:**
   Open your browser to `http://127.0.0.1:8000`

### Building the Site

To build the static site:
```bash
mkdocs build
```

The built site will be in the `site/` directory.

## 📁 Project Structure

```
HMH-Procedure-Notes/
├── docs/                          # Documentation source files
│   ├── index.md                   # Homepage
│   ├── procedures/                 # Procedure documentation
│   │   ├── hdr-prostate-planning.md
│   │   ├── hdr-cylinder-planning.md
│   │   ├── hdr-tandem-ring-planning.md
│   │   ├── hdr-daily-qa.md
│   │   ├── epid-imrt-qa-procedure.md
│   │   ├── exporting-anonymizing-data.md
│   │   ├── importing-exporting-imaging-data.md
│   │   └── resident-exercises.md
│   ├── notes/                     # Study notes
│   │   ├── tg-51-protocol-study-notes.md
│   │   └── daily-qa-incomplete.md
│   ├── technical/                  # Technical documentation
│   │   ├── film-qa.md
│   │   ├── winston-lutz.md
│   │   └── inverse-planning-prostate-hdr-brachytherapy.md
│   └── resources/                  # Resource documentation
│       ├── female-rtog-normal-pelvis-atlas.md
│       ├── modusqa-product-brochure.md
│       └── tilt-plate-users-guide.md
├── attachments/                    # Image attachments
├── resources/                      # PDF resources
├── mkdocs.yml                      # MkDocs configuration
├── requirements.txt                # Python dependencies
├── .github/workflows/docs.yml      # GitHub Actions workflow
└── README.md                       # This file
```

## 🔧 Configuration

The site is configured in `mkdocs.yml` with:

- **Material theme** with professional medical documentation styling
- **Navigation tabs** for easy browsing
- **Search functionality** for finding specific procedures
- **Code syntax highlighting** for technical content
- **Responsive design** that works on all devices

## 🌐 GitHub Pages Deployment

The site automatically deploys to GitHub Pages when you push to the main branch. The deployment is handled by GitHub Actions (`.github/workflows/docs.yml`).

### Setting up GitHub Pages:

1. **Create a GitHub repository** with this code
2. **Update the repository URLs** in `mkdocs.yml`:
   ```yaml
   site_url: https://yourusername.github.io/HMH-Procedure-Notes/
   repo_name: yourusername/HMH-Procedure-Notes
   repo_url: https://github.com/yourusername/HMH-Procedure-Notes
   ```
3. **Enable GitHub Pages** in repository settings:
   - Go to Settings → Pages
   - Source: GitHub Actions
4. **Push to main branch** - the site will automatically deploy

## 📝 Adding Content

### Adding New Procedures

1. Create a new markdown file in `docs/procedures/`
2. Add it to the navigation in `mkdocs.yml`
3. Use the existing procedure files as templates

### Adding Images

1. Place images in the `attachments/` directory
2. Reference them in markdown using:
   ```markdown
   ![Alt text](attachments/image-name.png)
   ```

### Adding Resources

1. Place PDF files in the `resources/` directory
2. Create a corresponding markdown file in `docs/resources/`
3. Add it to the navigation in `mkdocs.yml`

## 🎨 Customization

### Theme Colors
Edit the `palette` section in `mkdocs.yml` to change colors.

### Navigation
Modify the `nav` section in `mkdocs.yml` to reorganize the menu structure.

### Extensions
Add or remove markdown extensions in the `markdown_extensions` section.

## 📚 Features

- **Professional medical documentation** styling
- **Responsive design** for mobile and desktop
- **Search functionality** across all content
- **Code syntax highlighting** for technical procedures
- **Automatic deployment** to GitHub Pages
- **Version control** integration
- **PDF resource management**

## 🤝 Contributing

1. Make changes to markdown files in the `docs/` directory
2. Test locally with `mkdocs serve`
3. Commit and push changes
4. The site will automatically update on GitHub Pages

## 📞 Support

For questions about this documentation system, contact the Houston Methodist Medical Physics team.

---

*Built with ❤️ using MkDocs and Material theme*
