# Troubleshooting Guide

Solutions for common problems.

---

## 🔧 General Troubleshooting

### Browser Issues

#### Page Won't Load
**Symptoms:** Blank page or "Cannot find file" error

**Solutions:**
1. Check file path is correct
2. Verify file name spelling (case-sensitive on Linux/Mac)
3. Ensure file isn't corrupted
4. Try different browser
5. Clear browser cache: `Ctrl+Shift+Delete`
6. Hard refresh: `Ctrl+Shift+R` (Windows/Linux) or `Cmd+Shift+R` (Mac)

#### Page Loads But Looks Wrong
**Symptoms:** Layout broken, text misaligned, styling incorrect

**Solutions:**
1. **Hard refresh** browser cache
2. Check browser developer tools (F12):
   - Console tab for errors
   - Network tab for failed resources
   - Elements tab for HTML structure
3. Try different browser
4. Check file encoding (should be UTF-8)
5. Verify HTML syntax

#### Characters Display Incorrectly
**Symptoms:** Gibberish text, wrong characters, broken accents

**Solutions:**
1. **Check meta charset tag:**
   ```html
   <meta charset="UTF-8">
   ```
   Must be first meta tag in `<head>`

2. **Verify file encoding:**
   - VS Code: Bottom right corner shows encoding
   - Should show "UTF-8"
   - If not, right-click → "Reopen with Encoding" → UTF-8

3. **Save file as UTF-8:**
   - VS Code: Click encoding → Select UTF-8
   - Save file
   - Refresh browser

4. **Check language attribute:**
   ```html
   <html lang="en">
   ```

---

## 📱 Mobile & Responsive Issues

### Not Responsive on Mobile
**Symptoms:** Page doesn't scale, requires horizontal scrolling

**Solutions:**
1. **Check viewport meta tag:**
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

2. **Test in DevTools:**
   - Open DevTools (F12)
   - Click "Toggle device toolbar" (Ctrl+Shift+M)
   - Select mobile device
   - Check scaling

3. **Hard refresh** browser

4. **Test on actual device** to verify

### Touch Not Working
**Symptoms:** Can't tap elements on mobile

**Solutions:**
1. Check element is interactive (link, button, etc.)
2. Verify proper HTML semantics
3. Check if JavaScript is blocking interactions
4. Test in different browser
5. Try on different device

---

## 🎨 Display Issues

### Colors Look Wrong
**Symptoms:** Colors appear differently than expected

**Solutions:**
1. **Check color values:**
   ```html
   <style>
     body { color: #000000; }
     /* Verify hex codes are correct */
   </style>
   ```

2. **Browser color settings:**
   - Check if browser has night mode enabled
   - Disable browser extensions that modify colors
   - Try incognito/private mode

3. **Monitor calibration:**
   - Colors vary by monitor
   - This is normal

