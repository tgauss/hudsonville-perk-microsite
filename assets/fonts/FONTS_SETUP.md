# Hudsonville Fonts Setup Guide
## Replicating Typography for Campaign Microsite

---

## Primary Font: Bebas Neue Pro

The Hudsonville website uses **Bebas Neue Pro** for headings, buttons, and CTAs.

### About Bebas Neue Pro
- **Type**: Sans-serif display font
- **Style**: Condensed, uppercase-optimized
- **Usage**: Headings, buttons, CTAs, navigation
- **License**: Commercial font (requires purchase/license)

---

## Accent Font: Lesley Script ✨

Hudsonville uses **Lesley** (script/handwritten font) for emphasis on key words like "Real" in headlines.

### About Lesley
- **Type**: Script/Handwritten font
- **Style**: Elegant, flowing script
- **Usage**: Accent words in headlines (e.g., "Experience _Real_ Premium Ice Cream")
- **Implementation**: Self-hosted WOFF file included

### @font-face Declaration
```css
@font-face {
  font-family: 'Lesley';
  src: url('../fonts/Lesley.woff') format('woff');
  font-weight: normal;
  font-style: normal;
  font-display: swap;
}
```

### Usage Pattern
Use for emphasizing key brand words within headlines:

```html
<h1>EXPERIENCE <span class="script-accent">Real</span> PREMIUM ICE CREAM</h1>
<h2>MADE BETTER BY ICE CREAM EXPERTS</h2>
```

```css
.script-accent {
  font-family: 'Lesley', cursive;
  text-transform: none; /* Remove uppercase for script font */
  font-style: normal;
  letter-spacing: 0; /* Reset letter-spacing for natural script flow */
}
```

---

## Implementation Options

### Option 1: Bebas Neue (Free - Google Fonts) ⭐ RECOMMENDED

The free "Bebas Neue" font from Google Fonts is nearly identical to Bebas Neue Pro for most use cases.

#### HTML Implementation
```html
<!-- Add to <head> section -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap" rel="stylesheet">
```

#### CSS Implementation
```css
:root {
  --font-heading: 'Bebas Neue', sans-serif;
  --font-body: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, sans-serif;
}

h1, h2, h3, h4, h5, h6,
.btn,
.cta,
nav a {
  font-family: var(--font-heading);
  text-transform: uppercase;
  letter-spacing: 1px;
}

body {
  font-family: var(--font-body);
}
```

---

### Option 2: Bebas Neue Pro (Premium - Exact Match)

For exact brand matching, license the professional version.

#### Where to Purchase
- **MyFonts**: https://www.myfonts.com/collections/bebas-neue-pro-font-dharma-type
- **Adobe Fonts**: May be included with Adobe Creative Cloud subscription
- **Font Squirrel**: Check for web font license

#### Self-Hosted Implementation
Once you have the font files (WOFF2, WOFF, TTF):

```css
@font-face {
  font-family: 'Bebas Neue Pro';
  src: url('../fonts/BebasNeuePro-Regular.woff2') format('woff2'),
       url('../fonts/BebasNeuePro-Regular.woff') format('woff');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: 'Bebas Neue Pro';
  src: url('../fonts/BebasNeuePro-Bold.woff2') format('woff2'),
       url('../fonts/BebasNeuePro-Bold.woff') format('woff');
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}

:root {
  --font-heading: 'Bebas Neue Pro', 'Bebas Neue', sans-serif;
}
```

#### Adobe Fonts (Typekit) Implementation
If available through Adobe subscription:

```html
<!-- Add to <head> -->
<link rel="stylesheet" href="https://use.typekit.net/[your-kit-id].css">
```

```css
:root {
  --font-heading: 'bebas-neue-pro', sans-serif;
}
```

---

### Option 3: System Fallback Stack

If fonts aren't loading, ensure graceful degradation:

```css
:root {
  --font-heading: 'Bebas Neue Pro', 'Bebas Neue', 'Arial Narrow', 'Arial', 'Helvetica Neue', sans-serif;
  --font-body: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
}
```

---

## Complete Typography System

### Full CSS Setup (Using Google Fonts - Recommended)

