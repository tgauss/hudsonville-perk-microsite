# Hudsonville Ice Cream - Brand Guide
## Campaign Microsite Design System

This guide documents the brand identity, design elements, and styling from hudsonvilleicecream.com for use in the loyalty program campaign microsite.

---

## Color Palette

### Primary Colors
```css
--primary-navy: #102250;        /* Main brand color - buttons, headers */
--primary-blue: #4495d2;        /* Hover states, accents */
--primary-white: #ffffff;       /* Backgrounds, text on dark */
--primary-black: #000000;       /* Body text */
```

### Usage Guidelines
- **Navy (#102250)**: Primary CTAs, navigation, key brand moments
- **Light Blue (#4495d2)**: Hover states, interactive elements
- **White (#ffffff)**: Primary backgrounds, text on dark backgrounds
- **Black (#000000)**: Body copy, primary content text

---

## Typography

### Font Families
```css
--font-primary: 'bebas-neue-pro', sans-serif;  /* Headings, CTAs */
--font-script: 'Lesley', cursive;              /* Script accent for "Real" */
--font-body: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
```

### Font Files
- **Bebas Neue**: Google Fonts (free alternative to Bebas Neue Pro)
- **Lesley**: Self-hosted WOFF file (`assets/fonts/Lesley.woff`) ✅ Included

### Font Sizes
```css
--font-size-small: 13px;
--font-size-medium: 20px;
--font-size-large: 36px;
--font-size-xlarge: 42px;
```

### Typography Treatments
- **Headings**: Bebas Neue Pro, uppercase, letter-spacing: 1px
- **Script Accents**: Lesley font for emphasis words (e.g., "Real" in "EXPERIENCE Real PREMIUM ICE CREAM")
- **CTAs/Buttons**: Bebas Neue Pro, uppercase, letter-spacing: 1px
- **Body Text**: System sans-serif stack

### Script Accent Usage Pattern
The Lesley script font is used to emphasize key brand words within headlines:

```html
<h1>EXPERIENCE <span class="script-accent">Real</span> PREMIUM ICE CREAM</h1>
```

```css
.script-accent {
  font-family: 'Lesley', cursive;
  text-transform: none;  /* Keep natural script capitalization */
  letter-spacing: 0;     /* Natural script flow */
}
```

---

## Spacing System

### CSS Custom Properties
```css
--space-20: 0.44rem;   /* ~7px */
--space-30: 0.67rem;   /* ~10px */
--space-40: 1rem;      /* 16px */
--space-50: 1.5rem;    /* 24px */
--space-60: 2.25rem;   /* 36px */
--space-70: 3.38rem;   /* ~54px */
--space-80: 5.06rem;   /* ~81px */
```

### Common Spacing Patterns
- **Button padding**: 10px 30px
- **Side margins (mobile)**: 25px
- **Flex/grid gap**: 0.5em (8px)
- **Column gap**: 2em (32px)

---

## Components

### Buttons

#### Primary Button (CTA)
```css
.btn-primary {
  background-color: #102250;
  color: #ffffff;
  text-transform: uppercase;
  letter-spacing: 1px;
  padding: 10px 30px;
  border-radius: 100px;
  font-family: 'bebas-neue-pro', sans-serif;
  border: none;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.btn-primary:hover {
  background-color: #4495d2;
  color: #102250;
}
```

#### Block Button
```css
.btn-block {
  border-radius: 9999px;
  /* Same styling as primary */
}
```

---

## Shadows

### Predefined Shadow Styles
```css
--shadow-natural: 6px 6px 9px rgba(0, 0, 0, 0.2);
--shadow-deep: 12px 12px 50px rgba(0, 0, 0, 0.4);
--shadow-sharp: 6px 6px 0px rgba(0, 0, 0, 0.2);
--shadow-crisp: 6px 6px 0px rgba(0, 0, 0, 1);
```

---

## Layout

### Grid System
- Responsive grid-based layout
- Six-category product grid pattern
- Modular card layouts for content
- Two-column footer (stacks on mobile)

### Breakpoints
```css
/* Mobile */
@media (max-width: 786px) {
  /* Mobile-specific styles */
}
```

### Container Margins
- **Mobile**: 25px side margins
- **Desktop**: Wider containers with centered content

---

## Brand Assets

### Logos

#### Primary Logo (Navy)
```
URL: https://www.hudsonvilleicecream.com/wp-content/uploads/2023/03/HUD23_Logo_IceCream_Navy_RGB.jpg
Dimensions: 1200x600px
Format: JPG
```

#### White Logo (For dark backgrounds)
```
URL: https://www.hudsonvilleicecream.com/wp-content/uploads/2023/03/logo-white.svg
Format: SVG
```

---

## Design Patterns

### Product Presentation
- High-quality product photography
- Grid layout showcasing ice cream varieties
- Category-based organization
- Clean, appetizing imagery with white backgrounds

### Navigation
- Horizontal primary navigation
- Skip-to-content accessibility link
- Secondary navigation for utility links
- Footer mirrors main navigation structure

### Content Cards
- Clean, minimal design
- Product imagery prominently featured
- Descriptive category labels
- Hover states for interactivity

---

## Brand Voice & Messaging

### Key Themes
- **Quality**: "Since 1926" - heritage and trust
- **Authenticity**: Emphasis on "Real" ingredients (italicized)
- **Premium**: Modern, clean design balancing playful and professional
- **Approachable**: Friendly, accessible brand personality

### Messaging Patterns
- Short, punchy headlines in Bebas Neue
- Value-focused copy
- Product variety emphasis
- Community connection (scoop locator, social media)

---

## Interactive Elements

### Hover States
- Buttons: Navy → Light Blue background, Navy text
- Links: Color transitions
- Cards: Subtle elevation or shadow effects

### Transitions
```css
transition: background-color 0.3s ease;
```

---

## Accessibility Features
- Skip to content link
- Semantic HTML structure
- High contrast color combinations
- Clear focus states for keyboard navigation

---

## Social Media Integration
- Facebook
- Instagram
- Newsletter signup prominent
- Community engagement emphasis

---

## Implementation Notes

### Font Loading
Bebas Neue Pro must be loaded (likely via Adobe Fonts or similar):
```html
<link rel="stylesheet" href="https://use.typekit.net/xxx.css">
<!-- OR -->
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap">
```

Note: "Bebas Neue Pro" is slightly different from the free "Bebas Neue" - consider the free version as fallback or source the Pro version.

### CSS Architecture Recommendation
Use CSS custom properties for the design system to maintain consistency:

```css
:root {
  /* Colors */
  --color-primary: #102250;
  --color-secondary: #4495d2;
  --color-white: #ffffff;
  --color-black: #000000;

  /* Typography */
  --font-heading: 'bebas-neue-pro', sans-serif;
  --font-body: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;

  /* Spacing - use the values from spacing system above */

  /* Effects */
  --shadow-natural: 6px 6px 9px rgba(0, 0, 0, 0.2);
  --radius-pill: 100px;
  --radius-round: 9999px;
}
```

---

## Next Steps

1. **Content Integration**: Ready to receive campaign content for the loyalty program
2. **Template Development**: Build HTML/CSS templates using this design system
3. **Asset Collection**: Gather product images and any campaign-specific imagery
4. **Responsive Testing**: Ensure mobile breakpoint matches at 786px
5. **Brand Compliance**: Verify all elements match the established patterns

---

*Document created: 2025-10-24*
*Source: hudsonvilleicecream.com*
