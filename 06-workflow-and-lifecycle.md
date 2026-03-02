# Workflow and Lifecycle

This guide covers the structured process for building things at Flow. Following this process ensures quality, consistency, and speed.

---

## The Build Lifecycle

Every project follows this sequence:

```
Idea → PRD → Tooling Audit → Plan → Scaffold → Build (70% MVP) → Polish → Ship
```

Do not skip steps. The upfront work (PRD, plan) saves hours of rework later.

### 1. Idea

Start with a clear problem or need. "We need a way to track weekly KPIs" or "The team needs a branded landing page for the event."

### 2. PRD (Product Requirements Document)

Before building anything, scope it. In Cursor, say "generate a PRD" and the AI will walk you through structured questions:

- What problem does this solve?
- Who are the users?
- What is the MVP scope?
- What data does it need?
- Any design references?

The output is a markdown document that becomes the blueprint for the build.

### 3. Tooling Audit

After the PRD, the AI evaluates whether you need any additional skills, integrations, or tools. For example:

- A data-heavy project might need a database connection
- A slide deck might need the deck-builder agent
- A complex multi-page app might need specific routing patterns

### 4. Plan

The AI creates a phased build plan. Review it before proceeding. Plans should be:

- Specific (file paths, component names)
- Phased (what to build first, second, third)
- Reviewable (you can see intermediate progress)

### 5. Scaffold

Project setup: create the repo, install dependencies, configure brand tokens, set up routing. The AI handles this automatically.

### 6. Build (70% MVP)

Build to 70% completion. At this point, deploy and review it live. This is where you catch fundamental issues before investing in polish.

### 7. Polish

Responsive design, edge cases, error handling, visual refinement. Iterate on feedback.

### 8. Ship

Final build check, deploy to Vercel, confirm everything works in production.

---

## Using Custom Agents

Cursor supports specialized agents that have domain expertise. To use one, mention it in your chat.

### Available Agents

**Project Launcher**
Best for: Starting something brand new
Trigger: "Let's build something new" or "start a new project"
What it does: Orchestrates the full lifecycle -- generates a PRD, runs the tooling audit, creates a plan, scaffolds the project, then delegates the build.

**Deck Builder**
Best for: Creating or editing HTML slide decks
Trigger: "Create a slide deck" or "edit the presentation"
What it does: Manages the slide template system, applies brand CSS, creates charts with the Flow color palette, handles slide structure and navigation.

---

## Plan Mode

For any non-trivial task, ask Cursor to plan first:

```
Plan: Build a team directory page with photos and contact info
```

The AI will outline its approach, list the files it will create or edit, and describe the structure. Review and approve before it starts building.

This catches misunderstandings early. If the plan does not match what you had in mind, correct it before any code is written.

---

## Common Workflow Patterns

### "I need a new page on an existing site"

1. Tell Cursor what the page should show and where it fits
2. The AI creates the route, component, and styling
3. Review, iterate, deploy

### "I need a branded slide deck"

1. Activate the deck-builder agent
2. Describe the slides: titles, content, any charts or tables
3. The AI generates HTML slides with Flow branding
4. Review in browser, adjust, ship as PDF or HTML

### "Something is broken"

1. Describe the bug: what you expected vs what happened
2. Paste any error messages
3. The AI diagnoses, fixes, and verifies the fix
4. Do not accept the fix until you see it working

### "I want to try a new idea"

1. Start in Claude Desktop for brainstorming
2. Generate a PRD in Cursor when the idea is clear
3. Follow the full lifecycle

---

## Key Principles

- **Plan before building.** Always.
- **Review at 70%.** Do not wait until the end to look at the output.
- **Verify before marking done.** The AI should prove it works, not just say it does.
- **If something goes sideways, stop and re-plan.** Do not push forward on a broken foundation.
- **Never delete files.** Move to `_Archive` instead.

---

## Next Step

Proceed to [07 - Your First Build](07-your-first-build.md) for a hands-on walkthrough.
