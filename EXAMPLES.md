# Code Examples

Practical code examples and use cases for this project.

---

## 📚 Overview

This document provides real-world examples for working with the Hello World Project.

---

## 🌐 Basic HTML Examples

### Simple Hello World
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hello World</title>
</head>
<body>
  <h1>Hello World</h1>
</body>
</html>
```

### With Comments
```html
<!DOCTYPE html>
<!-- This is a comment explaining the document -->
<html lang="en">
<head>
  <!-- Metadata section -->
  <meta charset="UTF-8">
  <title>Example</title>
</head>
<body>
  <!-- Main content -->
  <h1>Hello World</h1>
</body>
</html>
```

### With Structure
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Structured Page</title>
</head>
<body>
  <!-- Header -->
  <header>
    <h1>My Website</h1>
  </header>
  
  <!-- Main content -->
  <main>
    <section>
      <h2>Welcome</h2>
      <p>Hello World!</p>
    </section>
  </main>
  
  <!-- Footer -->
  <footer>
    <p>&copy; 2026 My Website</p>
  </footer>
</body>
</html>
```

---

## 🌍 Multilingual Examples

### English Version
```html
<!DOCTYPE html>
<!-- English Comments -->
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Hello World - English</title>
</head>
<body>
  <h1>Hello World!</h1>
</body>
</html>
```

### Spanish Version
```html
<!DOCTYPE html>
<!-- Comentarios en Español -->
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Hola Mundo - Español</title>
</head>
<body>
  <h1>¡Hola Mundo!</h1>
</body>
</html>
```

### With Multiple Languages
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Multilingual Example</title>
</head>
<body>
  <h1>Hello World</h1>
  
  <!-- English -->
  <p lang="en">This is English text.</p>
  
  <!-- Spanish -->
  <p lang="es">Este es texto en español.</p>
  
  <!-- French -->
  <p lang="fr">Ceci est du texte en français.</p>
</body>
</html>
```

---

## 🎨 HTML Structure Examples

### Semantic HTML
```html
<!-- Good: Semantic HTML -->
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Page Title</title>
</head>
<body>
  <header>
    <h1>Main Title</h1>
  </header>
  
  <nav>
    <ul>
      <li><a href="/">Home</a></li>
      <li><a href="/about">About</a></li>
    </ul>
  </nav>
  
  <main>
    <article>
      <h2>Article Title</h2>
      <p>Article content...</p>
    </article>
  </main>
  
  <footer>
    <p>&copy; 2026</p>
  </footer>
</body>
</html>
```

### Heading Hierarchy
```html
<!-- Correct hierarchy -->
<h1>Main Page Title</h1>

<h2>Section 1</h2>
<p>Section 1 content...</p>

<h3>Subsection 1.1</h3>
<p>Subsection content...</p>

<h2>Section 2</h2>
<p>Section 2 content...</p>
```

### Paragraph Grouping
```html
<section>
  <h2>Introduction</h2>
  
  <p>First paragraph of introduction.</p>
  <p>Second paragraph of introduction.</p>
  <p>Third paragraph of introduction.</p>
</section>

<section>
  <h2>Main Content</h2>
  
  <p>Main content goes here.</p>
</section>
```

---

## 🔗 Link Examples

### Simple Links
```html
<!-- Internal link -->
<a href="/page.html">Link to page</a>

<!-- External link -->
<a href="https://example.com">Visit Example</a>

<!-- Email link -->
<a href="mailto:info@example.com">Email us</a>

<!-- Phone link -->
<a href="tel:+1-555-123-4567">Call us</a>

<!-- Link with title -->
<a href="/page.html" title="Go to page">Click here</a>
```

### Descriptive Link Text
```html
<!-- Good: Descriptive -->
<a href="/about">Learn more about our team</a>

<!-- Avoid: Generic -->
<a href="/about">Click here</a>

<!-- Good: With context -->
<p>Read more about our <a href="/services">services</a>.</p>
```

---

## 🖼️ Image Examples

### Basic Image
```html
<!-- With alt text (required for accessibility) -->
<img src="image.jpg" alt="Image description">

<!-- With dimensions -->
<img src="image.jpg" alt="Description" width="400" height="300">

<!-- With link -->
<a href="/larger-image.jpg">
  <img src="thumbnail.jpg" alt="Thumbnail description">
</a>
```

### Responsive Images
```html
<!-- Multiple formats -->
<picture>
  <source srcset="image.webp" type="image/webp">
  <source srcset="image.jpg" type="image/jpeg">
  <img src="image.jpg" alt="Description">
</picture>

<!-- Responsive sizing -->
<img 
  srcset="small.jpg 400w, medium.jpg 800w, large.jpg 1200w"
  src="medium.jpg" 
  alt="Description"
  sizes="(max-width: 600px) 100vw, 50vw">
```

---

## 📋 Form Examples

### Basic Form
```html
<form action="/submit" method="POST">
  <!-- Text input -->
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required>
  
  <!-- Email input -->
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required>
  
  <!-- Submit button -->
  <button type="submit">Submit</button>
</form>
```

### Form with Validation
```html
<form action="/submit" method="POST">
  <!-- Required field -->
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required>
  
  <!-- Email validation -->
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required>
  
  <!-- Number range -->
  <label for="age">Age:</label>
  <input type="number" id="age" name="age" min="0" max="120">
  
  <!-- Submit -->
  <button type="submit">Submit</button>
</form>
```

---

## 🎯 Accessibility Examples

### Proper Heading Structure
```html
<!-- Good -->
<h1>Page Title</h1>
<section>
  <h2>Section</h2>
  <h3>Subsection</h3>
