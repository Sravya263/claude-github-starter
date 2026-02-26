# 🤖 Claude + GitHub Starter Project

A ready-to-use template for integrating Claude AI into your GitHub workflow.
Includes a GitHub Actions workflow, a `CLAUDE.md` config, and a setup guide.
---
## ✨ Features

- **`@claude` mentions** — Tag Claude in any PR or issue comment to get AI assistance
- **Auto PR reviews** — Claude automatically reviews new pull requests
- **`CLAUDE.md`** — Teach Claude your project's coding standards, commands, and context
- **Claude Projects sync** — Instructions for connecting your repo to claude.ai Projects

---
## 🚀 Quick Setup

### Step 1 – Add your Anthropic API Key to GitHub Secrets

1. Go to your repo → **Settings** → **Secrets and variables** → **Actions**
2. Click **New repository secret**
3. Name: `ANTHROPIC_API_KEY`
4. Value: your key from [console.anthropic.com](https://console.anthropic.com)

> Don't have a key? Sign up at [anthropic.com](https://www.anthropic.com)

---

### Step 2 – Copy these files into your repo

```
your-repo/
├── CLAUDE.md                          ← Edit this with your project context
└── .github/
    └── workflows/
        └── claude.yml                 ← GitHub Actions workflow (no edits needed)
```

---

### Step 3 – Edit `CLAUDE.md`

Open `CLAUDE.md` and fill in the **TODO** sections:
- Project description
- Folder structure
- Dev commands (install, run, test, lint, build)
- Coding standards
- What Claude should and shouldn't touch

The more context you give, the better Claude performs.

---

### Step 4 – Try it out

Open any PR or issue and comment:

```
@claude Can you review this and suggest improvements?
```

```
@claude Fix the failing test in src/utils.js
```

```
@claude Refactor this function to be more readable
```

Claude will respond directly in the thread.

---

## 🔗 Connect to Claude Projects (claude.ai)

For even deeper context, sync your repo with a Claude Project:

1. Go to [claude.ai](https://claude.ai) → open or create a **Project**
2. Click **Add content** → **GitHub**
3. Authorize GitHub and select your repository
4. Choose which branches/files to sync
5. Click **Sync** — Claude now has full codebase context in chat

**Best for:** asking questions about your codebase, generating code, planning features, writing docs.

---

## ⚙️ Workflow Customization

Edit `.github/workflows/claude.yml` to adjust behavior:

| Setting | Description |
|---|---|
| `max_turns` | Limit how many steps Claude takes (default: unlimited) |
| `direct_prompt` | Custom prompt for auto-triggered jobs (e.g., PR review) |
| `on:` triggers | Add/remove events that activate Claude |

---

## 📁 File Reference

| File | Purpose |
|---|---|
| `CLAUDE.md` | Project context, rules, and commands for Claude |
| `.github/workflows/claude.yml` | GitHub Actions workflow — triggers Claude |
| `README.md` | This setup guide |

---

## 🛡️ Security Notes

- Your `ANTHROPIC_API_KEY` is stored as a GitHub Secret and never exposed in logs
- Claude only has permissions defined in the workflow's `permissions:` block
- Claude cannot push to protected branches unless you explicitly configure it
- Review Claude's suggested changes before merging

---

## 🙋 Need Help?

- [Claude Code Docs](https://docs.claude.com/en/docs/claude-code/github-actions)
- [Anthropic Quickstarts on GitHub](https://github.com/anthropics/anthropic-quickstarts)
- [Claude Projects Guide](https://support.claude.ai)
