# Design Specifications for Framer/Webflow

Complete implementation guide for building the landing page in no-code tools.

---

## Design System

### Colors

| Name | Hex | Usage |
|------|-----|-------|
| **Black** | `#111111` | Primary text, headers, buttons |
| **White** | `#FFFFFF` | Background, button text |
| **Gray 50** | `#FAFAFA` | Alternate section background |
| **Gray 100** | `#F5F5F5` | Card backgrounds, badges |
| **Gray 200** | `#E5E5E5` | Borders, dividers |
| **Gray 400** | `#A3A3A3` | Placeholder text |
| **Gray 500** | `#737373` | Secondary text, captions |
| **Gray 600** | `#525252` | Body text |
| **Accent** | `#FF6B35` | CTAs, highlights, icons |
| **Accent Hover** | `#E55A2B` | Button hover state |

### Typography

**Font Family:** Inter (Google Fonts)
- Fallback: -apple-system, BlinkMacSystemFont, sans-serif

| Element | Size (Desktop) | Size (Mobile) | Weight | Line Height |
|---------|---------------|---------------|--------|-------------|
| H1 (Hero) | 80px | 48px | 900 (Black) | 1.1 |
| H2 (Section) | 56px | 36px | 900 (Black) | 1.1 |
| H3 (Card Title) | 32px | 24px | 900 (Black) | 1.1 |
| H4 (Subhead) | 20px | 18px | 700 (Bold) | 1.3 |
| Body Large | 24px | 18px | 400 (Regular) | 1.5 |
| Body | 18px | 16px | 400 (Regular) | 1.6 |
| Body Small | 16px | 14px | 400 (Regular) | 1.6 |
| Caption | 14px | 12px | 600 (Semibold) | 1.4 |
| Button | 16px | 16px | 600 (Semibold) | 1.0 |

**Letter Spacing:**
- Headlines: `-0.02em` (tight)
- Body: `0` (normal)
- All caps text: `0.1em` (loose)

---

## Spacing System

Use 8px base unit:

| Token | Value | Usage |
|-------|-------|-------|
| `xs` | 8px | Tight gaps, icon padding |
| `sm` | 16px | Between related elements |
| `md` | 24px | Standard component padding |
| `lg` | 48px | Between components |
| `xl` | 80px | Between sections (mobile) |
| `2xl` | 120px | Between sections (desktop) |

### Section Padding
- **Desktop:** 120px top and bottom
- **Tablet:** 80px top and bottom
- **Mobile:** 60px top and bottom

### Container Width
- **Max width:** 1200px
- **Narrow container:** 800px (for FAQ, text-heavy sections)
- **Side padding:** 24px

---

## Components

### Navigation Bar

```
Height: 60px
Background: rgba(255, 255, 255, 0.95)
Backdrop blur: 10px
Border bottom: 1px solid #E5E5E5
Position: Fixed, top: 0
Z-index: 1000

Logo:
- Font size: 20px
- Font weight: 800
- Color: #111111

CTA Button:
- Padding: 10px 20px
- Font size: 14px
- Background: #111111
- Border radius: 8px
```

### Buttons

**Primary Button (Black)**
```
Padding: 16px 32px
Background: #111111
Color: #FFFFFF
Font size: 16px
Font weight: 600
Border radius: 8px
Transition: all 0.2s ease

Hover:
- Background: #262626
- Transform: translateY(-2px)
```

**Accent Button (Orange)**
```
Padding: 16px 32px
Background: #FF6B35
Color: #FFFFFF
Font size: 16px
Font weight: 600
Border radius: 8px
Transition: all 0.2s ease

Hover:
- Background: #E55A2B
- Transform: translateY(-2px)
```

**Outline Button**
```
Padding: 16px 32px
Background: transparent
Color: #111111
Border: 2px solid #111111
Font size: 16px
Font weight: 600
Border radius: 8px
Transition: all 0.2s ease

Hover:
- Background: #111111
- Color: #FFFFFF
```

**Large Button Variant**
```
Padding: 20px 40px
Font size: 18px
```

### Cards

**Pain Point Card**
```
Background: #FFFFFF
Padding: 48px
Border radius: 12px
Border: 1px solid #E5E5E5

Title:
- Font size: 24px
- Font weight: 900
- Margin bottom: 16px

Body:
- Font size: 16px
- Color: #525252
```

**Pricing Card**
```
Background: #FFFFFF
Padding: 48px
Border radius: 16px
Border: 2px solid #E5E5E5
Display: flex
Flex direction: column

Featured variant:
- Border color: #111111
- Transform: scale(1.02) (desktop only)
```

**Testimonial Card**
```
Background: #FFFFFF
Padding: 48px
Border radius: 12px
Border: 1px solid #E5E5E5

Quote:
- Font size: 18px
- Font style: italic
- Color: #404040
- Margin bottom: 24px
```

