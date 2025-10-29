# Hudsonville x Perk Microsite - Development Notes

**Project Repository:** https://github.com/tgauss/hudsonville-perk-microsite
**Live Site:** https://hudsonville.perk.ooo/
**Last Updated:** October 28, 2025

---

## Project Overview

A campaign microsite showcasing Perk's receipt-driven loyalty platform for Hudsonville Ice Cream. The site demonstrates platform capabilities using real data from M&M'S Fun Club, complete with Hudsonville's brand identity.

---

## Current State (Latest Commit: 80b2f7f)

### Technical Stack
- **Frontend:** Pure HTML/CSS/JavaScript (no framework)
- **Hosting:** Vercel (auto-deploys from main branch)
- **Domain:** hudsonville.perk.ooo
- **Repository:** GitHub (tgauss/hudsonville-perk-microsite)

### Key Files
- `index.html` - Main microsite (2,300+ lines)
- `assets/logos/` - Hudsonville logos (navy JPG, white SVG)
- `assets/fonts/Lesley.woff` - Script accent font
- `assets/products/` - 6 product images
- `assets/receipt-example-fred-meyer.jpg` - Real receipt for OCR demo
- `.vercelignore` - Deployment exclusions
- `BRAND_GUIDE.md` - Complete design system
- `README.md` - Deployment instructions

---

## Session Changes (October 28, 2025)

### 1. Mobile Responsiveness Improvements
**Commit:** f749827

Added comprehensive mobile breakpoints and responsive grid systems:
- **Primary breakpoint (786px):** Single column layouts, reduced font sizes
- **Medium breakpoint (650px):** Stats grid border adjustments
- **Small breakpoint (480px):** Extra small screen optimizations

**CSS Classes Added:**
```css
.ocr-grid { grid-template-columns: 1fr 2fr → 1fr on mobile }
.receipt-insights-grid { 2 columns → 1 column on mobile }
.multiplier-grid { 3 columns → 1 column on mobile }
.profile-header-content { flex → column on mobile }
.stats-grid { Responsive borders }
```

**Key Fixes:**
- Receipt image loses sticky positioning on mobile
- Code viewers reduce to 300px max-height on mobile
- Container padding adjusts for small screens
- Text wrapping enabled for headings

### 2. GitHub & Vercel Deployment Setup
**Commits:** 24172dd, db01845, 751b065, 60a5f4d, b42ec43, 7ff119d

**GitHub Setup:**
- Initialized git repository
- Created remote: `tgauss/hudsonville-perk-microsite`
- Initial commit with all assets and code

**Vercel Configuration:**
- Removed custom `vercel.json` (auto-detection works better)
- Configured `.vercelignore` to exclude:
  - Documentation files (except README.md)
  - Source data (JSON files, unused receipts)
  - Development files (font-demo.html, lesley/ folder)
  - Root-level duplicates (Lesley.woff, Perk logos)

**Deployment Issues Fixed:**
- Logo not showing: Fixed `.vercelignore` path patterns
- Receipt image not showing: Changed wildcard to specific filename
- Lesley font not loading: Changed `Lesley.woff` → `/Lesley.woff` (root-only exclusion)

### 3. Footer Updates
**Commits:** db01845, 751b065

**Contact Information:**
- Email: joe@perksocial.com
- Phone: (614) 668-8884
- Website: perkstudios.com

**Messaging:**
- Changed "About This Proposal" → "Building the Future"
- Changed copyright text from "proposal" → "reimagined"
- More forward-looking, partnership-focused tone

### 4. M&M'S Fun Club Case Study Section
**Commit:** 81685c2

Added comprehensive case study section with 10 proven results:

1. **Engagement = Sales:** 8× more spending from high-engagement users
2. **Gamification Works:** 2× higher receipt activity
3. **Massive Campaign Lifts:** +273% actions, +501% receipt uploads
4. **Habit-Building Content:** 3× longer active, 2.5× more actions
5. **Interactive Fun Pays:** 3.1 receipts/user, $70-$100 baskets
6. **Automation Drives Growth:** Weekly engagement, no manual lift
7. **Omni-Channel Loyalty:** 5× more spend, 18.6× more receipts
8. **First-Party Data Advantage:** 1,700+ retailers, 11K products
9. **Referral Flywheel:** 1,758 friends recruited, $4,786 incremental purchases
10. **Proven Revenue Impact:** $1.6M+ direct online revenue (featured card)

**Design:**
- Dark navy gradient background
- Glass-morphism cards with backdrop blur
- Gold highlights for key metrics (later changed to light blue)
- Responsive grid layout
- CTA at bottom linking to contact

**Initial Position:** After "How It Works" section
**Final Position:** Before final CTA section (better flow)

### 5. Hero Section Redesign
**Commit:** 24ae6a4

