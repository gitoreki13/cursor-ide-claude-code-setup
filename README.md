# Cursor IDE + Claude Code Setup

## Tools Installed

- **Cursor IDE** — AI-powered code editor (standalone app) downloaded from [cursor.com](https://cursor.com)
- **Node.js** — Required runtime to install Claude Code via npm, downloaded from [nodejs.org](https://nodejs.org)
- **Claude Code v2.1.146** — Anthropic's agentic coding CLI tool, installed via npm

## Steps Completed

1. Downloaded and installed **Cursor IDE** from [cursor.com](https://cursor.com)
2. Attempted to find Claude Code in Cursor's Marketplace — not listed there
3. Opened the built-in PowerShell terminal inside Cursor (`Ctrl+backtick`)
4. Installed Claude Code via the terminal using npm:
   ```
   npm install -g @anthropic-ai/claude-code
   ```
5. Launched Claude Code by running `claude` in the terminal
6. Selected a terminal theme and completed the setup wizard

## Issues Encountered & How I Solved Them

### Issue 1: Claude Code not in Cursor Marketplace
- **Problem:** Searching "Claude Code" in Cursor's Marketplace returned no results
- **Solution:** Installed Claude Code via the terminal using npm instead

### Issue 2: Node.js / npm not installed
- **Problem:** Running `npm install` gave the error: *"npm is not recognized as the name of a cmdlet"*
- **Solution:** Downloaded and installed Node.js LTS from [nodejs.org](https://nodejs.org), then restarted the terminal

### Issue 3: PowerShell Execution Policy blocked npm
- **Problem:** After installing Node.js, npm still failed with a `PSSecurityException / UnauthorizedAccess` error due to Windows PowerShell's script execution policy
- **Solution:** Ran the following command to allow scripts for the current user:
  ```
  Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
  ```
  Then re-ran the npm install command successfully