```css
/* Import Bebas Neue from Google Fonts */
@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap');

/* Load Lesley Script Font (Self-Hosted) */
@font-face {
  font-family: 'Lesley';
  src: url('../fonts/Lesley.woff') format('woff');
  font-weight: normal;
  font-style: normal;
  font-display: swap;
}

/* Root Variables */
:root {
  /* Typography */
  --font-heading: 'Bebas Neue', sans-serif;
  --font-script: 'Lesley', cursive;
  --font-body: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;

  /* Font Sizes (from Hudsonville) */
  --font-size-small: 13px;
  --font-size-medium: 20px;
  --font-size-large: 36px;
  --font-size-xlarge: 42px;

  /* Letter Spacing */
  --letter-spacing-wide: 1px;
}

/* Base Typography */
body {
  font-family: var(--font-body);
  font-size: 16px;
  line-height: 1.6;
  color: #000000;
}

/* Headings */
h1, h2, h3, h4, h5, h6 {
  font-family: var(--font-heading);
  text-transform: uppercase;
  letter-spacing: var(--letter-spacing-wide);
  font-weight: 400; /* Bebas Neue is naturally bold-looking */
  line-height: 1.2;
}

h1 {
  font-size: var(--font-size-xlarge);
}

h2 {
  font-size: var(--font-size-large);
}

h3 {
  font-size: var(--font-size-medium);
}

/* Buttons and CTAs */
.btn,
button,
.cta {
  font-family: var(--font-heading);
  text-transform: uppercase;
  letter-spacing: var(--letter-spacing-wide);
  font-size: var(--font-size-medium);
}

/* Navigation */
nav a,
.nav-link {
  font-family: var(--font-heading);
  text-transform: uppercase;
  letter-spacing: var(--letter-spacing-wide);
}

/* Script Accent - "Real" and Key Brand Words */
.script-accent,
.real-accent {
  font-family: var(--font-script);
  text-transform: none;
  letter-spacing: 0;
  font-style: normal;
}

/* Emphasized Text */
em, .emphasis {
  font-style: italic;
}
```

---

## Performance Optimization

### Font Loading Strategy

```html
<!-- Preconnect to Google Fonts for faster loading -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<!-- Load font with display=swap to prevent FOIT (Flash of Invisible Text) -->
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap" rel="stylesheet">
```

### CSS Font Display Property
```css
@font-face {
  font-family: 'Bebas Neue Pro';
  src: url('../fonts/BebasNeuePro-Regular.woff2') format('woff2');
  font-display: swap; /* Show fallback font while loading */
}
```

---

## Testing Font Accuracy

### Visual Comparison Checklist
- [ ] Uppercase letters appear condensed and bold
- [ ] Letter spacing matches (1px)
- [ ] Buttons have proper font weight
- [ ] Headings maintain hierarchy
- [ ] Mobile rendering is consistent

### Differences: Bebas Neue vs Bebas Neue Pro
- **Pro version**: Slightly more refined letterforms, better kerning
- **Free version**: Nearly identical for digital/screen use
- **Recommendation**: Use free version unless client specifically requires Pro

---

## Quick Start HTML Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hudsonville Loyalty Campaign</title>

  <!-- Google Fonts - Bebas Neue -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap" rel="stylesheet">

  <style>
    /* Lesley Script Font */
    @font-face {
      font-family: 'Lesley';
      src: url('assets/fonts/Lesley.woff') format('woff');
      font-weight: normal;
      font-style: normal;
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

    h1, h2, h3, .btn {
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
  <header>
    <img src="assets/logos/hudsonville-logo-navy.jpg" alt="Hudsonville Ice Cream">
    <h1>EXPERIENCE <span class="script-accent">Real</span> PREMIUM ICE CREAM</h1>
    <button class="btn">Sign Up Today</button>
  </header>
</body>
</html>
```

---

## Recommended Approach for Campaign Microsite

### ✅ Use Bebas Neue (Free from Google Fonts)

**Reasons:**
1. **99% visual match** to Bebas Neue Pro for screen use
2. **Free and legal** to use
3. **Fast CDN delivery** from Google
4. **No licensing concerns** for campaign use
5. **Easy implementation** - single line of code

### Implementation Steps:
1. Add Google Fonts link to HTML `<head>`
2. Apply font-family to headings and buttons
3. Add uppercase transform and letter-spacing
4. Test across devices

---

## File Structure

```
assets/
├── fonts/
│   ├── FONTS_SETUP.md (this file)
│   ├── Lesley.woff ✅ (Included - Script accent font)
│   └── [Optional: Bebas Neue Pro - if using Pro version]
│       ├── BebasNeuePro-Regular.woff2
│       ├── BebasNeuePro-Regular.woff
│       ├── BebasNeuePro-Bold.woff2
│       └── BebasNeuePro-Bold.woff
```

---

## Additional Resources

- **Google Fonts - Bebas Neue**: https://fonts.google.com/specimen/Bebas+Neue
- **Bebas Neue Pro (Purchase)**: https://www.myfonts.com/collections/bebas-neue-pro-font-dharma-type
- **Font Pairing Guide**: Bebas Neue + System Sans-serif (Roboto, San Francisco, Segoe UI)

---

*Last Updated: 2025-10-24*
*Recommended: Use Bebas Neue from Google Fonts*
