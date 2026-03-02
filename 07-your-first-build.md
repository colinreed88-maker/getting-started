# Your First Build

This guide walks you through building a simple Flow-branded page from start to finish, using the full workflow. Set aside about 45 minutes.

---

## What We Are Building

A **Team Directory** page -- a clean, branded grid of team members with photos, names, titles, and contact info. Simple enough to complete in one session, complex enough to use every part of the workflow.

---

## Phase 1: Generate the PRD

Open Cursor. Start a new chat and type:

```
Generate a PRD for a team directory page. It should show team members in a 
card grid with photos, names, titles, and email addresses. Flow brand 
styling. Deploy to Vercel. Use placeholder data for now.
```

The AI will ask you a few scoping questions. Answer them:

- **Users:** Flow team members (internal)
- **MVP scope:** A single page with a responsive card grid, search/filter, and placeholder photos from Unsplash
- **Data source:** Hardcoded array for now (we can connect a database later)
- **Design reference:** "Clean, warm, Flow brand" (the AI already knows what this means)

Review the PRD it generates. Does it match what you want? Adjust if needed, then confirm.

---

## Phase 2: Plan and Scaffold

Tell Cursor:

```
Plan this build.
```

The AI will outline the phases:

1. Scaffold a Next.js 15 project with Tailwind and pnpm
2. Create the page route and layout
3. Build the team card component
4. Add search/filter functionality
5. Style everything with Flow brand tokens
6. Deploy to Vercel

Review the plan. If it looks right, tell the AI to proceed:

```
Looks good. Start building.
```

---

## Phase 3: Build and Review

The AI will:

1. Create the project structure
2. Install dependencies with pnpm
3. Create the page with placeholder data
4. Apply Flow brand styling (Moonlight background, Midnight text, card shadows, Poppins font)

At around 70% completion, the AI should run a build check. Watch for this in the terminal output -- if it passes, the project is structurally sound.

**Review it live.** The AI will deploy to Vercel or you can run `pnpm dev` locally to preview. Look for:

- Do the colors match Flow's brand? (Cream background, dark charcoal text, warm accents)
- Are the cards well-spaced and visually balanced?
- Does it work on mobile? (Resize your browser to check)
- Does the search filter work?

If something is off, describe what you want changed:

```
The cards need more spacing between them. And make the name text larger.
```

---

## Phase 4: Polish and Ship

Once the core page works, refine:

```
Add a subtle hover effect on the cards. Make sure the page has a proper 
title and description. Add a Flow logo in the header.
```

When you are satisfied:

```
Run a final build check and deploy.
```

The AI will:
1. Run `pnpm build` to verify no errors
2. Commit and push to GitHub
3. Vercel deploys automatically
4. Share the live URL

---

## What Just Happened

You built a production-ready, Flow-branded web page without writing code from scratch. Here is what the AI handled:

- **Project scaffolding** -- Next.js, Tailwind, pnpm, all configured
- **Component architecture** -- Card component, layout, search logic
- **Brand application** -- Colors, fonts, spacing, visual style
- **Responsive design** -- Works on desktop and mobile
- **Deployment** -- GitHub + Vercel, live in production

And here is what you handled:

- **Defining the need** -- What to build and why
- **Reviewing the PRD** -- Ensuring the scope was right
- **Quality judgment** -- Is this good enough? Does it feel like Flow?
- **Iteration direction** -- "More spacing," "larger text," "add a hover effect"

This is the pattern for everything you build going forward. The AI writes the code; you bring the taste, the judgment, and the domain knowledge.

---

## What to Try Next

Now that you have completed the full cycle, try these on your own:

1. **Add a detail view** -- Click a team member card to see their full profile
2. **Create a slide deck** -- Use the deck-builder agent to make a team overview presentation
3. **Build a dashboard** -- A page with metrics, charts, and summary cards

Each one follows the same lifecycle: PRD → Plan → Build → Review → Ship.

---

## Reference

See [08 - Reference](08-reference.md) for a quick-lookup cheat sheet of commands, brand values, and tool shortcuts.
