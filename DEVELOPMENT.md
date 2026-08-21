# Development Guide

Complete guide for developing and contributing to this project.

---

## 🛠 Prerequisites

- Text editor or IDE (VS Code recommended)
- Web browser (Chrome, Firefox, Safari, or Edge)
- Git (for version control)
- Basic HTML knowledge

**No additional software or dependencies required!**

---

## 📁 Project Structure

```
hello-world/
├── index.html                              # Main application
├── README.md                               # Project overview
├── QUICK-START.md                          # Quick setup guide
├── CONTRIBUTING.md                         # Contribution guidelines
├── DEVELOPMENT.md                          # This file
├── CODE-STYLE.md                           # Coding standards
├── ACCESSIBILITY.md                        # Accessibility info
├── SECURITY.md                             # Security guidelines
├── TESTING.md                              # Testing guide
├── FAQ.md                                  # Frequently asked questions
├── TROUBLESHOOTING.md                      # Troubleshooting
├── PERFORMANCE.md                          # Performance tips
├── DEPLOYMENT.md                           # Deployment guide
├── VERSION-GUIDE.md                        # Version info
├── EXAMPLES.md                             # Code examples
├── LICENSE.md                              # MIT License
├── .agents                                 # AI skills config
├── codebase.md                             # Architecture
├── design.md                               # Design principles
├── agents.md                               # Automation docs
├── changelog.md                            # Version history
├── multilingual/                           # Multilingual versions
│   ├── index-en.html                       # English
│   ├── index-id.html                       # Indonesian
│   ├── index-ko.html                       # Korean
│   ├── index-ja.html                       # Japanese
│   ├── index-zh.html                       # Chinese
│   ├── index-es.html                       # Spanish
│   ├── index-fr.html                       # French
│   ├── index-de.html                       # German
│   ├── index-it.html                       # Italian
│   ├── index-ru.html                       # Russian
│   ├── index-vi.html                       # Vietnamese
│   ├── index-lo.html                       # Lao
│   ├── README.md                           # Multilingual guide
│   └── HTML-TAG-DOCUMENTATION.md           # HTML tag reference
└── .gitignore                              # Git configuration
```

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone git@github.com:SauraAsh/Hello-world.git
cd hello-world
```

### 2. Create Feature Branch
```bash
git checkout -b feature/your-feature-name
```

### 3. Open in Editor
```bash
# VS Code
code .

# Or open folder in your preferred editor
```

### 4. Start Development
- Edit files in your editor
- Refresh browser to see changes
- No build process needed!

---

## 💻 Local Development Server

### Option 1: Python
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
```
Visit: `http://localhost:8000`

### Option 2: Node.js
```bash
# Install (one-time)
npm install -g http-server

# Run
http-server
```
Visit: `http://localhost:8080`

### Option 3: VS Code Live Server
1. Install "Live Server" extension
2. Right-click on HTML file
3. Select "Open with Live Server"
4. Browser opens automatically with auto-refresh

### Option 4: Ruby
```bash
ruby -run -ehttpd . -p8000
```
Visit: `http://localhost:8000`

---

## 📝 Code Organization

### File Naming
- Use lowercase with hyphens: `index-en.html`, `HTML-TAG-DOCUMENTATION.md`
- Keep names descriptive and concise
- Use language codes: `en`, `id`, `ko`, `ja`, `zh`, `es`, `fr`, `de`, `it`, `ru`, `vi`, `lo`

### Directory Structure
- Group related files together
- Keep root level organized
- Use subdirectories for content types (e.g., `multilingual/`)

### HTML Structure
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Meta tags first -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page Title</title>
</head>
<body>
    <!-- Content here -->
</body>
</html>
```

---

## 🔄 Git Workflow

### Basic Workflow
```bash
# 1. Create feature branch
git checkout -b feature/awesome-feature

# 2. Make changes
# ... edit files ...

# 3. Check status
git status

# 4. Stage changes
git add .

# 5. Commit with descriptive message
git commit -m "feat: add awesome feature"

# 6. Push to GitHub
git push origin feature/awesome-feature

# 7. Create Pull Request on GitHub
# Wait for review and merge
```

### Commit Message Format
```
type(scope): subject

body (optional)

footer (optional)
```

**Types:** `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`

**Example:**
```
feat(multilingual): add Portuguese translation

- Added index-pt.html
- Updated multilingual README
- Added language code to table

