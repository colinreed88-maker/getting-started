# Flow Domain Knowledge

This guide covers what you need to know about Flow as a business so the AI can build things that make sense in our context.

---

## Who We Are

Flow is a hospitality company. We create spaces where people feel at home -- restaurants, hotels, bars, event spaces, and mixed-use properties. Everything we build digitally should reflect the same warmth, authenticity, and elevated quality as the physical spaces.

---

## Brand Identity

Flow's brand is warm, welcoming, and elevated. Not flashy, not corporate, not "tech startup." Think: a beautifully designed boutique hotel lobby, not a Silicon Valley pitch deck.

### Colors

| Name | Hex | Usage |
|------|-----|-------|
| Moonlight | `#F3EDDF` | Backgrounds, cards, surface |
| Midnight | `#3D3D3D` | Primary text, headers (dark charcoal, NOT blue) |
| Sunlight | `#E89700` | CTAs, highlights, accents |
| Heart | `#F99AA9` | Warm pink accent |
| Ocean Swell | `#7DADBB` | Cool secondary accent |
| Olive | `#767317` | Earthy accent |
| Roots | `#8C4500` | Warm brown accent |

### Fonts

| Font | Usage | Size |
|------|-------|------|
| Roughwell | Headlines, display text | ~48px |
| Generation 1970 Light | Subheaders, CTAs | ~24px |
| Poppins | Body text, captions | Standard |

### Tone

- First-person plural: "we" and "us," not "the company" or "Flow Inc."
- No exclamation points. No emojis. Oxford comma.
- Positive, approachable, elevated, authentic
- Casual but rhythmic -- like a conversation, not a press release

### Visual Style

- Warm cream backgrounds (`#EDE8DA`)
- White cards with thin borders, soft shadows
- `border-radius: 12px` on cards and containers
- Clean, elevated, timeless

**Flow IS:** Welcoming, Elevated, Authentic, Calm, Soulful

**Flow is NOT:** Pretentious, Cheesy, Overbearing, Generic

---

## Digital Properties

Flow has several internal and external digital properties:

- **Flow Intranet** — Internal dashboard for team metrics, announcements, and operational data
- **Slide decks** — HTML-based presentation system (not PowerPoint) with branded templates
- **Internal tools** — Various dashboards and utilities built with Next.js

When you build something new, it should visually fit alongside these existing properties.

---

## Tech Stack

All Flow digital projects share this foundation:

| Layer | Tool |
|-------|------|
| Framework | Next.js 15 (App Router) + TypeScript |
| Styling | Tailwind CSS |
| Package manager | pnpm v10 (never npm or yarn) |
| Deployment | GitHub → Vercel |
| Charts | Recharts (lazy-loaded) |

---

## Financial Conventions

When working with financial data in any context:

- Negatives in parentheses: ($3.2M) not -$3.2M
- Use M for millions, K for thousands: $4.2M, $150K
- Always include units and time periods
- Currency precision: thousands with one decimal ($4.2M), exact amounts with two decimals ($4,231.50)

---

## Next Step

Proceed to [06 - Workflow and Lifecycle](06-workflow-and-lifecycle.md) to learn the structured process for building things at Flow.
