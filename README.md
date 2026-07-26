# Master Wealth & Acquisition Roadmap (2027–2051+)

A comprehensive financial execution plan covering accumulation, growth, capital preservation, and retirement income drawdown — all built on the HDFC Mutual Fund ecosystem.

## Phases

| Phase | Timeline            | Strategy                                                    |
| ----- | ------------------- | ----------------------------------------------------------- |
| **1** | Jan 2027 – Jan 2037 | Accumulation & Goal Funding (HDFC BAF)                      |
| **2** | Next 10 years       | Aggressive Wealth Creation (Small Cap + Hybrid Debt)        |
| **3** | 5-Year Duration     | STP & Capital Preservation (Equity Savings / Gold / Liquid) |
| **4** | Post-2051           | SWP & Retirement Income (4% annual withdrawal)              |

## Features

- Desktop-first spacious layout — premium typography, generous padding, clean visual hierarchy
- 2-column quadrant grid — all 4 phases, timeline matrix, and summary stats
- Mobile-optimized responsive design — card-based execution matrix, stacked phase headers, responsive typography, reduced padding/gaps, and 2×2 stats wrap
- Print-optimized A4 layout — multi-page supported with `break-inside: avoid` on all cards and tables
- Color-coded phase system with allocation bars
- Master execution matrix — desktop table + mobile card layout via `hidden md:block` / `md:hidden`
- Zero JavaScript — pure HTML/CSS, GitHub Pages compatible

## Project Structure

```
investement-plan/
├── index.html      # Main page (all 4 phases)
├── styles.css      # Desktop styles + isolated print engine
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

## Tech Stack

- **HTML5** — semantic structure
- **Tailwind CSS** (CDN) — utility-first styling
- **Custom CSS** — desktop base styles + premium print engine with A4 optimization (isolated in `@media print`)
- **Prettier** — consistent code formatting (`printWidth: 120`)
- **Zero JavaScript** — pure HTML/CSS, GitHub Pages compatible

## Print to PDF

Open `index.html` in your browser and use **Ctrl+P** / **Cmd+P`. The print stylesheet:

- **A4 portrait layout** — `@page { size: A4 portrait; margin: 12mm 14mm }` for premium whitespace
- **9pt body font** with 1.5 line-height — comfortable reading at print density
- **All animations disabled** — no hover effects, no transitions, no shadows
- **Colors preserved** — `print-color-adjust: exact` on all backgrounds
- **Break protection** — `break-inside: avoid` on cards, table rows, and headers
- **Orphan/widow control** — `widows: 3; orphans: 3` for professional typesetting
- **Phase badge spacing** — flexbox `gap-4` with `margin-right` fallback ensures 16px separation from heading text
- **Consistent card padding** — 12pt/14pt on main cards, 8pt/10pt on inner sub-cards
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