### Form Elements

**Email Input**
```
Padding: 14px 16px
Font size: 16px
Border: 2px solid #E5E5E5
Border radius: 8px
Font family: Inter

Focus:
- Border color: #111111
- Outline: none
```

### Timeline Item

```
Border left: 3px solid #FF6B35
Padding left: 24px
Padding: 24px

Days label:
- Font size: 14px
- Font weight: 700
- Color: #FF6B35
- Text transform: uppercase
- Letter spacing: 2px
- Margin bottom: 8px

Title:
- Font size: 20px
- Font weight: 700
- Color: #FFFFFF
```

### Badge

**Hero Badge**
```
Display: inline-block
Padding: 8px 16px
Background: #F5F5F5
Border radius: 100px
Font size: 14px
Font weight: 600
Color: #525252
```

**Pricing Badge**
```
Position: absolute
Top: -12px
Left: 50%
Transform: translateX(-50%)
Background: #111111
Color: #FFFFFF
Padding: 6px 16px
Border radius: 100px
Font size: 12px
Font weight: 700
Text transform: uppercase
Letter spacing: 1px
```

---

## Section Specifications

### 1. Hero Section

```
Min height: 100vh
Display: flex
Align items: center
Padding top: 120px (account for nav)
Background: #FFFFFF

Content max width: 900px
```

### 2. Pain Points Section

```
Background: #FAFAFA
Padding: 120px 0

Grid:
- Columns: repeat(auto-fit, minmax(300px, 1fr))
- Gap: 24px
```

### 3. Value Section (What You Get)

```
Background: #111111
Color: #FFFFFF
Padding: 120px 0

Timeline grid:
- Columns: repeat(auto-fit, minmax(250px, 1fr))
- Gap: 24px

Outcomes grid:
- Columns: repeat(auto-fit, minmax(200px, 1fr))
- Gap: 24px
```

### 4. Pricing Section

```
Background: #FFFFFF
Padding: 120px 0

Grid:
- Columns: repeat(auto-fit, minmax(320px, 1fr))
- Gap: 24px
- Align items: stretch
```

### 5. Social Proof Section

```
Background: #FAFAFA
Padding: 120px 0

Grid:
- Columns: repeat(auto-fit, minmax(300px, 1fr))
- Gap: 24px
```

### 6. Facilitator Section

```
Background: #FFFFFF
Padding: 120px 0

Grid (desktop):
- Columns: 300px 1fr
- Gap: 80px
- Align items: center

Mobile:
- Single column
- Text centered
```

### 7. FAQ Section

```
Background: #FAFAFA
Padding: 120px 0

Content max width: 800px
```

### 8. Final CTA Section

```
Background: #111111
Color: #FFFFFF
Padding: 120px 0
Text align: center
```

---

## Responsive Breakpoints

| Breakpoint | Width | Changes |
|------------|-------|---------|
| Desktop | > 1024px | Full layout |
| Tablet | 768px - 1024px | Reduce spacing, stack some grids |
| Mobile | < 768px | Stack all grids, show mobile CTA bar |

### Mobile-Specific

1. **Show mobile sticky CTA bar** (fixed bottom)
2. **Add body padding bottom** (80px for sticky bar)
3. **Stack pricing cards** vertically
4. **Remove featured card scale** transform
5. **Stack hero buttons** vertically
6. **Center facilitator content** and stack

---

## Animations

### Scroll Animations (Optional)
- Fade in from bottom: `opacity: 0 → 1`, `translateY: 20px → 0`
- Duration: 0.6s
- Timing: ease-out
- Trigger: When element enters viewport

### Hover Animations
- Buttons: `translateY(-2px)`, `transition: 0.2s`
- Cards: Subtle shadow on hover (optional)

---

## Framer-Specific Notes

1. **Use Components** for reusable elements (buttons, cards)
2. **Use Variables** for colors and spacing tokens
3. **Use Breakpoints** at 768px and 1024px
4. **Use Scroll Effects** for fixed nav transparency
5. **Use Forms** component for email capture
6. **Link buttons** to Stripe/Gumroad checkout URLs

## Webflow-Specific Notes

1. **Create Classes** matching the component names above
2. **Use Symbols** for nav, footer, pricing cards
3. **Use CMS** if you want to manage testimonials/FAQs
4. **Use Interactions** for scroll-based animations
5. **Use Form Block** for email capture with Zapier/Make integration
6. **Add Custom Code** for Stripe payment buttons

---

## Integration Checklist

Before launch, integrate:

- [ ] Email signup → ConvertKit / Mailchimp / Beehiiv
- [ ] Workbook purchase → Gumroad / Stripe / Lemon Squeezy
- [ ] Sprint purchase → Stripe Checkout / Gumroad
- [ ] Analytics → Google Analytics / Plausible / Fathom
- [ ] Custom domain → Connect in Framer/Webflow
