# Converting Obsidian Files to Jekyll

## Obsidian → Jekyll Syntax Conversion Guide

### Images

**Obsidian:**
```markdown
![[image-name.png|center|400]]
```

**Jekyll:**
```html
<p align="center">
  <img src="../attachments/image-name.png" alt="Description" width="400">
</p>
```

### Callouts/Admonitions

**Obsidian:**
```markdown
> [!note] Title
> Content here
```

**Jekyll:**
```markdown
> **📝 Note:** Title
> 
> Content here
```

Icons for different callout types:
- `[!note]` → **📝 Note:**
- `[!important]` → **⚠️ Important:**
- `[!warning]` → **⚠️ Warning:**
- `[!info]` → **ℹ️ Info:**
- `[!tip]` → **💡 Tip:**

### Links

**Obsidian:**
```markdown
[[Other Page]]
```

**Jekyll:**
```markdown
[Other Page](other-page.html)
```

## Quick Conversion Steps

1. Copy Obsidian markdown file
2. Convert image syntax: `![[image.png|center|400]]` → HTML `<p align="center"><img>` tags
3. Convert callouts: `> [!note]` → `> **📝 Note:**`
4. Convert internal links: `[[page]]` → `[page](page.html)`
5. Add YAML frontmatter at top:
   ```yaml
   ---
   layout: default
   title: Page Title
   ---
   ```
6. Save in appropriate folder (procedures/, notes/, etc.)

## Maintaining Both Versions

**Option 1: Keep Separate Files**
- Keep original in `source files/` for Obsidian
- Keep Jekyll version in `procedures/`, `notes/`, etc.

**Option 2: Script Conversion** (Future)
- Create a script to auto-convert from Obsidian to Jekyll format
- Keep source in Obsidian, generate Jekyll versions

## Current Setup

- Original Obsidian files: `source files/`
- Jekyll web files: `procedures/`, `notes/`, root directory
- Images: `attachments/` (shared by both)
- CSS styling: `assets/css/style.scss` (centers images automatically)
