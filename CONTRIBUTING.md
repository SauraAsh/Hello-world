# Contributing to Hello World Project

Thank you for your interest in contributing! This document provides guidelines for contributing to this project.

## 🎯 Code of Conduct

Please be respectful and constructive in all interactions. We're building a welcoming community.

## 💡 Ways to Contribute

### 1. **Report Issues**
- Found a bug? Open an issue with:
  - Clear description of the problem
  - Steps to reproduce
  - Expected vs. actual behavior
  - Your environment (browser, OS, etc.)

### 2. **Suggest Improvements**
- Have an idea? Submit a feature request with:
  - Detailed description
  - Use cases
  - Potential implementation approach

### 3. **Improve Documentation**
- Fix typos, unclear sections, or add examples
- Improve existing documentation files
- Add new guides or tutorials

### 4. **Add Multilingual Content**
- Add new language index files
- Translate documentation
- Improve existing translations

### 5. **Code Contributions**
- Bug fixes
- Feature implementations
- Code refactoring
- Performance improvements

## 🔧 Development Setup

1. **Clone the repository**
   ```bash
   git clone git@github.com:SauraAsh/Hello-world.git
   cd hello-world
   ```

2. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

3. **Make your changes**
   - Follow [CODE-STYLE.md](CODE-STYLE.md) guidelines
   - Update documentation as needed
   - Test thoroughly

4. **Commit your changes**
   ```bash
   git commit -m "feat: add your feature description"
   ```

5. **Push to your fork**
   ```bash
   git push origin feature/your-feature-name
   ```

6. **Create a Pull Request**
   - Clear title and description
   - Reference any related issues
   - Link to relevant documentation

## 📋 Commit Message Guidelines

Follow conventional commits format:

```
type(scope): subject

body

footer
```

**Types:**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes
- `refactor`: Code refactoring
- `test`: Test additions/changes
- `chore`: Build, dependencies, etc.

**Examples:**
```
feat(multilingual): add French language support
fix(html): correct meta viewport tag
docs: update accessibility guidelines
```

## 📝 Pull Request Process

1. **Before Creating PR:**
   - Ensure all changes are tested
   - Update documentation
   - Check for conflicts with main branch

2. **PR Description Template:**
   ```
   ## Description
   Brief description of changes
   
   ## Type of Change
   - [ ] Bug fix
   - [ ] New feature
   - [ ] Documentation update
   - [ ] Breaking change
   
   ## Testing Done
   Describe testing performed
   
   ## Checklist
   - [ ] Code follows style guidelines
   - [ ] Documentation is updated
   - [ ] No new warnings generated
   - [ ] Changes tested locally
   ```

3. **Code Review:**
   - Address all review comments
   - Engage in constructive discussion
   - Make requested changes

4. **Merge:**
   - Requires at least one approval
   - CI/CD checks must pass
   - Branch is up to date with main

## 🎨 Adding Multilingual Content

When adding a new language:

1. **Create language index file:**
   ```
   multilingual/index-[language-code].html
   ```

2. **Follow HTML structure:**
   - Use proper lang attribute
   - Add comments in target language
   - Include meta tags
   - Use UTF-8 encoding

3. **Update README:**
   - Add language to language table
   - Update statistics

4. **Test:**
   - Verify encoding displays correctly
   - Test in multiple browsers
   - Check RTL languages (if applicable)

## 📚 Documentation Standards

- Use clear, concise language
- Include examples where helpful
- Use consistent formatting
- Keep line length reasonable (80 characters)
- Update existing docs when changing code

## ✅ Quality Checklist

Before submitting:
- [ ] Code follows style guide
- [ ] Comments added for complex logic
- [ ] Documentation updated
- [ ] No console errors/warnings
- [ ] Changes tested locally
- [ ] Commit messages follow guidelines
- [ ] No merge conflicts
- [ ] Files use consistent encoding (UTF-8)

## 🐛 Bug Report Template

**Title:** Short description of bug

**Environment:**
- Browser: 
- OS: 
- Project Version: 

**Steps to Reproduce:**
1. 
2. 
3. 

**Expected Behavior:**

**Actual Behavior:**

**Screenshots:** (if applicable)

**Additional Context:**

## 💬 Questions or Need Help?

- Check [FAQ.md](FAQ.md) for common questions
- Review [TROUBLESHOOTING.md](TROUBLESHOOTING.md)
- Look at existing issues/PRs
- Comment on relevant issues to discuss

## 📄 License

By contributing, you agree that your contributions will be licensed under the project's license.

## 🏆 Recognition

Contributors are recognized in:
- CONTRIBUTORS.md (if created)
- Changelog for significant contributions
- GitHub repository credits

## 🚀 Getting Your PR Merged

1. Follow all guidelines above
2. Be responsive to feedback
3. Keep changes focused and small
4. Update documentation
5. Write clear commit messages
6. Pass all checks

---

**Thank you for contributing!** 🎉

For detailed questions about the project, refer to:
- [DEVELOPMENT.md](DEVELOPMENT.md) - Development setup
- [CODE-STYLE.md](CODE-STYLE.md) - Code standards
- [README.md](README.md) - Project overview
