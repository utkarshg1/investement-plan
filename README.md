# Master Wealth & Acquisition Roadmap (2027–2053+)

A comprehensive financial execution plan covering accumulation, growth, capital preservation, and retirement income drawdown — all built on the HDFC Mutual Fund ecosystem.

## Phases

| Phase | Timeline                      | Strategy                                                                                      |
| ----- | ----------------------------- | --------------------------------------------------------------------------------------------- |
| **1** | Jan 2027 – Nov 2038 (~12 Yrs) | Accumulation & Goal Funding (HDFC BAF) — ₹8k SIP for 5 Yrs + ₹15k step-up SIP for 10 Yrs      |
| **2** | Dec 2038 – Dec 2048 (10 Yrs)  | Diversified Wealth Creation (HDFC Flexi Cap + Small Cap + Hybrid Debt)                        |
| **3** | Jan 2049 – Jan 2054 (5 Yrs)   | STP & Capital Preservation (HDFC Equity Savings Fund / HDFC Gold ETF Fund / HDFC Liquid Fund) |
| **4** | Post-2054                     | SWP & Retirement Income (4% annual withdrawal from HDFC Equity Savings Fund only)             |

## Wealth Projections (Conservative Estimates)

| Phase                      | Nominal Corpus  | Real Value (6% Inflation) |
| -------------------------- | --------------- | ------------------------- |
| Phase 1 End (Nov 2038)     | ₹21.75 Lakh     | ₹10.81 Lakh               |
| Phase 2 End (Dec 2048)     | ₹1.32 Crore     | ₹36.63 Lakh               |
| **Phase 3 End (Jan 2054)** | **₹1.99 Crore** | **₹41.36 Lakh**           |
| Phase 4 SWP (Monthly)      | ₹51,700         | ₹10,700                   |

- **Total Invested:** ₹67.17 Lakh
- **Total Withdrawn (Trek + Speedmaster):** ₹38.50 Lakh
- **Gold + Liquid Buffer (locked):** ₹43.70 Lakh
- **Assumed rates:** 12% Equity/Flexi Cap/Small Cap, 10% Hybrid Debt/Equity Savings, 12% Gold ETF, 6% Liquid

## Features

- Desktop-first spacious layout — premium typography, generous padding, clean visual hierarchy
- 2-column quadrant grid — all 4 phases, timeline matrix, and summary stats
- **Wealth projection card** — phase-wise corpus estimates with inflation-adjusted real values
- Mobile-optimized responsive design — iPhone 12 Pro+ tested, `overflow-x: hidden` prevents horizontal scroll, Phase 1 sub-cards stack in single column (`grid-cols-1`) on mobile with `sm:grid-cols-2` for tablet/desktop, footer stats wrap on narrow screens, cards clip at rounded corners
- Print-optimized **single-page A4 layout** — header, 4 phases (2-column grid), execution matrix table, wealth projection card, and stats all fit on one page; ultra-compact wealth card with 4-col grid and 6.5–7pt fonts; `break-inside: avoid` on all cards and tables
- Color-coded phase system with allocation bars
- **Compact Phase 2 cards** — inline category badges, percentage allocations, and `/ mo` labels for reduced vertical height
- **Single-line fund titles** — `text-[11px] tracking-tight whitespace-nowrap text-ellipsis` prevents wrapping; "Fund" suffix trimmed
- **Print-optimized Phase 2** — `print:` modifiers use pt units (`6.5pt`, `8.5pt`, `9pt`) to prevent text overflow in A4 columns; `tracking-normal` on category badges, `leading-none` on descriptions
- Master execution matrix — desktop table + mobile card layout via `hidden md:block` / `md:hidden`
- Zero JavaScript — pure HTML/CSS, GitHub Pages compatible

## Project Structure

```
investement-plan/
├── index.html      # Main page (all 4 phases)
├── styles.css      # Desktop styles + isolated print engine
├── favicon.svg     # SVG favicon (growth arrow icon)
├── .prettierrc     # Prettier config (120 print width)
├── .nojekyll       # Disables Jekyll on GitHub Pages
└── README.md
```

## Preview Locally

```bash
# Clone the repo
git clone https://github.com/<your-username>/investement-plan.git
cd investement-plan

# Open in browser
start index.html
# or
open index.html
```

## GitHub Pages Deployment

1. Push this repo to GitHub
2. Go to **Settings > Pages**
3. Set **Source** to `Deploy from a branch`
4. Select branch `main` and folder `/ (root)`
5. Click **Save** — your site will be live at `https://<your-username>.github.io/investement-plan/`

> **Favicon:** The SVG favicon (`favicon.svg`) is linked in `index.html` and doubles as the header logo. Browsers that support SVG favicons will display it; older browsers will gracefully ignore it.

## Tech Stack

- **HTML5** — semantic structure
- **Tailwind CSS** (CDN) — utility-first styling
- **Custom CSS** — desktop base styles + single-page A4 print engine (isolated in `@media print`)
- **SVG Favicon** — crisp growth-arrow icon, works as both favicon and header logo
- **Prettier** — consistent code formatting (`printWidth: 120`)
- **Zero JavaScript** — pure HTML/CSS, GitHub Pages compatible
- **Creator credit** — "Plan Created by Utkarsh Gaikwad" in footer

## Print to PDF

Open `index.html` in your browser and use **Ctrl+P** / **Cmd+P**. The print stylesheet produces a clean **single-page A4 PDF**:

- **Everything on one page** — header + 4 phases (2-column grid) + execution matrix table + wealth projection card + stats & footer
- **A4 portrait layout** — `@page { size: A4 portrait; margin: 12mm 14mm }`
- **Ultra-compact typography** — 12pt title, 10pt headings, 7.5–9pt body, 7.5pt table cells
- **Header forced side-by-side** — `flex-direction: row` ensures benchmarks stay at top-right of header
- **2-column phase grid preserved** — no single-column mobile stacking in print
- **4-column wealth projection grid** — all 4 phase corpus values on one row
- **Execution matrix forced to table** — `.print-visible` overrides Tailwind's `hidden md:block` so the table always renders in print; mobile card layout hidden via `.no-print` / `.md\:hidden`
- **All animations disabled** — no hover effects, no transitions, no shadows
- **Colors preserved** — `print-color-adjust: exact` on all backgrounds
- **Break protection** — `break-inside: avoid` on cards, table rows, and headers
- **Orphan/widow control** — `widows: 3; orphans: 3` for professional typesetting
- **Balanced spacing** — 20mm top/bottom margins, 4pt container gap, 7pt/10pt card padding, 4pt/6pt sub-card padding, 2pt/4pt table rows, 7pt table font, 6.5pt footer font (no-wrap), footer auto-pushed to page bottom
- **Desktop unaffected** — all print rules are strictly inside `@media print`, zero impact on screen rendering

## Code Formatting

```bash
# Format all files
npx prettier --write .

# Check without writing
npx prettier --check .
```

Config in `.prettierrc`: `printWidth: 120`, `htmlWhitespaceSensitivity: ignore`.

## License

Personal project — not licensed for redistribution.
