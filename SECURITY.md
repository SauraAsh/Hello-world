# Security Guidelines

Security best practices and policies for this project.

---

## 🔒 Security Overview

This is a static HTML project with minimal security risks. However, we follow security best practices for all aspects.

---

## 🔐 General Security Principles

### 1. No Sensitive Data
- ❌ Never include passwords in code
- ❌ Never include API keys
- ❌ Never include tokens or credentials
- ❌ Never include personal information
- ✅ Use environment variables (for future backend)

### 2. Code Security
- ✅ Use semantic HTML
- ✅ Validate input (if forms added)
- ✅ Escape output
- ✅ Use HTTPS for external resources
- ✅ Keep dependencies updated

### 3. Comment Security
- ✅ Use comments for documentation
- ❌ Don't include sensitive info in comments
- ❌ Don't include credentials anywhere
- ✅ Remember: Source code is visible to all

---

## 📝 Code Practices

### Secure HTML
```html
<!-- Good: Semantic, secure structure -->
<html lang="en">
<head>
  <meta charset="UTF-8">
</head>
<body>
  <h1>Content</h1>
</body>
</html>

<!-- Avoid: Inline event handlers (when JavaScript is used) -->
<button onclick="doSomething()">Click</button>

<!-- Better: External event listeners -->
<button id="btn">Click</button>
<script>
  document.getElementById('btn').addEventListener('click', doSomething);
</script>
```

### Input Validation (When Forms Are Added)
```html
<!-- Validate on client side -->
<input type="email" required>
<input type="number" min="0" max="100">

<!-- Always validate on server side too -->
```

### XSS Prevention
```html
<!-- Don't use innerHTML with user input -->
<!-- Vulnerable: -->
element.innerHTML = userInput;

<!-- Safe: -->
element.textContent = userInput;
```

---

## 🔗 External Resources

### HTTPS Only
```html
<!-- Good: HTTPS -->
<script src="https://example.com/script.js"></script>
<img src="https://example.com/image.png">

<!-- Avoid: HTTP (unencrypted) -->
<script src="http://example.com/script.js"></script>
```

### Trusted Sources Only
- Only link to reputable, trusted sources
- Verify domains before linking
- Use official CDN links
- Check for HTTPS certificates

### Subresource Integrity (SRI)
```html
<!-- When linking external resources -->
<script 
  src="https://example.com/lib.js"
  integrity="sha384-...">
</script>
```

---

## 🌐 HTTPS & TLS

### Deployment Requirements
- ✅ Always use HTTPS in production
- ✅ Use valid SSL certificates
- ✅ Enforce HTTPS redirects
- ✅ Use HSTS headers
- ✅ Keep certificates updated

### Configuration (If Using Web Server)
```
# Redirect HTTP to HTTPS
http://example.com → https://example.com

# Enable HSTS
Strict-Transport-Security: max-age=31536000
```

---

## 📋 Git Security

### What NOT to Commit
- ❌ Passwords or API keys
- ❌ Private keys or certificates
- ❌ Tokens or credentials
- ❌ Sensitive personal information
- ❌ Config files with secrets

### .gitignore Example
```
# Credentials and keys
.env
.env.local
.env.*.local

# IDE secrets
.vscode/settings.json
.idea/workspace.xml

# OS files
.DS_Store
Thumbs.db
```

### Commit Message Security
```bash
# Good: Descriptive without sensitive info
git commit -m "feat: add user authentication"

# Avoid: Including credentials
git commit -m "feat: add API key abc123xyz"
```

---

## 🚨 Common Security Issues

### 1. Hardcoded Credentials
```javascript
// BAD - Never do this!
const apiKey = "abc123xyz";
const password = "mypassword";

// GOOD - Use environment variables
const apiKey = process.env.API_KEY;
const password = process.env.PASSWORD;
```

### 2. Sensitive Data in Comments
```html
<!-- BAD: Includes sensitive info -->
<!-- User: admin@example.com Password: pass123 -->

<!-- GOOD: No sensitive info in comments -->
<!-- User authentication system -->
```

### 3. Unescaped Output
```javascript
// BAD: Vulnerable to XSS
element.innerHTML = userInput;

// GOOD: Safe from XSS
element.textContent = userInput;

// GOOD: If HTML needed, sanitize first
element.innerHTML = sanitizeHTML(userInput);
```

### 4. Weak Validation
```javascript
// BAD: No validation
function processEmail(email) {
  sendEmail(email);
}

// GOOD: With validation
function processEmail(email) {
  if (isValidEmail(email)) {
    sendEmail(email);
  }
}
```

