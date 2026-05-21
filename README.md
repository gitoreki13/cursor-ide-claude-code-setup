# How to Set Up Cursor IDE with Claude Code on Windows

A beginner-friendly step-by-step guide to installing Cursor IDE and Claude Code.

---

## Prerequisites

- A Windows PC
- An Anthropic account (sign up at [anthropic.com](https://anthropic.com))

---

## Step 1: Install Cursor IDE

1. Go to [cursor.com](https://cursor.com)
2. Download the installer for Windows
3. Run the installer and follow the on-screen steps

---

## Step 2: Install Node.js

Claude Code requires Node.js to install via npm.

1. Go to [nodejs.org](https://nodejs.org)
2. Download the **LTS** version (recommended)
3. Run the installer and click through the steps
4. Restart your computer after installation

---

## Step 3: Fix PowerShell Execution Policy (Windows Only)

Windows blocks npm scripts by default. You need to allow them first.

1. Open the terminal inside Cursor using **Ctrl+`** (backtick)
2. Run this command:
   ```
   Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
   ```
3. When prompted, type **Y** and press **Enter**

---

## Step 4: Install Claude Code

In the same terminal, run:

```
npm install -g @anthropic-ai/claude-code
```

Wait for it to finish — it should say "added 2 packages".

---

## Step 5: Launch Claude Code

1. In the terminal, run:
   ```
   claude
   ```
2. Select your preferred theme (e.g. Dark mode)
3. Sign in with your Anthropic account when prompted
4. Claude Code is now running inside Cursor!

---

## Troubleshooting

| Problem | Solution |
|---|---|
| `npm` is not recognized | Install Node.js from [nodejs.org](https://nodejs.org) and restart the terminal |
| `UnauthorizedAccess` error | Run `Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned` |
| Claude Code not found in Cursor Marketplace | Install via terminal using npm (see Step 4) |

---

## Notes

- Claude Code is **not** available in Cursor's built-in Marketplace — it must be installed via the terminal
- These instructions are for **Windows**. Mac/Linux users do not need the PowerShell execution policy fix
