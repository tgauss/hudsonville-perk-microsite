# Getting Started with Hudsonville Campaign Microsite

Quick start guide for building the loyalty program campaign.

---

## ⚡ 5-Minute Setup

### Step 1: View the Demo (1 min)
Open `font-demo.html` in your browser to see:
- ✅ How fonts work together
- ✅ Color palette in action
- ✅ Button hover effects
- ✅ Headline patterns with script accents

### Step 2: Understand the Typography (2 min)
The headline pattern is **key to the Hudsonville brand**:

```html
<h1>EXPERIENCE <span class="script-accent">Real</span> PREMIUM ICE CREAM</h1>
```

- **UPPERCASE BEBAS NEUE** = Structure and impact
- **Lesley script** = Warmth and authenticity on emphasis words

### Step 3: Copy the Starter Template (2 min)
See `README.md` for the HTML starter template with all fonts and colors pre-configured.

---

## 🎨 The Two Essential Fonts

### 1. Bebas Neue (Headings)
```css
font-family: 'Bebas Neue', sans-serif;
text-transform: uppercase;
letter-spacing: 1px;
```
**Use for**: All headlines, buttons, navigation

### 2. Lesley (Script Accent)
```css
font-family: 'Lesley', cursive;
text-transform: none;
letter-spacing: 0;
```
**Use for**: The word "Real" and other emphasis words in headlines

---

## 🎯 The Pattern You'll Use Most

### Headline with Script Accent

**HTML:**
```html
<h1>
  LOYALTY MADE <span class="script-accent">Real</span>
</h1>
```

**Result:**
LOYALTY MADE *Real* (where *Real* is in flowing script)

### More Examples:
```html
<!-- Loyalty messaging -->
<h1>EARN <span class="script-accent">Real</span> REWARDS</h1>

<!-- Product messaging -->
<h1>TASTE <span class="script-accent">Real</span> ICE CREAM</h1>

<!-- Value proposition -->
<h1>EXPERIENCE <span class="script-accent">Real</span> PREMIUM QUALITY</h1>

<!-- Multiple accents -->
<h1>
  <span class="script-accent">Real</span> INGREDIENTS.
  <span class="script-accent">Real</span> FLAVOR.
</h1>
```

---

## 🎨 Color Usage Quick Reference

```css
/* Primary Navy - Main brand color */
background: #102250;  /* Buttons, headers, key sections */

/* Light Blue - Interactive states */
background: #4495d2;  /* Button hover, links, accents */

/* White & Black - Content */
background: #ffffff;  /* Page backgrounds */
color: #000000;       /* Body text */
```

### Button Pattern
```css
.btn {
  background: #102250;  /* Navy */
  color: #ffffff;       /* White text */
}

.btn:hover {
  background: #4495d2;  /* Light blue */
  color: #102250;       /* Navy text */
}
```

---

## 📐 Spacing Quick Reference

Use these standard spacing values:

```css
--space-small: 1rem;    /* 16px - Between related elements */
--space-medium: 2rem;   /* 32px - Between sections */
--space-large: 3rem;    /* 48px - Major section breaks */
```

---

## 🖼️ Using Product Images

All product images are in `assets/products/`:

```html
<!-- Hero section with product -->
<div class="hero">
  <img src="assets/products/ice-cream-mackinac-island-fudge.png"
       alt="Mackinac Island Fudge Ice Cream">
  <h1>EXPERIENCE <span class="script-accent">Real</span> PREMIUM ICE CREAM</h1>
</div>
```

**Available Products:**
- `ice-cream-mackinac-island-fudge.png` - Classic pint
- `ice-cream-bars.png` - Bar products
- `limited-edition-tropical-twist.png` - Seasonal
- `new-flavors-mint-deer-traxx.png` - New releases
- `extra-indulgent-pints.png` - Premium line
- `little-debbie-collaboration.png` - Partnership product

---

## 🏗️ Common Layout Patterns

