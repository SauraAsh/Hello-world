# Code Style Guide

Coding standards and conventions for this project.

---

## 📋 Overview

This guide ensures consistency across all files and makes code easier to read, maintain, and contribute to.

---

## 🔤 Naming Conventions

### Files
- Use **lowercase with hyphens**: `index-en.html`, `HTML-TAG-DOCUMENTATION.md`
- Descriptive names: `index.html` not `page.html`
- Use language codes for multilingual: `index-[lang-code].html`

### HTML Elements
- Use **lowercase**: `<div>`, `<p>`, `<h1>`
- Never: `<Div>`, `<P>`, `<H1>`

### CSS Classes (if used)
- Use **kebab-case**: `hello-world`, `main-content`
- Descriptive: `main-navigation` not `nav1`
- Semantic: `primary-button` not `blue-button`

### IDs (if used)
- Use **kebab-case**: `main-content`, `page-header`
- Unique per page
- Meaningful and descriptive

---

## 🗂️ File Organization

### Directory Structure
```
hello-world/
├── Documentation files (README.md, etc.)
├── multilingual/
│   ├── HTML files
│   └── Documentation specific to multilingual
└── Assets/ (when images/CSS are added)
```

### File Grouping
- Keep related files together
- Group by language in multilingual/
- Separate documentation from application files

---

## 💻 HTML Formatting

### Indentation
- Use **2 spaces** (not tabs)
- Consistent throughout file
- Indent nested elements

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Page Title</title>
</head>
<body>
  <h1>Main Title</h1>
  <p>Paragraph text</p>
</body>
</html>
```

### Line Length
- Keep lines **80 characters** or less (readable in all editors)
- Break long attributes onto new lines

```html
<!-- Good -->
<meta name="viewport" 
      content="width=device-width, initial-scale=1.0">

<!-- Avoid -->
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
```

### Element Attributes
- Use **double quotes**: `lang="en"` not `lang='en'`
- Order: `id`, `class`, `lang`, `data-*`
- One attribute per line if multiple

```html
<!-- Good -->
<html 
  lang="en"
  id="app">

<!-- Avoid -->
<html lang="en" id="app" class="main">
```

### Self-Closing Tags
- Always close: `<meta />`, `<img />`
- Or modern HTML: `<meta>`, `<img>`
- Consistent within file

```html
<!-- Modern HTML5 (acceptable) -->
<meta charset="UTF-8">
<img src="image.jpg" alt="Description">

<!-- Self-closing (also acceptable) -->
<meta charset="UTF-8" />
<img src="image.jpg" alt="Description" />
```

---

## 📝 Comments

### Comment Format
```html
<!-- Clear description of what this does -->
```

### Single Line Comments
```html
<!-- HTML declaration specifies this is an HTML5 document -->
<html lang="en">
```

### Multi-Line Comments
```html
<!--
  Main application structure
  - Header with navigation
  - Main content area
  - Footer
-->
<body>
  ...
</body>
```

### Section Dividers (for large files)
```html
<!-- ============== Navigation Section ============== -->
<nav>...</nav>

<!-- ============== Main Content ============== -->
<main>...</main>
```

### Documentation Comments
- Explain **why**, not just what
- Use in different languages for multilingual files
- Keep concise but complete

```html
<!-- Multilingual comment example -->
<!-- This loads user data from API -->
<!-- Cargamos los datos del usuario desde la API -->
```

### Comment Placement
- Place comment above the element it describes
- Use in-line only for brief clarifications
- Comment complex logic

```html
<!-- Good -->
<!-- Main page heading -->
<h1>Hello World</h1>

<!-- Avoid -->
<h1>Hello World</h1> <!-- Main page heading -->
```

---

## 🏗️ HTML Structure

### Semantic Markup
- Use semantic elements: `<header>`, `<main>`, `<footer>`, `<section>`, `<article>`
- Use `<strong>` for important, `<em>` for emphasis
- Never use `<div>` for semantic content

### Heading Hierarchy
- Use `<h1>` for main page title (one per page)
- Use proper hierarchy: h1 → h2 → h3 (no skipping)
- Never use for styling

```html
<!-- Good -->
<h1>Main Title</h1>
<h2>Section</h2>
<h3>Subsection</h3>

<!-- Avoid -->
<h1>Main Title</h1>
<h3>Subsection</h3> <!-- Skipped h2 -->
```

### Document Structure
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <!-- Meta tags (first) -->
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  
  <!-- Title -->
  <title>Page Title</title>
  
  <!-- Styles (if any) -->
  <style>
    /* CSS here */
  </style>
</head>
<body>
  <!-- Main content -->
  
  <!-- Scripts (if any) -->
  <script>
    // JavaScript here
  </script>
</body>
</html>
```

---

## 🌐 Character Encoding

### Always Use UTF-8
```html
<meta charset="UTF-8">
```

