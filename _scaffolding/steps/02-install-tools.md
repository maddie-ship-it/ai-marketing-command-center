---
step: 2
title: "Install Missing Tools"
estimated_time: "5-10 minutes"
produces: "Git, Node.js, and Live Server extension installed and verified"
---

# Step 2: Install Missing Tools

## Goal

Get Git, Node.js, and the Live Server extension installed on your machine. Claude handles this for you — just approve the commands when prompted.

## Context

These three tools complete your development environment:
- **Git** — tracks changes to your files and pushes them to GitHub (your backup + collaboration layer)
- **Node.js** — a runtime that many developer tools need (including some Claude features)
- **Live Server** — a VSCode extension that lets you preview your pages in a browser as you build them

## Exercise

### Part A: Install Git

Claude will check if Git is already installed. If not:

- **Mac:** Claude runs `xcode-select --install` which installs Apple's developer tools (includes Git). A popup will appear — click "Install" and wait a few minutes.
- **Windows:** Claude will give you a direct download link to git-scm.com. Download, run the installer, click through with defaults.

### Part B: Install Node.js

Claude will check if Node.js is already installed. If not:

- **Mac:** Claude runs `brew install node` (if Homebrew is installed) or gives you the nodejs.org download link
- **Windows:** Claude gives you the nodejs.org LTS download link. Download, run installer, click through with defaults.

After install, Claude verifies with `node --version`.

### Part C: Install Live Server Extension

Claude runs:
```bash
code --install-extension ritwickdey.LiveServer
```

This installs the Live Server extension into VSCode. You'll use it in Step 5 to preview your site before pushing it live.

## Verify

Claude will run these checks:

```bash
git --version     # Should show a version number
node --version    # Should show a version number
```

And the Live Server extension should appear in your VSCode Extensions sidebar.

## Next

When this step is complete, say: **"Step 2 done. Ready for step 3."**