### Hero Section
```html
<section class="hero" style="background: #102250; color: white; padding: 3rem; text-align: center;">
  <img src="assets/logos/hudsonville-logo-white.svg"
       alt="Hudsonville Ice Cream"
       style="width: 200px; margin-bottom: 2rem;">

  <h1 style="font-size: 42px; margin-bottom: 1rem;">
    LOYALTY MADE <span class="script-accent" style="color: #4495d2;">Real</span>
  </h1>

  <p style="font-size: 18px; margin-bottom: 2rem;">
    Join our rewards program and earn real benefits with every purchase.
  </p>

  <button class="btn" style="background: white; color: #102250;">
    Join Now
  </button>
</section>
```

### Product Grid
```html
<section style="padding: 3rem;">
  <h2 style="text-align: center; margin-bottom: 2rem;">
    EARN POINTS ON ALL <span class="script-accent">Real</span> FLAVORS
  </h2>

  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 2rem;">
    <div class="product-card">
      <img src="assets/products/ice-cream-mackinac-island-fudge.png"
           alt="Classic Ice Cream">
      <h3>Classic Pints</h3>
      <p>Earn 10 points per pint</p>
    </div>
    <!-- More products... -->
  </div>
</section>
```

### Call-to-Action Section
```html
<section style="background: #f5f5f5; padding: 3rem; text-align: center;">
  <h2 style="font-size: 36px; margin-bottom: 1rem;">
    READY TO EARN <span class="script-accent">Real</span> REWARDS?
  </h2>

  <p style="margin-bottom: 2rem;">
    Sign up today and get 50 bonus points to start!
  </p>

  <button class="btn">Sign Up Free</button>
</section>
```

---

## ✅ Quick Checklist for Every Page

- [ ] Logo in header (white on navy, navy on white)
- [ ] Headlines use Bebas Neue (uppercase, 1px letter-spacing)
- [ ] Emphasis words use `.script-accent` (Lesley font)
- [ ] Buttons are pill-shaped (100px border-radius)
- [ ] Primary color is navy (#102250)
- [ ] Button hover changes to light blue (#4495d2)
- [ ] Body text uses system sans-serif
- [ ] Mobile-friendly (responsive at 786px breakpoint)

---

## 🚫 Common Mistakes to Avoid

1. **Don't** make script words uppercase
   - ❌ `<span class="script-accent">REAL</span>`
   - ✅ `<span class="script-accent">Real</span>`

2. **Don't** use script font for entire headlines
   - ❌ `<h1 class="script-accent">Experience Real Premium Ice Cream</h1>`
   - ✅ `<h1>EXPERIENCE <span class="script-accent">Real</span> PREMIUM ICE CREAM</h1>`

3. **Don't** forget letter-spacing on Bebas Neue
   - ❌ `font-family: 'Bebas Neue', sans-serif;`
   - ✅ `font-family: 'Bebas Neue', sans-serif; letter-spacing: 1px;`

4. **Don't** use italic for emphasis - use script accent instead
   - ❌ `<h1>EXPERIENCE <em>Real</em> PREMIUM ICE CREAM</h1>`
   - ✅ `<h1>EXPERIENCE <span class="script-accent">Real</span> PREMIUM ICE CREAM</h1>`

---

## 📚 Where to Find More Info

| Need | See Document |
|------|--------------|
| Complete design system | [BRAND_GUIDE.md](BRAND_GUIDE.md) |
| Font troubleshooting | [assets/fonts/FONTS_SETUP.md](assets/fonts/FONTS_SETUP.md) |
| Asset details | [assets/ASSETS_INVENTORY.md](assets/ASSETS_INVENTORY.md) |
| Visual reference | [font-demo.html](font-demo.html) |
| Project overview | [README.md](README.md) |

---

## 💡 Pro Tips

1. **Use the demo as reference**: Keep `font-demo.html` open while building
2. **Start with a section**: Copy a pattern from the demo and modify
3. **Test fonts early**: Make sure Lesley.woff loads before building pages
4. **Mobile-first**: Design looks great on all screen sizes
5. **Keep it simple**: The brand is clean and minimal - don't over-design

---

## 🎉 You're Ready!

You now have everything needed to build a brand-accurate Hudsonville loyalty campaign microsite.

**Next step**: Add your campaign content (copy, CTAs, rewards info) and start building!

---

*Happy building! 🍦*
