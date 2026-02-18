# Business Sprint Ideation - Cursor Learning

A complete package for running a 10-day business launch sprint, including a landing page for signups and a comprehensive workbook for participants.

---

## Package Contents

### Landing Page Assets

| File | Description |
|------|-------------|
| `sprint-landing.html` | Main landing page with tiered pricing ($99 live, $17 workbook, free email) |
| `sprint-copy.md` | All landing page copy in one document for easy editing |
| `design-specs.md` | Design system and visual specifications |
| `assets-needed.md` | List of assets needed before launch |
| `index.html` | Original workbook-focused landing page (legacy) |

### Workbook & Templates

| File | Description |
|------|-------------|
| `design-sprint-workbook.html` | Complete 10-day workbook (8000+ lines, print-ready) |
| `templates/` | 7 standalone fillable templates (canvases, checklists) |
| `examples/` | Completed example templates for reference |

### Agent Documentation

| File | Description |
|------|-------------|
| `sprint-facilitator.md` | AI agent prompt for the Business Launch Sprint facilitator |

---

## Quick Start

### View Landing Page
Open `sprint-landing.html` in any browser.

### View Workbook
Open `design-sprint-workbook.html` in any browser.

### Edit Copy
All landing page text is in `sprint-copy.md`. Edit there, then update the HTML.

---

## Landing Page Structure

The `sprint-landing.html` page includes:

1. **Hero Section** - Main headline + primary CTA + secondary options
2. **Who Benefits** - 3-column personas + "Why Now" message
3. **10 Days to Launch** - Timeline + outcomes list
4. **Pricing** - Three tiers with promo code support
5. **Social Proof** - Testimonials
6. **Facilitator** - Personal intro
7. **FAQ** - Collapsible questions
8. **Final CTA** - Conversion section

### Promo Codes

Valid codes for free Live Sprint access (edit in JavaScript section):
- `FRIEND2026` - For friends and referrals
- `LAUNCH` - Launch promotion
- `BETA` - Beta testers
- `VIP` - VIP invites

---

## Workbook Structure

The `design-sprint-workbook.html` covers all 10 days:

| Days | Phase | Focus |
|------|-------|-------|
| 1-3 | Validate & Position | Problem discovery, personas, business model |
| 4-6 | Build & Register | MVP definition, legal setup, website |
| 7-9 | Market & Sell | Content, marketing channels, soft launch |
| 10 | Launch & Pitch | Public launch, founder pitch |

### Interactive Features

- Progress tracking with localStorage persistence
- Completion score in navigation header
- Confetti celebration on day completion
- Editable notes with auto-save
- Collapsible theory sections
- Floating Telegram support button
- Print-optimized layout

---

## Templates (in `/templates/`)

1. `01-problem-statement-canvas.html` - Day 1
2. `02-customer-persona.html` - Day 2
3. `03-business-model-canvas.html` - Day 3 (landscape)
4. `04-value-proposition-canvas.html` - Day 3
5. `05-mvp-specification.html` - Day 4
6. `06-launch-checklist.html` - Day 10
7. `07-pitch-script.html` - Day 10

---

## Design System

Both landing page and workbook use a consistent design system:

```css
:root {
    --black: #111111;
    --white: #FFFFFF;
    --gray-50: #FAFAFA;
    --accent: #FF6B35;
    --font-sans: 'Inter', sans-serif;
}
```

- Nike-inspired minimalist design
- Black/white primary palette with orange accent
- Clean typography with Inter font
- Generous white space
- Print-optimized layouts

---

## Generating PDFs

### Browser Print (Recommended)
1. Open any `.html` file in Chrome/Safari/Firefox
2. Press `Cmd+P` (Mac) / `Ctrl+P` (Windows)
3. Select "Save as PDF"
4. Enable "Background graphics"
5. Set margins to "None"

### Command Line
```bash
/Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome \
  --headless --print-to-pdf="workbook.pdf" \
  design-sprint-workbook.html
```

---

## Customization

### Updating Colors
Edit CSS `:root` variables in any HTML file.

### Updating Copy
1. Edit `sprint-copy.md` first
2. Copy changes to `sprint-landing.html`

### Adding Logo
Edit the `.cover-logo` section in `design-sprint-workbook.html`.

---

## Before Launch Checklist

- [ ] Replace `[Your Name]` with facilitator name
- [ ] Update cohort date in hero badge
- [ ] Add facilitator photo
- [ ] Set up payment links (Stripe/Gumroad)
- [ ] Connect email form to ConvertKit/Mailchimp
- [ ] Add real testimonials when available
- [ ] Test promo codes

---

## File Structure

```
Business sprint ideation cursor learning/
├── README.md                    # This file
├── sprint-landing.html          # Main landing page
├── sprint-copy.md               # Landing page copy document
├── design-specs.md              # Design specifications
├── assets-needed.md             # Assets checklist
├── design-sprint-workbook.html  # Complete workbook
├── sprint-facilitator.md        # AI agent prompt
├── index.html                   # Legacy landing page
├── copy-document.md             # Legacy copy document
├── templates/                   # Standalone templates
│   ├── 01-problem-statement-canvas.html
│   ├── 02-customer-persona.html
│   ├── 03-business-model-canvas.html
│   ├── 04-value-proposition-canvas.html
│   ├── 05-mvp-specification.html
│   ├── 06-launch-checklist.html
│   └── 07-pitch-script.html
└── examples/                    # Completed examples
    ├── completed-problem-statement.html
    └── completed-customer-persona.html
```

---

*10-Day Business Launch Sprint - From idea to live business in 10 working days.*
