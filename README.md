# Hudsonville Ice Cream - Loyalty Program Campaign Microsite

A campaign microsite replicating the Hudsonville Ice Cream brand identity for their loyalty program launch.

---

## 📁 Project Structure

```
Hudsonville/
├── README.md                          # This file
├── BRAND_GUIDE.md                     # Complete brand design system
├── font-demo.html                     # Typography demonstration page
│
├── assets/
│   ├── ASSETS_INVENTORY.md            # Asset catalog and usage guide
│   │
│   ├── logos/
│   │   ├── hudsonville-logo-navy.jpg  # Primary logo (light backgrounds)
│   │   └── hudsonville-logo-white.svg # Logo for dark backgrounds
│   │
│   ├── products/
│   │   ├── ice-cream-mackinac-island-fudge.png
│   │   ├── ice-cream-bars.png
│   │   ├── limited-edition-tropical-twist.png
│   │   ├── new-flavors-mint-deer-traxx.png
│   │   ├── extra-indulgent-pints.png
│   │   └── little-debbie-collaboration.png
│   │
│   └── fonts/
│       ├── FONTS_SETUP.md             # Font implementation guide
│       └── Lesley.woff                # Script accent font
```

---

## 🎨 Brand Identity

### Colors
- **Primary Navy**: `#102250` - Main brand color
- **Light Blue**: `#4495d2` - Hover states & accents
- **White**: `#ffffff` - Backgrounds
- **Black**: `#000000` - Body text

### Typography
- **Headlines/CTAs**: Bebas Neue (via Google Fonts)
- **Script Accent**: Lesley (self-hosted) - for emphasis words like "Real"
- **Body Text**: System sans-serif stack

### Key Design Element
Headlines use a **two-font approach**:
```html
<h1>EXPERIENCE <span class="script-accent">Real</span> PREMIUM ICE CREAM</h1>
```
- Uppercase Bebas Neue for structure
- Script Lesley font for emphasis words

---

## 🚀 Quick Start

### 1. View Font Demo
Open `font-demo.html` in a browser to see:
- Typography system in action
- Color palette swatches
- Button styles and hover states
- Headline variations with script accents
- Campaign layout examples

### 2. Review Brand Guide
See [BRAND_GUIDE.md](BRAND_GUIDE.md) for:
- Complete design system
- CSS custom properties
- Component styles
- Spacing system
- Implementation examples

### 3. Font Setup
See [assets/fonts/FONTS_SETUP.md](assets/fonts/FONTS_SETUP.md) for:
- Font loading instructions
- @font-face declarations
- Usage patterns
- Alternative font options

---

## 📋 Documentation

| Document | Purpose |
|----------|---------|
| [BRAND_GUIDE.md](BRAND_GUIDE.md) | Complete brand design system |
| [assets/ASSETS_INVENTORY.md](assets/ASSETS_INVENTORY.md) | All downloaded assets with details |
| [assets/fonts/FONTS_SETUP.md](assets/fonts/FONTS_SETUP.md) | Typography implementation guide |
| [font-demo.html](font-demo.html) | Live typography demonstration |

---

## 🔧 Implementation Guide

### HTML Template Starter
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hudsonville Loyalty Program</title>

  <!-- Google Fonts - Bebas Neue -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap" rel="stylesheet">

  <style>
    /* Lesley Script Font */
    @font-face {
      font-family: 'Lesley';
      src: url('assets/fonts/Lesley.woff') format('woff');
      font-display: swap;
    }

    :root {
      --font-heading: 'Bebas Neue', sans-serif;
      --font-script: 'Lesley', cursive;
      --font-body: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
      --color-primary: #102250;
      --color-secondary: #4495d2;
    }

    body {
      font-family: var(--font-body);
      margin: 0;
      padding: 0;
    }

    h1, h2, h3 {
      font-family: var(--font-heading);
      text-transform: uppercase;
      letter-spacing: 1px;
    }

    .script-accent {
      font-family: var(--font-script);
      text-transform: none;
      letter-spacing: 0;
    }

    .btn {
      font-family: var(--font-heading);
      text-transform: uppercase;
      letter-spacing: 1px;
      background: var(--color-primary);
      color: white;
      padding: 10px 30px;
      border-radius: 100px;
      border: none;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }

    .btn:hover {
      background: var(--color-secondary);
      color: var(--color-primary);
    }
  </style>
</head>
<body>
  <!-- Your content here -->
</body>
</html>
```

---

## ✨ Design Features

### Buttons
- Pill-shaped (100px border-radius)
- Navy background, white text
- Hover: Light blue background, navy text
- Uppercase Bebas Neue font

### Headlines
- Bebas Neue uppercase with 1px letter-spacing
- Script accent (Lesley) for emphasis words
- Three size options: 42px, 36px, 20px

### Product Cards
- Clean grid layout
- High-quality product imagery
- Consistent spacing and shadows

---

## 🎯 Next Steps

1. **Add Campaign Content**: Ready to integrate loyalty program copy and CTAs
2. **Build Pages**: Create landing page, sign-up forms, rewards pages
3. **Responsive Design**: Already mobile-ready at 786px breakpoint
4. **Testing**: Verify fonts load correctly across browsers

---

## 📦 Assets Summary

- **2** Logo files (navy JPG, white SVG)
- **6** Product images (PNG format)
- **1** Custom font (Lesley.woff)
- **100%** Brand-accurate color palette
- **Full** design system documentation

---

## 🔗 Source

All assets and styling extracted from: https://www.hudsonvilleicecream.com/

**Brand Heritage**: Since 1926

---

## 💡 Key Brand Messages

- **"Real"** - Authentic ingredients (emphasized with script font)
- **Premium Quality** - Expert craftsmanship
- **Approachable** - Modern, friendly design
- **Heritage** - Trust and tradition since 1926

---

## 📞 Support

For questions about implementation or brand guidelines, refer to:
- [BRAND_GUIDE.md](BRAND_GUIDE.md) - Design decisions
- [assets/fonts/FONTS_SETUP.md](assets/fonts/FONTS_SETUP.md) - Font troubleshooting
- [font-demo.html](font-demo.html) - Visual reference

---

*Created: 2025-10-24*
*Ready for campaign content integration*
