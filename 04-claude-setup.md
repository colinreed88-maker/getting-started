# Claude Setup

This guide configures the Claude Desktop app with Flow's brand standards and workflow context. After this, Claude will know our brand, our conventions, and how we like to work.

---

## What is Claude Desktop?

Claude is an AI assistant made by Anthropic. The Desktop app lets you have conversations, upload documents, and work through complex analysis. We configure it with a "Project" that pre-loads Flow's context so you do not have to explain who we are in every conversation.

---

## 1. Install Claude Desktop

1. Download from [claude.ai/download](https://claude.ai/download)
2. Install and sign in (you will need an Anthropic account or use our team account)
3. Verify: Claude opens and you can start a conversation

---

## 2. Create a Flow Project

Claude Projects let you attach persistent instructions and reference files.

1. In Claude Desktop, click the **Projects** icon in the sidebar
2. Click **Create a project**
3. Name it: `Flow Development`
4. In the project settings, find **Custom Instructions**
5. Open the file `getting-started-flow/config/claude-project-instructions.md`
6. Copy everything below the `---` line and paste it into the Custom Instructions field
7. Click **Save**

---

## 3. Upload Brand Assets (Optional)

You can upload reference files to the project so Claude can see them in every conversation:

- The brand guide (`config/brand-guide.html` — save as PDF first, or paste the key sections as text)
- Any example slides or pages you want Claude to match

To upload: Open the project > click **Add content** > upload files.

---

## 4. Verify It Works

Start a new conversation inside the Flow Development project and type:

```
What are Flow's brand colors and fonts?
```

Claude should respond with the correct hex codes (Moonlight, Midnight, Sunlight, etc.) and font names (Roughwell, Generation 1970, Poppins). If it does, the project instructions are working.

---

## When to Use Claude vs Cursor

| Use Claude Desktop When | Use Cursor When |
|------------------------|-----------------|
| Brainstorming ideas | Building or editing code |
| Writing project briefs (PRDs) | Creating dashboards and pages |
| Analyzing documents or data | Working with HTML slide decks |
| Working through strategy | Deploying to Vercel |
| Quick questions about Flow | Any task that involves files |

They complement each other. Start ideas in Claude, build them in Cursor.

---

## Next Step

Proceed to [05 - Flow Domain Knowledge](05-flow-domain-knowledge.md) to learn how Flow is structured and the domain context the AI needs.