---

## 🔑 Key Management (For Future Backend)

### Environment Variables
```bash
# .env (local only, never commit)
API_KEY=your_key_here
DATABASE_URL=your_db_url
SECRET_KEY=your_secret
```

### Configuration
```javascript
// Load from environment
const apiKey = process.env.API_KEY;

// Never in source code
// ❌ const apiKey = "abc123";
```

### Rotation
- ✅ Rotate keys regularly
- ✅ Invalidate old keys
- ✅ Use key versioning
- ✅ Document rotation schedule

---

## 🛡️ Headers & Security

### Content Security Policy (CSP)
```html
<!-- Restrict resource loading -->
<meta http-equiv="Content-Security-Policy" 
      content="default-src 'self'; script-src 'self' 'unsafe-inline'">
```

### X-Content-Type-Options
```
X-Content-Type-Options: nosniff
```

### X-Frame-Options
```
X-Frame-Options: SAMEORIGIN
```

---

## 🧪 Security Testing

### Manual Testing
- [ ] No credentials in code
- [ ] No sensitive data in comments
- [ ] HTTPS links for external resources
- [ ] No console errors related to security
- [ ] No mixed content warnings

### Using Browser DevTools
1. Open DevTools (F12)
2. Go to Console tab
3. Look for security warnings
4. Check Network tab for HTTP resources
5. Check Security tab for certificate info

### Security Headers Check
- Use: https://securityheaders.com
- Enter your URL
- Review recommendations

---

## 🔍 Dependency Security

### For Future Npm Packages
```bash
# Check for vulnerabilities
npm audit

# Fix vulnerabilities
npm audit fix

# Update packages safely
npm update

# Check specific package
npm audit [package-name]
```

---

## 📚 Security Checklist

### Before Deployment
- [ ] No hardcoded credentials
- [ ] No sensitive data in comments
- [ ] No HTTP resources
- [ ] HTTPS configured
- [ ] Security headers set
- [ ] Dependencies updated
- [ ] No console warnings
- [ ] Input validated
- [ ] Output escaped
- [ ] .gitignore configured

### Regular Maintenance
- [ ] Weekly: Check for security updates
- [ ] Monthly: Dependency audit
- [ ] Quarterly: Security review
- [ ] Annually: Full security audit

---

## 🐛 Vulnerability Reporting

### Reporting Security Issues
**DO NOT** create public GitHub issues for security vulnerabilities.

Instead:
1. Email security contact (when available)
2. Use responsible disclosure
3. Provide detailed information
4. Allow time for patch
5. Coordinate public disclosure

### Vulnerability Report Template
```
**Severity:** [Critical/High/Medium/Low]

**Type:** [XSS/CSRF/SQL Injection/etc]

**Description:** 
[Detailed description of vulnerability]

**Affected Version:**
[Version numbers]

**Reproduction:**
[Steps to reproduce]

**Impact:**
[Potential impact]

**Fix Suggestion:**
[Suggested fix]
```

---

## 🏆 Security Best Practices

### Development
1. ✅ Keep code simple and clear
2. ✅ Use secure defaults
3. ✅ Validate all input
4. ✅ Escape all output
5. ✅ Use HTTPS everywhere
6. ✅ Keep software updated
7. ✅ Follow least privilege principle
8. ✅ Document security decisions

### Code Review
1. ✅ Review for security issues
2. ✅ Check for credentials
3. ✅ Verify dependencies
4. ✅ Check for XSS vulnerabilities
5. ✅ Validate error handling

### Deployment
1. ✅ Use HTTPS only
2. ✅ Set security headers
3. ✅ Configure WAF (if applicable)
4. ✅ Enable logging
5. ✅ Monitor for anomalies

---

## 📖 Resources

### OWASP
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [OWASP Guidelines](https://owasp.org/)
- [Cheat Sheets](https://cheatsheetseries.owasp.org/)

### Security Guides
- [MDN Security](https://developer.mozilla.org/en-US/docs/Web/Security)
- [NIST Cybersecurity](https://www.nist.gov/cybersecurity)

### Tools
- [OWASP ZAP](https://www.zaproxy.org/) - Security scanner
- [Burp Suite](https://portswigger.net/burp) - Penetration testing
- [npm audit](https://docs.npmjs.com/cli/audit) - Dependency check

---

## 📞 Questions?

- Review [DEVELOPMENT.md](DEVELOPMENT.md)
- Check existing security issues
- Start discussion on GitHub
- Email security contact

---

**Security is everyone's responsibility** 🔐

[← Back to Documentation](README.md)
