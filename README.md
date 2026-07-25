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

- Subtle CSS animations (hover effects, fade-ins, gradient accents, shimmer badges) — zero JavaScript
- Fully responsive mobile layout with touch-friendly tap targets
- Dense A4 print optimization — all 4 phases fit cleanly on 4 compact pages
- Color-coded phase system with animated allocation bars
- SWP income flow diagram (4-step, CSS-only)
- Hard rule warning cards with pulsing borders
- Tax implication notes
- Master timeline matrix with hover highlights
- Summary statistics dashboard

## Project Structure

```
investement-plan/
├── index.html      # Main page (all 4 phases)
├── styles.css      # Animations, mobile, print styles
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
- **Custom CSS** — animations, print compaction, mobile optimizations
- **Prettier** — consistent code formatting (`printWidth: 120`)
- **Zero JavaScript** — pure HTML/CSS, GitHub Pages compatible

## Print to PDF

Open `index.html` in your browser and use **Ctrl+P** / **Cmd+P**. The print stylesheet handles:

- **Dense A4 layout** — compact padding (0.625rem), smaller fonts (9.5pt), tight margins (12mm × 10mm)
- **Page breaks** between each phase for clean separation
- **All animations disabled** — no hover effects, no gradients, no pulses
- **Colors preserved** — `print-color-adjust: exact` on all backgrounds and badges
- **Cards kept together** — `page-break-inside: avoid` prevents mid-card splits
- **Allocation bars** — slimmer height (18px) with correct proportions
- **Tables** — compact rows with reduced padding
- **Phase headers** — smaller badges (22px) and tighter spacing

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
