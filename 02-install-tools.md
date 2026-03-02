# Install Tools

This guide walks you through installing everything you need. Follow each section in order. If you get stuck on any step, describe the error to Claude or Cursor and it will help you troubleshoot.

---

## 1. Node.js

Node.js is the runtime that executes JavaScript outside of a browser. Our scripts, build tools, and package manager all depend on it.

1. Go to [https://nodejs.org](https://nodejs.org)
2. Download the **LTS** (Long Term Support) version -- it will be a button labeled something like "22.x LTS"
3. Run the installer. Accept all defaults. Click Next through each screen.
4. When it finishes, open a terminal (press `Win + R`, type `cmd`, press Enter) and run:

```
node --version
```

You should see a version number like `v22.x.x`. If you see an error, restart your computer and try again.

---

## 2. pnpm

pnpm is our package manager. It installs libraries and runs project scripts. We use pnpm exclusively -- never npm or yarn.

In the same terminal, enable Corepack (a Node.js tool that manages package managers) and activate pnpm:

```
corepack enable
corepack prepare pnpm@10.30.1 --activate
```

Verify it installed:

```
pnpm --version
```

You should see `10.30.1`.

---

## 3. Git

Git tracks changes to code and syncs with GitHub. Every project we build uses it.

1. Go to [https://git-scm.com/download/win](https://git-scm.com/download/win)
2. Download and run the installer. Accept all defaults.
3. After installation, open a new terminal and run:

```
git --version
```

You should see something like `git version 2.x.x`.

4. Configure your identity (replace with your actual name and email):

```
git config --global user.name "Your Name"
git config --global user.email "your.name@flow.life"
```

### Connect to GitHub

1. Go to [https://github.com](https://github.com) and sign in (or create an account)
2. In your terminal, run:

```
git config --global credential.helper manager
```

This stores your GitHub credentials so you do not have to type your password every time. The next time you push code, a browser window will open asking you to authorize Git. Click "Authorize."

---

## 4. Cursor

Cursor is our primary AI code editor.

1. Go to [https://cursor.com](https://cursor.com)
2. Click "Download" and install it
3. Open Cursor. It will ask you to sign in -- create an account or sign in with GitHub
4. When it opens, you will see a screen that looks like a code editor with a sidebar on the left and a chat panel on the right

### Quick Tour

- **Left sidebar**: file explorer (your project files)
- **Top bar**: file tabs (like browser tabs, but for code files)
- **Bottom panel**: terminal (where you run commands)
- **Right panel or `Ctrl+L`**: AI chat (where you talk to the agent)
- **`Ctrl+I`**: inline edit (highlight code and ask the AI to change it)
- **`Ctrl+Shift+P`**: command palette (search for any action)

To open a terminal inside Cursor: press `` Ctrl+` `` (the backtick key, above Tab).

To open a folder: File > Open Folder, then navigate to `C:\Users\YourName\CR Sandbox` (or wherever your workspace is).

---

## 5. Claude Desktop

Claude is our AI assistant for brainstorming, analysis, and planning.

1. Go to [https://claude.ai/download](https://claude.ai/download)
2. Download and install the desktop app
3. Sign in with your Anthropic account
4. You should see a chat interface where you can start conversations

We will configure Claude with Flow-specific knowledge in [04 - Claude Setup](04-claude-setup.md).

---

## 6. Create Your Workspace

If you do not already have a workspace folder:

1. Open File Explorer
2. Navigate to `C:\Users\YourName\`
3. Create a new folder for your workspace (e.g. `Flow Projects`)
4. Open Cursor
5. Go to File > Open Folder and select your new folder

This is your workspace. All projects live here.

---

## Verify Everything Works

Open a terminal in Cursor (`` Ctrl+` ``) and run each of these:

```
node --version
```
Expected: `v22.x.x`

```
pnpm --version
```
Expected: `10.30.1`

```
git --version
```
Expected: `git version 2.x.x`

If all three show version numbers, you are good to go.

---

## Next Step

Proceed to [03 - Cursor Setup](03-cursor-setup.md) to configure Cursor with Flow's rules, skills, and agents.
