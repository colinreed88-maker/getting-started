---
name: generate-prd
description: Generate a Product Requirements Document for a new project or feature. Use when someone says "let's build something new," "generate a PRD," "new project," or wants to brainstorm and scope a build before writing code.
---

# Generate PRD

Structured workflow for turning an idea into a scoped, actionable PRD before any code gets written.

## Step 1: Discovery

Use the AskQuestion tool to gather requirements. Ask these in batches of 2-3:

**Batch 1:**
- What problem does this solve? (free text or options if the context suggests specific choices)
- Who are the users? Options: Just me, Flow team, External/public

**Batch 2:**
- What's the MVP scope? (Describe the core features — what ships first)
- What data sources does it need? Options: Hardcoded/placeholder data, External API, Database, None yet

**Batch 3:**
- Tech stack? Default: Next.js 15 + Tailwind + pnpm + Vercel. Ask if anything different.
- Any design references or existing patterns to follow? (existing pages, decks, screenshots)

If context from the conversation already answers some of these, skip those questions and confirm assumptions instead.

## Step 2: Generate PRD

Create `docs/prd.md` in the project folder with this structure:

```markdown
# [Project Name] — PRD

## Problem Statement
[One paragraph. Clear, specific. What pain point does this solve?]

## Target Users
[Who uses this and how. Be specific about the audience.]

## Core Features (MVP)
1. [Feature — ships first]
2. [Feature — ships first]
3. [Feature — ships first]

## Nice-to-Have (Post-MVP)
1. [Feature — comes later]
2. [Feature — comes later]

## Data Sources and Integrations
- [Source]: [How it connects, what data flows]

## Tech Stack
- Framework: Next.js 15 (App Router)
- Styling: Tailwind CSS
- Package manager: pnpm v10
- Deployment: GitHub → Vercel
- [Any additional libraries or services]

## Design Notes
- Background: Moonlight #F3EDDF / warm cream #EDE8DA
- Text: Midnight #3D3D3D (never pure black)
- Accents: Sunlight #E89700 (CTAs), Ocean Swell #7DADBB (secondary)
- Cards: white, border-radius 12px, soft shadows
- Fonts: Roughwell (headlines), Poppins (body)
- [Any specific layout or UX references]

## Success Criteria
- [ ] [Measurable outcome]
- [ ] [Measurable outcome]

## Open Questions
- [Unresolved decision or dependency]
```

## Step 3: Tooling Audit

After saving the PRD, evaluate the project's needs:

1. **Review installed tools**: check `.cursor/rules/`, `.cursor/agents/`, installed skills, MCP servers
2. **Identify gaps**: does the PRD reference tech, APIs, or patterns we don't have rules/skills for?
3. **Recommend**: present a short list of suggested additions with rationale. The user approves before installing.

Present the audit as a brief summary:
- Already covered: [list what rules/agents/skills apply]
- Recommended additions: [list with one-line rationale each]
- Not needed: [anything considered but skipped, with reason]

## Step 4: Hand Off to Planning

After the user approves the PRD and tooling audit:

1. Enter plan mode
2. Break the MVP into 5 build phases: Scaffold, Wire Data, Style, Harden, Ship
3. Create todos for each phase
4. Begin execution with Phase 1 (Scaffold)

## Conventions

- No placeholder brackets like `{{PROJECT_NAME}}`. Use clean, natural text.
- No confidential numbers. Use realistic dummy data if examples are needed.
- The PRD is a living document — update it as scope evolves during the build.
