# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is the GitHub Pages repository for cognific.ai, a simple static website hosted on GitHub Pages. The repository contains:
- `index.html` - The main coming soon page with a dark hacker theme
- `CNAME` - GitHub Pages custom domain configuration pointing to cognific.ai
- `.github/workflows/claude-code.yml` - GitHub Actions workflow for Claude Code integration

## Project Structure

This is a minimal static website with no build process or dependencies:
- Single HTML file with embedded CSS
- No JavaScript framework or build tools
- Hosted directly via GitHub Pages

## Development Workflow

### Local Development
To preview changes locally:
```bash
# Open the HTML file directly in a browser
open index.html  # macOS
# or
xdg-open index.html  # Linux
# or simply drag the file to your browser
```

### Deployment
The site automatically deploys to cognific.ai when changes are pushed to the `main` branch via GitHub Pages.

### Git Workflow
1. Create feature branches from `main`
2. Make changes and test locally
3. Create pull requests to merge into `main`
4. Site deploys automatically after merge

## Design Guidelines

The current design follows a dark hacker aesthetic with:
- Dark background (#0a0a0a) with subtle gradients
- Green accent color (#00ff00) for text and borders
- Red glow effect on the main title
- Monospace font (Courier New) throughout
- Centered layout with glowing border effect
- Responsive design using CSS clamp() for fluid typography