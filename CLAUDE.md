# Charlotte Seller's Guide 2026 — Build Instructions

## Project Overview
Rebuild this multi-page static site to exactly match the Manus original at:
https://charlotte-sell-iluh5wd7.manus.space/

## Deployment
- **Hosting:** Vercel (auto-deploys from GitHub)
- **Output directory:** `public/public/public` (set in vercel.json)
- **Domain:** sellersguide.homegrownpropertygroup.com
- **Repo:** HGPG1/charlotte-sellers-guide-vercel
- **Branch:** main
- **GitHub PAT:** [USE_YOUR_PAT]
- **Remote URL:** https://[USE_YOUR_PAT]@github.com/HGPG1/charlotte-sellers-guide-vercel.git

## File Structure
```
public/public/public/
├── index.html              # Homepage
├── quiz/index.html         # Seller Readiness Quiz
├── home-selling-score/index.html  # Home Selling Score Calculator
├── neighborhoods/index.html       # Neighborhood Guide
├── compare/index.html             # Compare Areas Tool
├── market-heatmap/index.html      # Market Heatmap
└── thank-you/index.html           # Bonuses/Thank You Page
```

## Build Rules
- Each page is a **single standalone HTML file** with ALL CSS and JS embedded
- Use CDN links for external fonts only
- No build tools, no npm, no React — pure HTML/CSS/JS
- Every page shares the same nav and footer
- All internal links use relative paths (/, /quiz, /home-selling-score, etc.)
- Add `/* Last Updated: YYYY-MM-DD */` comment at top of each file

## Brand
- **Body font:** Cooper Hewitt (system fallback: system-ui, -apple-system, sans-serif)
- **Display font:** Sansita (Google Fonts CDN)
- **Colors:**
  - `#2A384C` — Dark navy (primary)
  - `#A0B2C2` — Steel blue (secondary)
  - `#D1D9DF` — Light steel (borders/muted)
  - `#F0F0F0` — Off-white (backgrounds)
  - `#ffffff` — White (cards)
  - **NO GREEN anywhere**
- **Logo URL:** https://charlotte-sell-iluh5wd7.manus.space/logo_cropped.webp
- **Alt logo:** https://charlotte-sell-iluh5wd7.manus.space/homegrown-logo.png

## Pages to Match (from Manus original)

### 1. Homepage (/)
- Sticky nav: logo left, links center, CTA button right
- Hero with location badge, headline, subtitle
- Market Pulse stats cards (Median Price, Days on Market, Active Listings, Mortgage Rate)
- "Get Your Free Guide" CTA
- "Why 2026 is the Right Time to Sell" — 3 feature cards
- "Complete Selling Timeline" — 4-step horizontal timeline
- "Unlock the Complete Seller's Guide" — lead capture CTA section
- "What's Included in Your Guide" — 6 feature cards grid
- "Success Stories" — testimonial cards with sale price and DOM
- "Sold in Your Neighborhood" — filterable recent sales cards
- "Ready to Get Started?" — bottom CTA
- Footer with logo and copyright

### 2. Seller Quiz (/quiz)
- 5-question multiple choice quiz
- Progress bar with question counter
- Radio button options with custom styling
- Back/Next navigation
- Results page with circular score gauge (SVG)
- Score interpretation with personalized message
- CTA to Home Selling Score

### 3. Home Selling Score (/home-selling-score)
- Lead capture form (name, email, phone, address)
- Multi-step form with property details
- Score calculation algorithm
- Animated score reveal with circular gauge
- Breakdown of score factors
- CTA to schedule consultation

### 4. Neighborhoods (/neighborhoods)
- Region tabs (Charlotte Core, South Charlotte, Fort Mill/Indian Land, Waxhaw/Union County, Lake Norman/North)
- Neighborhood cards with stats (median price, avg DOM, price change)
- Expandable neighborhood details
- Search/filter functionality

### 5. Compare Areas (/compare)
- Dual-column comparison tool
- Dropdown selectors for areas
- Side-by-side stats comparison
- Bar chart visualizations
- Key metrics: median price, DOM, inventory, price trends

### 6. Market Heatmap (/market-heatmap)
- Interactive neighborhood grid/list
- Color-coded by market heat (price appreciation)
- Filter controls (price range, area, market temp)
- Sortable table with market metrics
- Visual heat indicators

### 7. Thank You / Bonuses (/thank-you)
- Confirmation message
- Bonus content cards (negotiation scripts, checklist, etc.)
- Download links / access buttons
- "What's Next?" section with next steps
- CTA to schedule consultation

## Navigation (shared across all pages)
```html
<nav>
  <a href="/">Logo + "Home Grown Property Group"</a>
  <ul>
    <li><a href="/">Home</a></li>
    <li><a href="/quiz">Seller Quiz</a></li>
    <li><a href="/home-selling-score">Home Score</a></li>
    <li><a href="/neighborhoods">Neighborhoods</a></li>
    <li><a href="/compare">Compare Areas</a></li>
    <li><a href="/market-heatmap">Market Data</a></li>
    <li><a href="/thank-you">Bonuses</a></li>
  </ul>
  <a href="/home-selling-score" class="cta">Get Started</a>
</nav>
```

## Key Interactions to Match
- Smooth scroll behavior
- Nav becomes opaque/shadowed on scroll
- Hover effects on all cards and buttons
- Quiz radio buttons with custom styling and transitions
- Score gauge animated fill on results pages
- Testimonial carousel/slider behavior
- Neighborhood tab switching
- Compare area dropdown selection and chart updates
- Heatmap filter/sort interactions
- Mobile hamburger menu
- Form validation states
- All CTAs link to /home-selling-score

## Fetch the Manus Original
Before building each page, fetch the rendered content from the Manus URL to capture exact text, structure, and behavior:
- https://charlotte-sell-iluh5wd7.manus.space/
- https://charlotte-sell-iluh5wd7.manus.space/quiz
- https://charlotte-sell-iluh5wd7.manus.space/home-selling-score
- https://charlotte-sell-iluh5wd7.manus.space/neighborhoods
- https://charlotte-sell-iluh5wd7.manus.space/compare
- https://charlotte-sell-iluh5wd7.manus.space/market-heatmap
- https://charlotte-sell-iluh5wd7.manus.space/thank-you
