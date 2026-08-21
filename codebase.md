# Codebase Architecture

## Project Overview

This is a static web application project built with semantic HTML5. The architecture follows a minimalist approach, prioritizing clarity and maintainability over complexity.

## Directory Structure

```
hello-world/
├── index.html           # Main application entry point
│                        # Contains the Hello World display
├── README.md            # Project overview and quick start guide
├── agents.md            # Automation and workflow documentation
├── codebase.md          # This file - architecture documentation
├── design.md            # Design principles and standards
├── changelog.md         # Version history and release notes
└── .gitignore           # Git configuration (untracked files)
```

## Core Components

### index.html
**Purpose**: Main application entry point

**Structure**:
- DOCTYPE declaration
- HTML5 semantic markup
- Head metadata (charset, viewport)
- Body content (Hello World message)

**Standards**: Follows W3C HTML5 specifications

## Technology Stack

| Layer | Technology |
|-------|------------|
| Markup | HTML5 |
| Styling | CSS (minimal) |
| Scripting | None |
| Build Tools | Git |

## Design Patterns

1. **Static Site** - No server-side processing required
2. **Single Page Application** - Single entry point (index.html)
3. **Progressive Enhancement** - Content accessible without JavaScript

## File Descriptions

| File | Purpose | Audience |
|------|---------|----------|
| index.html | Application core | End users |
| README.md | Getting started | Developers |
| codebase.md | Technical reference | Developers |
| design.md | Standards & guidelines | Developers |
| agents.md | Automation workflows | DevOps/Developers |
| changelog.md | Version history | All stakeholders |
