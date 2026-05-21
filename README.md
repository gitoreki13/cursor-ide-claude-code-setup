How to Set Up Cursor IDE with Claude Code on Windows
A beginner-friendly step-by-step guide to installing Cursor IDE and Claude Code.

Prerequisites

A Windows PC
An Anthropic account (sign up at anthropic.com)


Step 1: Install Cursor IDE

Go to cursor.com
Download the installer for Windows
Run the installer and follow the on-screen steps


Step 2: Install Node.js
Claude Code requires Node.js to install via npm.

Go to nodejs.org
Download the LTS version (recommended)
Run the installer and click through the steps
Restart your computer after installation


Step 3: Fix PowerShell Execution Policy (Windows Only)
Windows blocks npm scripts by default. You need to allow them first.

Open the terminal inside Cursor using Ctrl+` (backtick)
Run this command:

   Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned

When prompted, type Y and press Enter


Step 4: Install Claude Code
In the same terminal, run:
npm install -g @anthropic-ai/claude-code
Wait for it to finish — it should say "added 2 packages".

Step 5: Launch Claude Code

In the terminal, run:

   claude

Select your preferred theme (e.g. Dark mode)
Sign in with your Anthropic account when prompted
Claude Code is now running inside Cursor!


Troubleshooting
ProblemSolutionnpm is not recognizedInstall Node.js from nodejs.org and restart the terminalUnauthorizedAccess errorRun Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSignedClaude Code not found in Cursor MarketplaceInstall via terminal using npm (see Step 4)

Notes

Claude Code is not available in Cursor's built-in Marketplace — it must be installed via the terminal
These instructions are for Windows. Mac/Linux users do not need the PowerShell execution policy fix