Closes #123
```

---

## 📚 Common Development Tasks

### Adding a New Language
1. Create `multilingual/index-[lang-code].html`
2. Copy structure from existing file
3. Translate comments to new language
4. Update `multilingual/README.md`
5. Commit with message: `feat(i18n): add [language] translation`

### Updating Documentation
1. Edit relevant `.md` file
2. Keep formatting consistent
3. Update table of contents if needed
4. Commit with message: `docs: update [document-name]`

### Fixing Bugs
1. Create issue if not exists
2. Branch: `git checkout -b fix/bug-description`
3. Fix the issue
4. Commit: `git commit -m "fix: resolve bug description"`
5. Push and create PR

### Adding Features
1. Plan in issue/discussion
2. Branch: `git checkout -b feature/feature-name`
3. Implement feature
4. Test thoroughly
5. Update documentation
6. Commit and push
7. Create PR with description

---

## 🧪 Testing

### Manual Testing
1. Open in different browsers
2. Test on mobile devices
3. Test keyboard navigation
4. Test with screen readers
5. View page source (Ctrl+U)
6. Inspect elements (F12)

### Browser Testing
- Chrome/Chromium
- Firefox
- Safari
- Edge
- Mobile browsers

### Accessibility Testing
- Use NVDA (Windows)
- Use JAWS (Windows)
- Use VoiceOver (Mac/iOS)
- Use Axe DevTools browser extension
- Check contrast with WebAIM

See [TESTING.md](TESTING.md) for detailed testing procedures.

---

## 🎨 Code Style

Follow the guidelines in [CODE-STYLE.md](CODE-STYLE.md):

- Use UTF-8 encoding
- Consistent indentation (2 spaces)
- Semantic HTML
- Proper heading hierarchy
- Meaningful comments
- Accessibility best practices

---

## 🔐 Security

- No sensitive data in comments
- No hardcoded credentials
- Use HTTPS for external resources
- Validate user input (when applicable)
- Follow [SECURITY.md](SECURITY.md)

---

## 📊 Performance

- Minimize HTTP requests (static files)
- Optimize images (when used)
- Use semantic HTML
- Cache-friendly setup
- Mobile-first design

See [PERFORMANCE.md](PERFORMANCE.md) for optimization tips.

---

## 🚢 Before Committing

Checklist:
- [ ] Code follows style guide
- [ ] Comments are clear and helpful
- [ ] No console errors or warnings
- [ ] Documentation updated
- [ ] Tested in multiple browsers
- [ ] Accessibility verified
- [ ] No merge conflicts
- [ ] UTF-8 encoding used
- [ ] Commit message is descriptive

---

## 📖 Useful Resources

### Documentation
- [README.md](README.md) - Project overview
- [CODE-STYLE.md](CODE-STYLE.md) - Style guidelines
- [CONTRIBUTING.md](CONTRIBUTING.md) - Contributing guide
- [multilingual/HTML-TAG-DOCUMENTATION.md](multilingual/HTML-TAG-DOCUMENTATION.md) - Tag reference

### External References
- [MDN Web Docs](https://developer.mozilla.org/)
- [W3C HTML Standard](https://html.spec.whatwg.org/)
- [Git Documentation](https://git-scm.com/doc)
- [GitHub Help](https://help.github.com/)

---

## 🆘 Troubleshooting

### Changes Not Appearing
- Browser cache: `Ctrl+Shift+Delete` or hard refresh `Ctrl+Shift+R`
- Live server: Check if running
- File not saved: Verify in editor

### Git Issues
- Merge conflicts: See TROUBLESHOOTING.md
- Push rejected: Pull latest changes first
- Wrong branch: Check with `git branch`

### Encoding Issues
- Always use UTF-8
- Check file encoding in editor
- Verify meta charset tag

See [TROUBLESHOOTING.md](TROUBLESHOOTING.md) for more issues.

---

## 🎓 Learning Path

1. **Start Here:**
   - Read [QUICK-START.md](QUICK-START.md)
   - Open index.html
   - View source code

2. **Learn HTML:**
   - Read [HTML-TAG-DOCUMENTATION.md](multilingual/HTML-TAG-DOCUMENTATION.md)
   - Study semantic markup
   - Review examples

3. **Explore Structure:**
   - Read [codebase.md](codebase.md)
   - Understand project layout
   - Review design principles

4. **Contribute:**
   - Read [CONTRIBUTING.md](CONTRIBUTING.md)
   - Make small improvements
   - Submit pull requests

5. **Master It:**
   - Review all documentation
   - Explore multilingual versions
   - Become a maintainer

---

## 💡 Tips & Tricks

### VS Code Extensions (Recommended)
- Live Server
- HTML Preview
- Prettier - Code Formatter
- HTMLHint
- Better Comments

### Keyboard Shortcuts
- View source: `Ctrl+U` (Windows/Linux) or `Cmd+Option+U` (Mac)
- Inspect element: `F12` or `Ctrl+Shift+I`
- Format document: `Shift+Alt+F` (VS Code)
- Quick fix: `Ctrl+.` (VS Code)

### Git Aliases
```bash
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.st status
```

---

## 📞 Getting Help

1. Check [FAQ.md](FAQ.md)
2. Search existing GitHub issues
3. Check [TROUBLESHOOTING.md](TROUBLESHOOTING.md)
4. Create new GitHub issue with [help needed] tag
5. Start discussion on GitHub Discussions

---

**Happy developing!** 🚀

[← Back to README](README.md)