</section>

<!-- Avoid -->
<h1>Page Title</h1>
<h3>Subsection</h3> <!-- Skipped h2 -->
```

### Image Alt Text
```html
<!-- Good -->
<img src="logo.png" alt="Company logo">
<img src="chart.png" alt="Monthly sales chart showing 50% increase">

<!-- Avoid -->
<img src="logo.png"> <!-- No alt text -->
<img src="logo.png" alt="image"> <!-- Generic -->
```

### Form Accessibility
```html
<!-- Good: Labels associated -->
<label for="username">Username:</label>
<input type="text" id="username" name="username">

<!-- Good: With description -->
<label for="password">Password:</label>
<input type="password" id="password" name="password">
<small>Minimum 8 characters</small>

<!-- Avoid: No label -->
<input type="text" name="username">
```

### Skip Links
```html
<body>
  <!-- Skip to main content -->
  <a href="#main" class="skip-link">Skip to main content</a>
  
  <!-- Navigation -->
  <nav>...</nav>
  
  <!-- Main content -->
  <main id="main">...</main>
</body>
```

---

## 💬 Comment Examples

### Documentation Comments
```html
<!DOCTYPE html>
<!-- 
  Application: Hello World
  Purpose: Demonstrate HTML structure
  Author: SauraAsh
  Version: 1.0.0
  Last Updated: 2026-08-21
-->
<html lang="en">
```

### Section Comments
```html
<!-- ============== Navigation Section ============== -->
<nav>...</nav>

<!-- ============== Main Content ============== -->
<main>...</main>

<!-- ============== Footer ============== -->
<footer>...</footer>
```

### Inline Comments
```html
<h1>Title</h1> <!-- Main page heading -->

<!-- This section requires user authentication -->
<section id="protected">...</section>

<!-- TODO: Add error handling for this form -->
<form>...</form>
```

---

## 🌍 UTF-8 & International Text

### UTF-8 Meta Tag
```html
<meta charset="UTF-8">
```

### International Characters
```html
<!-- Accented characters -->
<p>Café, naïve, résumé</p>

<!-- Symbols -->
<p>&copy; 2026 &bull; &euro; 100 &hearts;</p>

<!-- Emoji (if supported) -->
<p>Hello 👋 World 🌍</p>

<!-- Mathematical symbols -->
<p>&pi; &times; &divide; &infin;</p>
```

### Language Declarations
```html
<html lang="en">
  <p>English text</p>
  <p lang="es">Texto en español</p>
  <p lang="fr">Texte en français</p>
</html>
```

---

## 🔍 SEO Examples

### Meta Tags
```html
<head>
  <!-- Essential -->
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Page Title - Keywords Here</title>
  
  <!-- Descriptive -->
  <meta name="description" content="Page description for search results">
  <meta name="keywords" content="keyword1, keyword2, keyword3">
  
  <!-- Author -->
  <meta name="author" content="Author Name">
</head>
```

### Proper Heading Use
```html
<!-- One h1 per page -->
<h1>Main Page Topic</h1>

<!-- Hierarchical structure -->
<h2>Section 1</h2>
<p>Content...</p>

<h2>Section 2</h2>
<h3>Subsection 2.1</h3>
<p>Content...</p>
```

### Semantic HTML
```html
<!-- Good for SEO -->
<article>
  <h1>Article Title</h1>
  <p>Article content...</p>
</article>

<!-- Better than -->
<div class="article">
  <div class="title">Article Title</div>
  <p>Article content...</p>
</div>
```

---

## 🚀 Quick Start Templates

### Minimal Template
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Page Title</title>
</head>
<body>
  <h1>Hello World</h1>
</body>
</html>
```

### Standard Template
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Page description">
  <title>Page Title</title>
</head>
<body>
  <header>
    <h1>Site Title</h1>
  </header>
  
  <main>
    <h1>Page Title</h1>
    <p>Main content...</p>
  </main>
  
  <footer>
    <p>&copy; 2026</p>
  </footer>
</body>
</html>
```

### Comprehensive Template
```html
<!DOCTYPE html>
<!-- 
  Full-featured template with all best practices
  Language: English
  Version: 1.0
-->
<html lang="en">
<head>
  <!-- Character encoding (MUST be first) -->
  <meta charset="UTF-8">
  
  <!-- Mobile responsiveness -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  
  <!-- SEO -->
  <meta name="description" content="Page description">
  <meta name="keywords" content="key, words, here">
  <meta name="author" content="Author Name">
  
  <!-- Page title -->
  <title>Page Title - Keywords</title>
  
  <!-- Styles (if any) -->
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <!-- Header -->
  <header>
    <h1>Site Title</h1>
    <nav>
      <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/about">About</a></li>
      </ul>
    </nav>
  </header>
  
  <!-- Main content -->
  <main>
    <h1>Page Title</h1>
    <p>Main content...</p>
  </main>
  
  <!-- Footer -->
  <footer>
    <p>&copy; 2026 Company Name. All rights reserved.</p>
  </footer>
  
  <!-- Scripts (if any) -->
  <script src="script.js"></script>
</body>
</html>
```

---

## 📖 Additional Resources

- [MDN Web Docs - HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [W3Schools - HTML](https://www.w3schools.com/html/)
- [HTML Living Standard](https://html.spec.whatwg.org/)
- [WCAG Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)

---

**Use these examples as starting points for your projects!** 🚀

[← Back to Documentation](README.md)
