# Supreme Choice Insurance — Home CA Bid Optimization Report

A single-page bid optimization recommendations report for the **Supreme Choice Insurance Home · California** campaign. Built as a static HTML dashboard and deployed via Netlify.

## Overview

This report presents data-driven bid modifier recommendations designed to increase lead volume by aligning effective bids with market-rate CPCs. All pricing data is sourced from **Periscope RightPricing** (trailing 7-day window at the 2nd ad position).

### Key Recommendations

| Setting | Current | Recommended |
|---|---|---|
| **Base Bid** | $2.41 | **$3.57** |
| Anchor Source | — | Tier 2 @ 2nd Position |

The recommended base bid is anchored to the 2nd-position market CPC for Tier 2 referral traffic — the median cost across the three referral tiers with sufficient volume.

## Report Contents

The report includes the following sections:

- **KPI Summary** — Current base bid, recommended base bid, and anchor source at a glance.
- **Source Modifier Recommendations** — Per-source multiplier table covering Tier 1–3 referral, Home Search, and Home SearchB with market CPC, current vs. recommended multipliers, and effective bid calculations.
- **Supporting Data** — Side-by-side bar charts comparing current effective bids against market 2nd-position CPCs, plus a current campaign metrics panel (spend, leads, blended CPC, opportunities, win rate, bid rate).
- **Secondary Sources** — Preliminary recommendations for sources with fewer than 50 market clicks (Premium Paid Search 4 & 5, Internal SEO, Native/Display/Social, Premium Referral).
- **Implementation Approach** — A phased rollout plan (Day 1 initial modifiers → Days 1–7 monitoring → Day 7–8 full right-pricing → ongoing weekly review).
- **Quick Reference** — Phase 1 and Phase 2 settings in a scannable two-column layout for fast implementation.

## Tech Stack

| Component | Detail |
|---|---|
| Frontend | Single self-contained `index.html` (HTML + CSS, no JavaScript) |
| Hosting | Netlify (static site) |
| Styling | CSS custom properties using GOAL brand color system |
| Responsive | Mobile-friendly via CSS media queries (≤ 768 px breakpoint) |
| Print | Print-optimized styles with `break-inside: avoid` on key sections |

## Project Structure

```
sci-home-ca-bid-recs/
├── index.html      # Full report — markup, styles, and data in one file
├── netlify.toml    # Netlify build config and security headers
└── README.md       # This file
```

## Deployment

The site is configured for **Netlify** with the following setup in `netlify.toml`:

- **Publish directory:** `.` (root)
- **Security headers** applied to all routes:
  - `X-Frame-Options: DENY`
  - `X-Content-Type-Options: nosniff`
  - `Referrer-Policy: strict-origin-when-cross-origin`

To deploy your own instance, connect this repo to a Netlify site — no build step is required.

## Local Development

No dependencies or build tools are needed. Simply open `index.html` in a browser:

```bash
open index.html
# or
python3 -m http.server 8000
```

## Brand System

The report follows the **GOAL** performance marketing platform design language, using CSS custom properties for consistent theming:

| Token | Value | Usage |
|---|---|---|
| `--goal-brand` | `#077BE5` | Primary blue, KPI values, chart bars |
| `--goal-dark-blue` | `#00172D` | Headlines, body text |
| `--goal-accent-1` | `#3AEECA` | Success/positive indicators |
| `--goal-accent-2` | `#97C2E8` | Secondary chart elements |
| `--goal-accent-3` | `#9FDACD` | Tertiary accents |

## License

Internal use only — Supreme Choice Insurance / GOAL Platform.