4. **Color blindness simulator:**
   - Test with [Color Blind Simulator](https://www.color-blindness.com/coblis-color-blindness-simulator/)
   - Ensure sufficient contrast

### Text Too Small or Too Large
**Symptoms:** Text unreadable or too large

**Solutions:**
1. **Zoom settings:**
   - Reset zoom: `Ctrl+0` (Windows/Linux) or `Cmd+0` (Mac)
   - Browser → Settings → Text size

2. **Check font size in code:**
   ```html
   <style>
     body { font-size: 16px; }
   </style>
   ```

3. **Test zoom to 200%:** `Ctrl++` multiple times
   - Page should remain readable

---

## 🔊 Console Errors

### No Errors but Page Broken
**Solutions:**
1. Open DevTools (F12)
2. Go to Console tab
3. Refresh page (F5)
4. Look for error messages
5. Google error message
6. Check [multilingual/HTML-TAG-DOCUMENTATION.md](multilingual/HTML-TAG-DOCUMENTATION.md)

### Common Console Errors

#### Uncaught SyntaxError
**Meaning:** Error in JavaScript syntax
**Fix:** 
- Check JavaScript for typos
- Use JSHint or JSLint to validate

#### Failed to fetch resource
**Meaning:** External file (CSS, JS, image) not found
**Fix:**
- Verify file path is correct
- Check file exists
- Use absolute paths if needed

#### Mixed Content Warning
**Meaning:** HTTPS page loading HTTP resource
**Fix:**
- Change HTTP links to HTTPS
- Use protocol-relative URLs: `//example.com`

---

## ♿ Accessibility Issues

### Screen Reader Not Reading Content
**Symptoms:** Content not announced by screen reader

**Solutions:**
1. **Check semantic HTML:**
   ```html
   <!-- Good -->
   <h1>Main Title</h1>
   <p>Content</p>
   
   <!-- Avoid -->
   <div class="title">Main Title</div>
   ```

2. **Add alt text to images:**
   ```html
   <img src="image.jpg" alt="Descriptive text">
   ```

3. **Associate form labels:**
   ```html
   <label for="input-id">Label:</label>
   <input type="text" id="input-id">
   ```

4. **Test with actual screen reader:**
   - NVDA (Windows)
   - VoiceOver (Mac/iOS)
   - TalkBack (Android)

### Can't Navigate with Keyboard
**Symptoms:** Tab doesn't navigate, can't interact

**Solutions:**
1. **Check tab order:**
   - Use Tab key to navigate
   - Order should be logical
   - Left to right, top to bottom

2. **Verify interactive elements:**
   ```html
   <a href="#">Link</a>
   <button>Button</button>
   <input type="text">
   ```

3. **Ensure focus visible:**
   ```css
   element:focus {
     outline: 2px solid blue;
   }
   ```

4. **Check for skip links:**
   - Should be able to skip to main content

---

## 🌐 Multilingual Issues

### Wrong Language Displayed
**Symptoms:** Opening wrong language file, language not selected

**Solutions:**
1. **Verify file path:**
   - Check correct `index-[lang].html` file
   - Verify language code: `en`, `es`, `fr`, etc.

2. **Check lang attribute:**
   ```html
   <html lang="en">
   ```

3. **Clear browser cache** if switching languages

### Special Characters Broken in Multilingual Files
**Symptoms:** Gibberish characters, broken accents

**Solutions:**
1. **Verify file encoding is UTF-8:**
   - Check meta charset: `<meta charset="UTF-8">`
   - Check file encoding settings

2. **Check language attribute:**
   ```html
   <html lang="ko">  <!-- For Korean -->
   ```

3. **Use proper HTML entities:**
   ```html
   &nbsp; (non-breaking space)
   &copy; (copyright)
   &euro; (euro symbol)
   ```

---

## 🔍 Git Issues

### Changes Not Appearing After Commit
**Solutions:**
1. **Verify changes were committed:**
   ```bash
   git log --oneline
   ```

2. **Check current branch:**
   ```bash
   git branch
   ```

3. **Pull latest changes:**
   ```bash
   git pull origin main
   ```

4. **Hard reset if needed:**
   ```bash
   git fetch origin
   git reset --hard origin/main
   ```

### Merge Conflicts
**Symptoms:** Git says files have conflicts

**Solutions:**
1. **See conflicted files:**
   ```bash
   git status
   ```

2. **Open conflicted file:**
   - Look for conflict markers: `<<<<<<<`, `=======`, `>>>>>>>`
   - Choose which version to keep
   - Remove conflict markers

3. **Complete merge:**
   ```bash
   git add .
   git commit -m "fix: resolve merge conflicts"
   ```

### Can't Push Changes
**Symptoms:** "Permission denied" or "authentication failed"

**Solutions:**
1. **Check SSH keys:**
   ```bash
   ssh -T git@github.com
   ```

2. **Add SSH key if missing:**
   - Generate: `ssh-keygen -t ed25519`
   - Add to GitHub account

3. **Pull before push:**
   ```bash
   git pull origin main
   git push origin feature-branch
   ```

---

## ⚡ Performance Issues

### Page Loads Slowly
**Solutions:**
1. **Check network tab:**
   - Open DevTools (F12)
   - Go to Network tab
   - Refresh page
   - Look for slow resources

2. **Minimize HTTP requests:**
   - Combine files if possible
   - Remove unused resources

3. **Optimize images:**
   - Compress image files
   - Use appropriate formats
   - Use correct dimensions

4. **Check server:**
   - Try different server/connection
   - Check if server is down

### Live Server Won't Start
**Symptoms:** "Port already in use" error

**Solutions:**
1. **Use different port:**
   ```bash
   python -m http.server 8001
   ```

2. **Kill process using port:**
   ```bash
   # Windows
   netstat -ano | findstr :8000
   taskkill /PID <PID> /F
   
   # Mac/Linux
   lsof -i :8000
   kill -9 <PID>
   ```

3. **Wait a minute** and try again (port might still be closing)

---

## 💾 File Issues

### Can't Save File
**Symptoms:** File won't save, permission denied error

**Solutions:**
1. **Check file permissions:**
   - Right-click file → Properties
   - Ensure "Read-only" is unchecked
   - Click Apply

2. **Close file elsewhere:**
   - File might be open in another application
   - Close and retry

3. **Run as administrator:**
   - Right-click editor → Run as administrator
   - Save file again

### Wrong Line Endings
**Symptoms:** File display problems, Git shows all lines changed

**Solutions:**
1. **Set line endings:**
   - VS Code: Click "CRLF" or "LF" in bottom right
   - Convert all to LF (recommended for web projects)

2. **Configure Git:**
   ```bash
   git config --global core.autocrlf true
   ```

---

## 🆘 Still Having Issues?

### Debugging Steps
1. **Restart everything:**
   - Close browser completely
   - Close editor
   - Reopen both
   - Try again

2. **Hard refresh:**
   - `Ctrl+Shift+R` (Windows/Linux)
   - `Cmd+Shift+R` (Mac)

3. **Check documentation:**
   - [FAQ.md](FAQ.md)
   - [DEVELOPMENT.md](DEVELOPMENT.md)
   - [multilingual/HTML-TAG-DOCUMENTATION.md](multilingual/HTML-TAG-DOCUMENTATION.md)

4. **Google the error:**
   - Copy exact error message
   - Search on Google
   - Check Stack Overflow

5. **Create GitHub issue:**
   - Include error message
   - Include browser/OS info
   - Include steps to reproduce
   - Include screenshot if possible

### Issue Report Template
```
**Browser/OS:** [Chrome on Windows 10]
**Error Message:** [Copy exact error]
**Steps to Reproduce:**
1. 
2. 
3. 

**Expected Behavior:**
**Actual Behavior:**
**Screenshot:**
```

---

## 📞 Getting Help

- Check [FAQ.md](FAQ.md) for common questions
- Search GitHub Issues
- Create new GitHub Issue
- Start GitHub Discussion
- Check Stack Overflow

---

**Most issues can be solved by:**
1. Hard refresh browser (Ctrl+Shift+R)
2. Clear browser cache (Ctrl+Shift+Delete)
3. Checking UTF-8 encoding
4. Reading the error message carefully

---

**Still stuck?** Create a detailed GitHub issue! 🆘

[← Back to Documentation](README.md)
