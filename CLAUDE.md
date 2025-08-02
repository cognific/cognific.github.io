# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is the GitHub Pages repository for cognific.ai, a modern static website with SEO optimization and accessibility features. The repository structure:
- `index.html` - Main coming soon page with comprehensive SEO meta tags, accessibility features, and email signup
- `styles.css` - Separate CSS file with CSS custom properties, animations, and responsive design
- `CNAME` - GitHub Pages custom domain configuration pointing to cognific.ai
- `favicon.svg`, `site.webmanifest` - Brand assets and PWA configuration
- `robots.txt`, `sitemap.xml` - SEO files for search engine crawling
- `.github/workflows/claude-code.yml` - GitHub Actions workflow for Claude Code integration

## Project Structure

This is a progressive static website with:
- Separate HTML and CSS files for better maintainability
- Progressive enhancement approach (works without JavaScript)
- SEO optimization with Open Graph and Twitter Card meta tags
- Full accessibility support (ARIA labels, skip links, screen reader support)
- No build process or dependencies - pure HTML/CSS/vanilla JS

## Development Commands

### Local Development
```bash
# Preview changes locally
open index.html  # macOS
xdg-open index.html  # Linux

# Start a local HTTP server (optional, for testing)
python -m http.server 8000  # Python 3
# or
python -m SimpleHTTPServer 8000  # Python 2
```

### File Validation
```bash
# Validate HTML (requires npm install -g html-validator)
html-validator --file=index.html

# Check for broken links
# No automated tool configured - manually verify all links work
```

## Code Architecture

### HTML Structure (`index.html`)
- Comprehensive `<head>` section with SEO, Open Graph, Twitter Card meta tags
- Security headers via meta tags (CSP, X-Frame-Options, etc.)
- Semantic HTML5 with proper ARIA attributes
- Email signup form with progressive enhancement (works with/without JS)
- Simple JavaScript for form handling that degrades gracefully

### CSS Architecture (`styles.css`)
- CSS custom properties for theming and maintenance
- Mobile-first responsive design using `clamp()` for fluid typography
- Accessibility features: skip links, reduced motion support, high contrast mode
- Performance optimized animations using `transform` and `opacity`
- Print styles for clean output

### Key Features
1. **Email Signup**: Form submits to `mailto:contact@cognific.ai` with JavaScript enhancement for better UX
2. **Social Links**: Twitter/X, LinkedIn, GitHub links with proper `rel` attributes
3. **Animations**: Pulsing border and flickering title with reduced motion support
4. **SEO**: Canonical URL, meta descriptions, Open Graph, Twitter Cards, sitemap.xml, robots.txt

## Deployment Workflow

### GitHub Pages Deployment
The site automatically deploys to cognific.ai when changes are pushed to the `main` branch.

### Git Workflow
1. Current branch is `develop` (main branch is `main`)
2. Create feature branches from `develop`
3. Test locally before committing
4. Create PRs to merge into `main`
5. Site deploys automatically after merge to `main`

### Claude Code Integration
- PR comments with `/claude-code` trigger the GitHub Action
- PRs with `claude-code` label automatically run Claude Code
- Configured via `.github/workflows/claude-code.yml`

## Design System

### Color Palette (CSS Variables)
- Primary: `#00ff00` (green) - text and borders
- Accent: `#ff0000` (red) - title glow effect
- Background: `#0a0a0a` (near black) with gradient overlays
- Font: `'Courier New', Courier, monospace` with system font fallbacks

### Animation Timing
- Pulse animation: 3s ease-in-out infinite
- Flicker animation: 3s ease-in-out infinite
- All transitions: 0.3s ease

### Responsive Breakpoints
- Mobile: max-width 768px
- Extra small: max-width 480px
- Fluid typography using `clamp()` for all screen sizes