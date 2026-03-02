# Reference

Quick-lookup cheat sheet. Bookmark this page.

---

## Brand Colors

| Name | Hex | CSS Variable |
|------|-----|-------------|
| Moonlight | `#F3EDDF` | `--color-moonlight` |
| Midnight | `#3D3D3D` | `--color-midnight` |
| Sunlight | `#E89700` | `--color-sunlight` |
| Heart | `#F99AA9` | `--color-heart` |
| Ocean Swell | `#7DADBB` | `--color-ocean-swell` |
| Olive | `#767317` | `--color-olive` |
| Roots | `#8C4500` | `--color-roots` |

Background surface: `#EDE8DA`

---

## Brand Fonts

| Font | Usage | Weight |
|------|-------|--------|
| Roughwell | Headlines, display | Regular |
| Generation 1970 Light | Subheaders, CTAs | Light |
| Poppins | Body text | 300-700 |

---

## Common Commands

```
pnpm dev          # Start local dev server
pnpm build        # Production build (run before deploying)
pnpm add <pkg>    # Install a package
pnpm remove <pkg> # Uninstall a package
pnpm dlx <cmd>    # Run a one-off command (replaces npx)
```

---

## Git Basics

```
git status           # See what changed
git add .            # Stage all changes
git commit -m "msg"  # Commit with message
git push             # Push to GitHub (Vercel auto-deploys)
```

---

## Cursor Shortcuts

| Action | Shortcut |
|--------|----------|
| Open AI chat | `Ctrl+L` |
| Open terminal | `` Ctrl+` `` |
| Open command palette | `Ctrl+Shift+P` |
| Toggle sidebar | `Ctrl+B` |

---

## Custom Agents

| Agent | Use When |
|-------|----------|
| `project-launcher` | Starting a brand new project |
| `deck-builder` | Creating or editing slide decks |

---

## Build Lifecycle

```
Idea → PRD → Tooling Audit → Plan → Scaffold → Build (70%) → Polish → Ship
```

---

## File Structure (Typical Next.js Project)

```
my-project/
├── .cursor/
│   ├── rules/         # AI rules (brand, conventions)
│   └── agents/        # AI agent definitions
├── public/
│   ├── fonts/         # Roughwell, Gen1970, Poppins
│   └── logos/         # Flow logo variants
├── src/
│   └── app/           # Next.js App Router pages
├── package.json
├── pnpm-lock.yaml
├── tailwind.config.ts
└── CLAUDE.md          # Claude Code memory (if using CLI)
```

---

## Tailwind Brand Config

```js
// tailwind.config.ts — extend with Flow colors
colors: {
  moonlight: '#F3EDDF',
  midnight: '#3D3D3D',
  sunlight: '#E89700',
  heart: '#F99AA9',
  'ocean-swell': '#7DADBB',
  olive: '#767317',
  roots: '#8C4500',
  'flow-bg': '#EDE8DA',
}
```

---

## Financial Formatting

| Format | Example |
|--------|---------|
| Millions | $4.2M |
| Thousands | $150K |
| Negatives | ($3.2M) not -$3.2M |
| Exact amounts | $4,231.50 |

---

## Useful Prompts

**Starting a project:**
> "Generate a PRD for [describe what you need]"

**Getting help:**
> "What files exist in this project and what do they do?"

**Fixing something:**
> "This is broken: [paste error]. Fix it."

**Brand check:**
> "Does this page follow Flow brand guidelines? Check colors, fonts, and spacing."

**Deploying:**
> "Run a build check and deploy to Vercel."

---

## Getting Help

- **Cursor docs:** [cursor.com/docs](https://www.cursor.com/docs)
- **Claude docs:** [docs.anthropic.com](https://docs.anthropic.com)
- **Next.js docs:** [nextjs.org/docs](https://nextjs.org/docs)
- **Tailwind docs:** [tailwindcss.com/docs](https://tailwindcss.com/docs)
- **pnpm docs:** [pnpm.io](https://pnpm.io)

For Flow-specific questions, ask your manager or the team channel.
