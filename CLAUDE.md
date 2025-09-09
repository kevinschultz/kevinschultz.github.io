# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a GitHub Pages static site repository (`kevinschultz.github.io`) containing multiple HTML projects and kiosk applications. The repository serves as a collection of independent web applications rather than a single unified codebase.

## Project Structure

The repository contains several distinct projects:

- **Root**: Simple GitHub Pages landing page (`index.html`)
- **csm-team-general/**: Bootstrap-based team website with SCSS compilation
- **ogs-links-page/**: Links page with similar Bootstrap structure  
- **Kiosk Applications**: Multiple screener applications for different locations:
  - `mills-hall-kiosk-screener/`
  - `richards-kiosk-screener/` (with variants: `-door/`, `-ogs/`, `-sa/`)
- **Utilities**: `sl/`, `slate-checker/`, `webrtc-bard-test/`

## Architecture Notes

### Static Site Hosting
- Deployed via GitHub Pages
- No build process - direct HTML/CSS/JS serving
- Each project is self-contained with its own assets

### Bootstrap Projects (csm-team-general, ogs-links-page)
- Use Bootstrap 4+ framework
- SCSS source files in `assets/scss/` compile to `assets/css/main.css`
- Modular SCSS architecture with separate files for components
- jQuery-based interactions with plugins (carousel, lightbox, etc.)

### Kiosk Applications  
- Bootstrap-based screener forms
- Shared structure across variants (Richards location has multiple versions)
- Simple JavaScript for form interactions
- Consistent asset organization (css/, js/, assets/)

## Development Workflow

### SCSS Compilation
For Bootstrap projects with SCSS:
- Source files: `assets/scss/*.scss` 
- Output: `assets/css/main.css`
- Manual compilation required (no automated build process detected)

### File Organization
- Each project maintains independent asset folders
- Common pattern: `css/`, `js/`, `assets/` directories
- Images organized in `assets/img/` or `img/` subdirectories

### Testing
- No automated testing framework detected
- Manual browser testing for each project
- Test files exist (e.g., `test-box.html`) for kiosk applications

## Important Notes

- No package.json or build tools - pure static HTML/CSS/JS
- jsconfig.json exists for IDE autocomplete support only
- Multiple similar projects suggest template-based development approach  
- SCSS compilation must be handled manually or via IDE tools