# Quick Start Guide

**For resuming development on the Hudsonville x Perk microsite**

---

## Current Status

✅ **Live Site:** https://hudsonville.perk.ooo/
✅ **Repository:** https://github.com/tgauss/hudsonville-perk-microsite
✅ **Last Updated:** October 28, 2025
✅ **Production Ready:** Yes

---

## Get Started in 3 Steps

### 1. Open the Project
```bash
cd "/Users/tgauss/Projects/Claude Code/Hudsonville"
code .  # Or open in your preferred editor
```

### 2. View Locally
```bash
# Option A: Double-click index.html
open index.html

# Option B: Run local server
python3 -m http.server 8000
# Then visit http://localhost:8000
```

### 3. Deploy Changes
```bash
git add .
git commit -m "Your change description"
git push

# Vercel auto-deploys in 1-2 minutes
```

---

## Key Files to Know

| File | Purpose |
|------|---------|
| `index.html` | Main microsite (edit this for content changes) |
| `DEVELOPMENT_NOTES.md` | Complete session history and technical details |
| `BRAND_GUIDE.md` | Design system and brand colors |
| `assets/` | All images, logos, fonts |
| `.vercelignore` | Files excluded from deployment |

---

## Brand Colors (Use These!)

```css
Navy:       #102250  /* Headers, backgrounds */
Light Blue: #4495d2  /* Accents, highlights, CTAs */
White:      #FFFFFF  /* Text on dark backgrounds */
Cream:      #e8e4de  /* Section backgrounds */
```

**⚠️ Important:** Do NOT use gold/yellow (#FFD700) - we replaced it with light blue

---

## Common Tasks

### Update Content
1. Open `index.html`
2. Find section using comments (e.g., `<!-- Hero -->`)
3. Edit text/HTML
4. Save and test locally
5. Commit and push

### Add New Section
1. Copy existing section structure
2. Maintain responsive grid classes
3. Use brand colors from variables
4. Test on mobile (resize browser)

### Fix Mobile Issues
- Check breakpoints: 786px, 650px, 480px
- Use responsive grid classes (`.ocr-grid`, `.multiplier-grid`)
- Test in browser dev tools mobile view

### Update Contact Info
- Footer section (line ~2360)
- Email: joe@perksocial.com
- Phone: (614) 668-8884

---

## Fonts

**Bebas Neue** (Headings)
```html
<!-- Already loaded via Google Fonts -->
<h1>UPPERCASE HEADING</h1>
```

**Lesley** (Script accents)
```html
<!-- Use for emphasis words -->
<span class="script-accent">Scoop</span>
```

---

## Responsive Design

The site adapts at these breakpoints:

- **Desktop (1200px+):** Full 2-3 column layouts
- **Tablet (786-1200px):** Adjusted columns
- **Mobile (480-786px):** Single column, larger touch targets
- **Small (< 480px):** Reduced font sizes

**Test locally:** Resize browser or use Chrome DevTools

---

## Current Sections (In Order)

1. Header (sticky nav)
2. **Hero** - Gradient background, dual CTAs
3. Why It Matters
4. How It Works
5. **OCR Demo** - Receipt → JSON transformation
6. **Customer Profile** (Light Blue section)
7. Activity Ledger (timeline)
8. Data Tabs (interactive)
9. Activation Playbook
10. **M&M'S Case Study** (10 proven results)
11. **CTA** - Final contact section
12. Footer

---

## Need Help?

- **Full Documentation:** See [DEVELOPMENT_NOTES.md](DEVELOPMENT_NOTES.md)
- **Brand Guidelines:** See [BRAND_GUIDE.md](BRAND_GUIDE.md)
- **Contact Info:** joe@perksocial.com | (614) 668-8884

---

## Quick Commands

```bash
# View git history
git log --oneline -10

# Check what changed
git status

# See live site
open https://hudsonville.perk.ooo

# Deploy to production
git push
```

---

**Ready to continue? Open index.html and start editing!**