### File Encoding
- Save files as UTF-8 without BOM
- Configure in editor: UTF-8
- Verify in version control

### Multilingual Considerations
- Supports all languages and special characters
- Required for emoji and symbols
- Standard for web content

---

## 🌍 Language Attributes

### HTML Language
```html
<html lang="en">
<!-- Always include lang attribute -->
<!-- Use ISO 639-1 codes: en, fr, es, de, etc. -->
```

### Content Language Changes
```html
<p>
  This is English text.
  <span lang="es">Este es texto en español.</span>
</p>
```

---

## ♿ Accessibility Standards

### Alt Text for Images
```html
<!-- Good -->
<img src="logo.png" alt="Company logo">

<!-- Avoid -->
<img src="logo.png" alt="image">
<img src="logo.png"> <!-- Missing alt -->
```

### Form Labels
```html
<!-- Good -->
<label for="name">Name:</label>
<input type="text" id="name" name="name">

<!-- Avoid -->
<input type="text"> <!-- No label -->
```

### Link Text
```html
<!-- Good -->
<a href="/about">Learn more about us</a>

<!-- Avoid -->
<a href="/about">Click here</a>
```

---

## 🎨 CSS (If Used)

### Formatting
```css
/* Use consistent formatting */
selector {
  property: value;
  property: value;
}

/* Not */
selector{property:value;property:value;}
```

### Class Names
- Use kebab-case: `.main-content`, `.primary-button`
- Be descriptive: `.navigation-bar` not `.nav1`
- Semantic: `.alert-warning` not `.red-box`

### Organization
```css
/* Reset/Normalize */
* { margin: 0; padding: 0; }

/* Typography */
body { font-family: sans-serif; }

/* Layout */
.container { max-width: 1200px; }

/* Components */
.button { ... }
.card { ... }
```

---

## JavaScript (If Used)

### Variable Names
```javascript
// Good
const userName = "John";
const isActive = true;
let itemCount = 0;

// Avoid
const user_name = "John";
const is_active = true;
let ItemCount = 0;
```

### Comments
```javascript
// Single line comment
/* Multi-line
   comment here */

// Function documentation
/**
 * Function description
 * @param {type} paramName - Description
 * @return {type} Description
 */
function doSomething(paramName) {
  // Code here
}
```

---

## 📋 General Principles

### Clarity
- Code should be self-documenting
- Use meaningful names
- Avoid cryptic abbreviations

### Consistency
- Follow same style throughout
- Use consistent formatting
- Maintain file structure

### Comments
- Comment complex logic
- Explain **why**, not just **what**
- Keep comments up-to-date

### Performance
- Minimize HTTP requests
- Use semantic HTML
- Lazy load images (when applicable)

### Accessibility
- Use semantic HTML
- Include alt text
- Proper heading hierarchy
- Keyboard navigation support

---

## ✅ Code Review Checklist

Before submitting code:
- [ ] Follows naming conventions
- [ ] Proper indentation (2 spaces)
- [ ] Lines under 80 characters
- [ ] Semantic HTML used
- [ ] Proper heading hierarchy
- [ ] Comments clear and helpful
- [ ] No console errors/warnings
- [ ] UTF-8 encoding
- [ ] Accessible markup
- [ ] Consistent with codebase

---

## 🛠️ Tools for Enforcement

### VS Code Extensions
- Prettier (auto-formatting)
- HTMLHint (HTML validation)
- ESLint (JavaScript validation)
- Stylelint (CSS validation)

### Configuration (If Needed)
```json
// .prettierrc
{
  "htmlWhitespaceSensitivity": "css",
  "tabWidth": 2,
  "useTabs": false,
  "singleQuote": false
}
```

---

## 📚 Examples

### Good Code Example
```html
<!DOCTYPE html>
<!-- Helpful comment in target language -->
<html lang="en">
<head>
  <!-- Character encoding -->
  <meta charset="UTF-8">
  
  <!-- Responsive design -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  
  <!-- Descriptive title -->
  <title>Hello World - English</title>
</head>
<body>
  <!-- Main heading -->
  <h1>Hello World!</h1>
  
  <!-- Introduction paragraph -->
  <p>Welcome to the Hello World application.</p>
</body>
</html>
```

### Code to Avoid
```html
<!DOCTYPE html>
<HTML>
<HEAD>
<TITLE>Title</TITLE>
</HEAD>
<BODY>
<h1>Hello</h1>
<p>Text</p><!-- No comment -->
</BODY>
</HTML>
```

---

## 🔗 Related Documents

- [CONTRIBUTING.md](CONTRIBUTING.md) - Contribution guidelines
- [DEVELOPMENT.md](DEVELOPMENT.md) - Development setup
- [multilingual/HTML-TAG-DOCUMENTATION.md](multilingual/HTML-TAG-DOCUMENTATION.md) - HTML tag reference

---

**Consistency = Quality = Happy Developers** 🎉

[← Back to Documentation](README.md)