Complete redesign for more engaging, inspiring experience:

**Visual Enhancements:**
- Gradient background: Navy (#102250) → Medium Navy → Light Blue (#4495d2)
- Decorative blur circles for depth
- Centered layout with max-width 900px

**Content Updates:**
- Badge: "⚡ RECEIPT-DRIVEN LOYALTY REIMAGINED"
- New headline: "EVERY *Scoop* EVERY STORE EVERY INSIGHT"
- Enhanced copy mentioning Kroger, Meijer, Target, local grocers
- Dual CTAs: Primary (light blue) + Secondary (outline)

**Stats Grid:**
- 4 enhanced cards with 3-line details each
- 100% Omnichannel Coverage
- $1.6M+ Proven Revenue Impact
- SKU Line-Item Intelligence
- 2.8s OCR Processing Speed

### 6. Light Blue Accent Section
**Commit:** 24ae6a4

Converted "Get the Scoop" customer profile section:
- **Background:** #4495d2 (light blue)
- **Headers:** #102250 (navy)
- **Body text:** White
- Creates visual variety mid-page

### 7. Brand Color Standardization
**Commit:** 80b2f7f

Replaced all gold/yellow accents with Hudsonville's official light blue:
- ❌ #FFD700 (gold) → ✅ #4495d2 (light blue)
- ❌ #FFA500 (orange) → ✅ #4495d2 (light blue)

**Changes:**
- Hero badge text, "Scoop" headline, retailer names
- Primary CTA button background
- All stat card numbers
- M&M's case study emphasis text
- Featured revenue card gradient
- Achievement/bonus timeline cards
- Button shadows and glows

**Final Brand Palette:**
- **Primary Navy:** #102250
- **Light Blue:** #4495d2
- **White:** #FFFFFF
- **Black:** #000000

---

## Site Structure

### Page Sections (In Order)

1. **Header** - Sticky navigation with Hudsonville logo
2. **Hero** - Gradient background, dual CTAs, 4 stat cards
3. **Why It Matters** - 3 cards explaining value proposition
4. **How It Works** - 3-step process (Snap, Scan, Sync)
5. **OCR Demo** - 1/3 receipt image, 2/3 data visualization
   - Every Receipt Tells a Story
   - Complete Structured Payload (JSON viewer)
   - The Multiplier Effect
6. **Customer Profile** (Light Blue Accent) - Taylor G. real user data
7. **Activity Ledger** - 9-month timeline with color-coded actions
8. **Data Tabs** - 5 interactive tabs with JSON payloads
9. **Activation Playbook** - 6 campaign ideas
10. **M&M'S Case Study** - 10 proven results with revenue impact
11. **CTA Section** - Final call-to-action
12. **Footer** - Contact info, platform capabilities, copyright

### Interactive Features

**Tab Switching:**
```javascript
function showTab(tabName, event) {
  if (event) event.preventDefault();
  // Hide all tabs
  document.querySelectorAll('.tab-content').forEach(tab => {
    tab.classList.remove('active');
  });
  // Show selected tab
  document.getElementById('tab-' + tabName).classList.add('active');
  // Update button states
  document.querySelectorAll('.tab-btn').forEach(btn => {
    btn.classList.remove('active');
  });
  if (event && event.target) {
    event.target.classList.add('active');
  }
}
```

**Sticky Navigation:**
- Fixed header on scroll
- Smooth scroll to sections
- Mobile hamburger menu (future enhancement)

---

## Design System

### Typography
- **Headings:** Bebas Neue (Google Fonts) - Uppercase, 1px letter-spacing
- **Script Accent:** Lesley (self-hosted WOFF) - Used for "Real", "Scoop"
- **Body:** System sans-serif stack
- **Code:** SF Mono, Monaco, Cascadia Code, Roboto Mono

### Colors
```css
--color-primary: #102250;    /* Navy */
--color-secondary: #4495d2;  /* Light Blue */
--color-white: #ffffff;
--color-black: #000000;
--color-bg-light: #f5f5f5;
--color-bg-cream: #e8e4de;
--color-code-bg: #1e1e1e;   /* Dark theme for code viewers */
```

### Spacing
```css
--space-xs: 0.5rem;
--space-small: 1rem;
--space-medium: 2rem;
--space-large: 3rem;
--space-xl: 4rem;
--space-xlarge: 3rem; /* Reduced to 2rem on mobile */
```

### Shadows
```css
--shadow-natural: 6px 6px 9px rgba(0, 0, 0, 0.2);
--shadow-soft: 0 2px 8px rgba(0, 0, 0, 0.1);
```

### Breakpoints
- Desktop: 1200px+
- Tablet: 786px - 1200px
- Mobile: 480px - 786px
- Small Mobile: < 480px

---

## Data Sources

### Real User Data (Taylor G.)
- **Profile:** user_profile__comprehensive_snapshot_with_purchase_history_2025-10-24T17_33_34.100366099Z.json
- **Activity Feed:** query_result_2025-10-24T17_38_56.042832403Z.json
- **Stats:** 12,696 total points, 2,796 balance, $205 basket, $41 eligible
- **Tier:** "CHOCOLATE CHAMP"
- **Location:** Vancouver, WA 98683

### Receipt Example
- **File:** assets/receipt-example-fred-meyer.jpg
- **Store:** Fred Meyer, Vancouver, WA
- **Date:** October 21, 2025
- **Items:** 21 line items
- **Total:** $117.44
- **Order ID:** 1475425

### M&M'S Fun Club Results
Source data from Perk platform analytics:
- $1.6M+ direct online revenue
- 1,700+ unique retailers tracked
- 11K products in database
- 1,758 referrals generated
- 96% OCR confidence score
- 2.8s processing time

---

## Git Workflow

### Main Branch Protection
- All commits go to main
- Vercel auto-deploys on push
- Commit messages follow conventional format

### Recent Commit History
```
80b2f7f - Replace gold accents with Hudsonville brand light blue (#4495d2)
24ae6a4 - Redesign hero section and add light blue accent section
81685c2 - Add M&M'S Fun Club case study section with proven results
f749827 - Fix Lesley font deployment issue
7ff119d - Fix Vercel deployment - remove custom config, use auto-detection
b42ec43 - Fix .vercelignore to include receipt image
60a5f4d - Add Vercel deployment configuration
751b065 - Update footer messaging to be forward-looking
db01845 - Update footer with Joe's contact information
24172dd - Initial commit: Hudsonville x Perk campaign microsite
```

---

## Known Issues & Future Enhancements

### Minor Issues
- [ ] Mobile hamburger menu not yet implemented
- [ ] Tab focus states could be improved for accessibility
- [ ] No analytics tracking yet

### Enhancement Ideas
1. **Animation:** Add scroll-triggered animations for sections
2. **Video:** Embed demo video in hero or OCR section
3. **Forms:** Add lead capture form in CTA section
4. **Analytics:** Add Google Analytics or Mixpanel tracking
5. **A/B Testing:** Test different hero headlines
6. **SEO:** Add meta tags, Open Graph, schema markup
7. **Performance:** Lazy load images below fold
8. **Accessibility:** ARIA labels, keyboard navigation
9. **Interactive Demo:** Clickable receipt upload simulation
10. **Case Study Modal:** Expand M&M's results in popup

### Content Updates Needed
- [ ] Replace placeholder email in CTA section
- [ ] Add actual demo scheduling link
- [ ] Update with final Hudsonville contact if different from Joe
- [ ] Add privacy policy link if needed for compliance

---

## Development Commands

### Local Development
```bash
# Open in browser
open index.html

# Or use local server
python3 -m http.server 8000
# Visit http://localhost:8000
```

### Deployment
```bash
# Commit changes
git add .
git commit -m "Description of changes"
git push

# Vercel auto-deploys in 1-2 minutes
# Check status: https://vercel.com/dashboard
```

### Find & Replace Operations
```bash
# Find color usage
grep -n "#FFD700" index.html

# Replace colors globally
sed -i '' 's/#FFD700/#4495d2/g' index.html
```

---

## Contact & Support

**Primary Contact:** Joe
**Email:** joe@perksocial.com
**Phone:** (614) 668-8884
**Website:** perkstudios.com

**Repository Issues:** https://github.com/tgauss/hudsonville-perk-microsite/issues
**Vercel Dashboard:** https://vercel.com/tgauss/hudsonville-perk-microsite

---

## Quick Reference Links

- **Live Site:** https://hudsonville.perk.ooo/
- **GitHub Repo:** https://github.com/tgauss/hudsonville-perk-microsite
- **Brand Guide:** [BRAND_GUIDE.md](BRAND_GUIDE.md)
- **Asset Inventory:** [assets/ASSETS_INVENTORY.md](assets/ASSETS_INVENTORY.md)
- **Font Setup:** [assets/fonts/FONTS_SETUP.md](assets/fonts/FONTS_SETUP.md)
- **Deployment Docs:** [README.md](README.md)

---

## Session Summary

**Total Commits:** 10
**Lines Changed:** ~500+
**Key Achievements:**
- ✅ Fully responsive mobile design
- ✅ Deployed to production (Vercel)
- ✅ Added M&M'S case study with real data
- ✅ Redesigned hero for better engagement
- ✅ Standardized brand colors throughout
- ✅ Fixed all deployment issues
- ✅ Updated contact information
- ✅ Created comprehensive documentation

**Status:** Production-ready, live at https://hudsonville.perk.ooo/

---

*Last updated: October 28, 2025*
*Generated with Claude Code*
