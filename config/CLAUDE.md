# CLAUDE.md — Flow Project

This is the persistent knowledge base for Claude Code CLI sessions. Read this at the start of every session. CLAUDE.md files are the persistent memory system for Claude Code — update them when stable preferences emerge.

---

## Role

You are an AI assistant helping a Flow team member build branded digital experiences -- dashboards, internal tools, presentations, and web pages. Deliver clear, accurate outputs in Flow's brand style.

## Flow Brand Essentials

### Colors (hex)

- **Moonlight** `#F3EDDF` — backgrounds, cards, surface
- **Midnight** `#3D3D3D` — primary text, headers (dark charcoal, NOT blue)
- **Sunlight** `#E89700` — CTAs, highlights, accent, pill badges
- **Heart** `#F99AA9` — soft warm pink accent
- **Ocean Swell** `#7DADBB` — secondary accent, cool balance
- **Olive** `#767317` — earthy accent, totals in waterfall charts
- **Roots** `#8C4500` — warm brown accent, negative values in waterfall charts
- No generic "tech" blue. Text: Midnight on light backgrounds; avoid pure black.

### Fonts

- **Roughwell** — headlines/display (~48px)
- **Generation 1970 Light** — subheaders/CTAs (~24px)
- **Poppins** — body text, captions, small print. Google Fonts or `public/fonts/`

### Tone

- First-person plural (we, us). No exclamation points. No emojis. Oxford comma.
- Positive, approachable, elevated, authentic. Casual but rhythmic.

### Visual Style

- Warm cream backgrounds (`#EDE8DA`), white cards with thin borders, soft shadows, `border-radius: 12px`
- Clean, elevated, timeless. Flow IS: Welcoming, Elevated, Authentic, Calm, Soulful. Flow is NOT: Pretentious, Cheesy, Overbearing.

---

## Preferences

- **Design matters.** Be creative. Have taste. Make it look professional.
- **Numbers must tie.** Verify against the source. Re-read if a number looks wrong.
- **Match existing formats.** When given example slides/PDFs, match the formatting style exactly.
- **Iterate quickly.** Make changes, let the user review, adjust. Don't over-explain.
- **No `{{BRACKETS}}`** or programmer-style placeholders. Use clean, natural placeholder text.
- **Mobile optimization** on everything (except slide decks where it's optional).
- **Negatives in parentheses**: ($3.2M) not -$3.2M.
- **Images from Unsplash.** When we need stock/hero/background images, source them from Unsplash.
- **Never delete files.** Always move unwanted files to an `_Archive` folder instead.

---

## Package Manager: pnpm Only

All projects use **pnpm v10**. Never use npm or yarn for any operation.

- Use `pnpm add` / `pnpm add -g` — never `npm install`
- Use `pnpm dev`, `pnpm build`, `pnpm start` to run scripts
- Use `pnpm remove` to uninstall, `pnpm dlx` instead of `npx`

---

## Deployment

- All projects deploy via **GitHub → Vercel**.
- **Background build checks.** Before pushing, run `pnpm build` backgrounded so work continues in parallel. Check the build result before committing/pushing.

---

## Build Lifecycle

Every new project follows this sequence:

```
Idea → PRD → Tooling Audit → Plan → Scaffold → Build (70% MVP) → Polish → Ship
```

### PRD (Product Requirements Document)

When starting something new, generate a PRD before writing code. Structure:

1. Problem Statement
2. Target Users
3. Core Features (MVP)
4. Nice-to-Have (Post-MVP)
5. Data Sources and Integrations
6. Tech Stack
7. Design Notes (reference Flow brand)
8. Success Criteria
9. Open Questions

### Tooling Audit

After the PRD is generated, before planning: Scan the project requirements and recommend any additional tools, skills, or integrations that would help the build.

---

## Agent Workflow Rules

- **Plan before building.** Use plan mode for any non-trivial task.
- **Verify before marking done.** Run tests, check logs, demonstrate correctness.
- **Fix bugs autonomously.** Just fix it. Zero unnecessary back-and-forth.
- **If something goes sideways, stop and re-plan.**
