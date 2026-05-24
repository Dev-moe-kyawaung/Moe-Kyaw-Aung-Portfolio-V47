# 🛠 Installation & Setup Guide

## Complete Installation Instructions for All Platforms

---

## 📋 Table of Contents

1. [System Requirements](#system-requirements)
2. [Installation Methods](#installation-methods)
3. [Local Development Setup](#local-development-setup)
4. [Verification Steps](#verification-steps)
5. [Troubleshooting](#troubleshooting)
6. [Next Steps](#next-steps)

---

## 💻 System Requirements

### Minimum Requirements
- **OS**: Windows 7+, macOS 10.12+, Linux (any distribution)
- **Browser**: Chrome 90+, Firefox 88+, Safari 14+, Edge 90+
- **Storage**: 200MB free space
- **Internet**: Required for CDN resources (Tailwind, Font Awesome, Google Fonts)

### Recommended Requirements
- **OS**: Windows 10+, macOS 11+, Linux (Ubuntu 20.04+)
- **Browser**: Chrome 120+, Firefox 120+, Safari 17+, Edge 120+
- **RAM**: 4GB (for running local server)
- **CPU**: Multi-core processor

### Development Tools (Optional)
- **Code Editor**: VS Code, Sublime Text, Atom, WebStorm, etc.
- **Git**: Version 2.25+
- **Node.js**: v14+ (optional, for npm packages)
- **Python**: v3.6+ (optional, for built-in HTTP server)

---

## 🚀 Installation Methods

### Method 1: GitHub Clone (Recommended)

#### Step 1: Install Git
If you don't have Git installed:

**Windows:**
```bash
# Download from https://git-scm.com/download/win
# Or use package manager
choco install git
```

**macOS:**
```bash
# Using Homebrew
brew install git

# Or download from https://git-scm.com/download/mac
```

**Linux (Ubuntu/Debian):**
```bash
sudo apt-get update
sudo apt-get install git
```

**Verify Installation:**
```bash
git --version  # Should show version 2.25+
```

#### Step 2: Clone Repository

```bash
# Clone via HTTPS (recommended for beginners)
git clone https://github.com/moekyawaung-tech/portfolio-v47.git

# Or clone via SSH (if SSH key configured)
git clone git@github.com:moekyawaung-tech/portfolio-v47.git

# Navigate to directory
cd portfolio-v47
```

#### Step 3: Verify Files

```bash
# List files (shows file structure)
ls -la              # macOS/Linux
dir                 # Windows

# Should see: index.html, README.md, LICENSE, etc.
```

---

### Method 2: Direct Download (Easiest)

#### Step 1: Download ZIP
1. Visit [GitHub Repository](https://github.com/moekyawaung-tech/portfolio-v47)
2. Click **"Code"** button (green)
3. Select **"Download ZIP"**
4. Wait for download to complete

#### Step 2: Extract Files

**Windows:**
1. Right-click ZIP file
2. Select "Extract All..."
3. Choose destination folder
4. Click "Extract"

**macOS:**
1. Double-click ZIP file
2. Files auto-extract to same directory
3. Move to desired location

**Linux:**
```bash
unzip portfolio-v47-main.zip
cd portfolio-v47-main
```

#### Step 3: Verify Extraction

Check that these files exist in folder:
- `index.html` (main file)
- `README.md` (documentation)
- `LICENSE` (license file)

---

### Method 3: Using Package Managers

#### Using npm (Node.js)
```bash
# Install create-app tool
npm install -g create-portfolio-app

# Create new portfolio from template
create-portfolio-app my-portfolio

cd my-portfolio
```

#### Using Homebrew (macOS)
```bash
# Tap formula
brew tap moekyawaung/portfolio

# Install
brew install portfolio-v47

# Navigate to installation
cd /usr/local/opt/portfolio-v47
```

---

## 💻 Local Development Setup

### Setup Option 1: Python HTTP Server (Recommended)

**Best for**: Quick preview, simple testing

**Windows:**
```bash
# Open Command Prompt in project folder
# Press Shift + Right-Click > Open PowerShell here

python -m http.server 8000

# Or Python 2 (if installed)
python -m SimpleHTTPServer 8000

# Open browser: http://localhost:8000
```

**macOS/Linux:**
```bash
# Terminal in project directory
cd /path/to/portfolio-v47

python3 -m http.server 8000

# Output: "Serving HTTP on 0.0.0.0 port 8000"

# Open browser: http://localhost:8000
```

### Setup Option 2: Node.js HTTP Server

**Best for**: Developers familiar with Node.js

```bash
# Install globally
npm install -g http-server

# Run in project folder
http-server

# Or with custom port
http-server -p 3000

# Output: Hit CTRL-C to stop the server
# http-server version x.x.x
# http-server started on port 8080
```

### Setup Option 3: Ruby HTTP Server

**Best for**: Ruby developers

```bash
# macOS comes with Ruby pre-installed
ruby -run -ehttpd . -p8000

# Or use WEBrick
ruby -rwebrick -e 'WEBrick::HTTPServer.new(:Port => 8000, :DocumentRoot => ".").start'
```

### Setup Option 4: PHP Server

**Best for**: PHP environments

```bash
# PHP 5.4+ has built-in server
php -S localhost:8000

# Or custom port
php -S 127.0.0.1:3000
```

### Setup Option 5: VS Code Live Server

**Best for**: VS Code users

1. **Install Extension**
   - Open VS Code
   - Go to Extensions (Ctrl+Shift+X)
   - Search "Live Server"
   - Click Install

2. **Start Server**
   - Right-click `index.html`
   - Select "Open with Live Server"
   - Browser opens automatically

3. **Features**
   - Auto-reload on file changes
   - Real-time preview
   - Network address display

---

## ✅ Verification Steps

### Step 1: File Verification

Check all required files exist:

```bash
# In project directory
ls index.html        # Should show file exists

# Or on Windows
dir index.html       # Should show file exists
```

### Step 2: Browser Verification

1. **Open `index.html` in browser**
   - Double-click file, or
   - Use local server (recommended)

2. **Check Page Loads**
   - Preloader should appear briefly
   - Hero section should display
   - No console errors (F12 > Console)

3. **Test Responsiveness**
   - Resize browser window
   - Open DevTools (F12)
   - Click Device Toolbar icon
   - Select mobile device

### Step 3: Feature Testing

**Test Basic Features:**
```javascript
// Open browser console (F12 > Console)

// Test theme toggle
document.body.classList.toggle('light-mode')

// Test particle canvas
document.getElementById('heroCanvas')

// Test form validation
document.getElementById('contactForm')
```

**Test Interactive Elements:**
- Click hamburger menu (mobile)
- Toggle dark/light mode
- Scroll through sections
- Click form fields
- Test carousel navigation
- Expand FAQ items

### Step 4: Network Verification

Check external resources load:

1. **Open DevTools** (F12)
2. **Go to Network tab**
3. **Reload page**
4. Check for:
   - ✅ Tailwind CSS loaded
   - ✅ Font Awesome loaded
   - ✅ Google Fonts loaded
   - ✅ No 404 errors

---

## 🔧 Customization Prerequisites

Before customizing, ensure you have:

1. **Code Editor**
   - Download [VS Code](https://code.visualstudio.com/) (free)
   - Or any text editor

2. **Browser DevTools**
   - Chrome: F12 or Right-click > Inspect
   - Firefox: F12 or Right-click > Inspect Element
   - Safari: Enable in Preferences > Advanced

3. **Version Control** (optional)
   - Git installed and configured
   - GitHub account created

---

## 🐛 Troubleshooting

### Issue 1: File Not Opening
**Problem**: Double-clicking `index.html` doesn't open in browser

**Solutions**:
```bash
# Option 1: Drag file to browser window
# Drag index.html onto browser tab

# Option 2: Use local server (recommended)
python -m http.server 8000
# Then visit: http://localhost:8000

# Option 3: Use context menu
# Right-click index.html > Open With > Select browser
```

### Issue 2: Blank Page Loading
**Problem**: Page loads but appears blank/white

**Solutions**:
1. Check browser console (F12 > Console)
2. Check for JavaScript errors
3. Verify CDN resources loaded (F12 > Network)
4. Refresh page (Ctrl+F5 / Cmd+Shift+R)
5. Clear browser cache

### Issue 3: Styles Not Loading
**Problem**: Page layout looks broken, no colors/spacing

**Solutions**:
```bash
# Clear browser cache
Ctrl+F5 (Windows/Linux)
Cmd+Shift+R (macOS)

# Or use Incognito mode
Ctrl+Shift+N (Chrome)
Cmd+Shift+N (Safari)
```

### Issue 4: Images Not Showing
**Problem**: Images appear as broken link icons

**Solutions**:
1. Check internet connection (CDN images require internet)
2. Verify image URLs in HTML
3. Check browser console for 404 errors
4. Replace image URLs with your own:
   ```html
   <!-- Change this -->
   <img src="https://res.cloudinary.com/...">
   
   <!-- To this -->
   <img src="path/to/your-image.jpg">
   ```

### Issue 5: Mobile Menu Not Working
**Problem**: Hamburger menu doesn't toggle on mobile

**Solutions**:
1. Check viewport meta tag present in `<head>`
2. Test with actual device or DevTools emulation
3. Check JavaScript console for errors
4. Verify click handler attached:
   ```javascript
   document.getElementById('menuToggle').addEventListener('click', ...)
   ```

### Issue 6: Dark Mode Not Persisting
**Problem**: Theme preference resets on refresh

**Solutions**:
```javascript
// Check localStorage availability
typeof(Storage) !== "undefined"

// Clear storage and retry
localStorage.clear()

// Check privacy mode (disables localStorage)
// Use private/incognito window
```

### Issue 7: Forms Not Submitting
**Problem**: Contact form submission has no response

**Solutions**:
1. Open browser console (F12)
2. Look for form submission errors
3. Check email validation:
   ```javascript
   /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test('email@example.com')
   ```
4. Connect to email service (see [DEPLOYMENT.md](./DEPLOYMENT.md))

### Issue 8: Animations Stuttering
**Problem**: Animations appear laggy or jerky

**Solutions**:
1. Check for running processes consuming CPU
2. Close other browser tabs
3. Disable browser extensions
4. Update browser to latest version
5. Test on different browser

### Issue 9: Port Already in Use
**Problem**: Local server won't start - port 8000 in use

**Solutions**:
```bash
# Use different port
python -m http.server 8080   # Instead of 8000

# Or find process using port
# Windows
netstat -ano | findstr :8000

# macOS/Linux
lsof -i :8000

# Kill process
kill -9 <PID>  # macOS/Linux
```

### Issue 10: Mixed Content Warning
**Problem**: Browser shows "Mixed Content" warning in console

**Solutions**:
1. Ensure all external links use HTTPS
2. Use `https://` instead of `http://`
3. Update any image/resource URLs
4. Check cloud image service uses HTTPS

---

## 🔗 Environment Variables

No environment variables needed for basic setup!

For advanced deployment:

```bash
# Create .env file (if using backend services)
CONTACT_FORM_API=https://api.example.com/contact
NEWSLETTER_API=https://api.example.com/newsletter
GA_TRACKING_ID=UA-XXXXXXXXX-X
```

---

## 📦 Dependency Checklist

**Downloaded from CDN (Auto-loaded):**
- ✅ Tailwind CSS 3.x
- ✅ Font Awesome 6.5.1
- ✅ Google Fonts API

**No Manual Installation Required:**
- ✅ No npm packages
- ✅ No build tools
- ✅ No server framework
- ✅ No database setup

---

## 🎯 Post-Installation

### Immediate Next Steps

1. **Verify Installation**
   - Open `index.html` in browser
   - Check all elements display correctly
   - Test responsive design

2. **Basic Customization**
   - Replace name/tagline with yours
   - Update profile image
   - Change contact information

3. **Test Features**
   - Toggle dark/light mode
   - Open mobile menu
   - Test carousel/accordion
   - Submit contact form

### Setup Development Environment

1. **Editor Setup**
   - Install code editor
   - Install useful extensions
   - Configure formatting

2. **Version Control**
   - Initialize git repository
   - Create GitHub account
   - Push code to remote

3. **Local Server**
   - Choose HTTP server method
   - Start development server
   - Configure auto-reload

### Prepare for Customization

See [CUSTOMIZATION.md](./CUSTOMIZATION.md) for:
- Changing colors and fonts
- Adding/editing content sections
- Modifying interactive components
- Deploying to production

---

## 🚀 Quick Start Commands

### One-Liner Setups

**Python Server:**
```bash
cd portfolio-v47 && python -m http.server 8000
```

**Node Server:**
```bash
cd portfolio-v47 && npx http-server
```

**Ruby Server:**
```bash
cd portfolio-v47 && ruby -run -ehttpd . -p8000
```

**PHP Server:**
```bash
cd portfolio-v47 && php -S localhost:8000
```

---

## 📱 Mobile Testing

### Physical Device Testing

1. **Get Local IP**
   ```bash
   # macOS/Linux
   ifconfig | grep "inet "
   
   # Windows
   ipconfig
   ```

2. **Access on Phone**
   - Connect phone to same WiFi
   - Open browser
   - Visit `http://YOUR_IP:8000`

3. **Test Features**
   - Touch menu toggle
   - Scroll through content
   - Test form submission

### DevTools Emulation

1. Open DevTools (F12)
2. Click Device Toolbar icon (Ctrl+Shift+M)
3. Select device from dropdown
4. Test responsive behavior

---

## 🎓 Installation Tips

### Best Practices

1. **Use Version Control**
   - Clone with Git when possible
   - Maintain commit history
   - Easy to revert changes

2. **Use Local Server**
   - Better than file:// protocol
   - Tests real server behavior
   - Enables CORS features

3. **Test Regularly**
   - Test after each change
   - Check multiple browsers
   - Use DevTools console

4. **Backup Original**
   - Keep copy of original files
   - Easy to compare changes
   - Revert if needed

### Performance Optimization During Install

1. **Check Network**
   - Ensure good internet
   - CDN resources load faster
   - Cloudinary images optimize

2. **Browser Optimization**
   - Close unnecessary tabs
   - Disable extensions
   - Clear cache periodically

3. **System Optimization**
   - Close background applications
   - Ensure sufficient RAM
   - Update browser to latest

---

## ✨ Success Indicators

You've successfully installed when you see:

✅ **Page loads** without errors  
✅ **Preloader** animation displays  
✅ **Hero section** shows with particle animation  
✅ **Navigation** works (hamburger on mobile)  
✅ **Theme toggle** switches colors  
✅ **Content sections** display properly  
✅ **Forms** respond to input  
✅ **Images** load from CDN  
✅ **Console** shows no errors (F12)  
✅ **Responsive** layout adjusts on resize  

---

## 🆘 Getting Help

If you encounter issues:

1. **Check [Troubleshooting](#troubleshooting) section** above
2. **Review console errors** (F12 > Console)
3. **Check network tab** (F12 > Network)
4. **Read inline code comments** for hints
5. **Visit [GitHub Issues](https://github.com/moekyawaung-tech/portfolio-v47/issues)**
6. **Email support**: [moekyawaung@programmer.net](mailto:moekyawaung@programmer.net)

---

## 📖 Related Documentation

- **[README.md](./README.md)** - Project overview
- **[FEATURES.md](./FEATURES.md)** - Feature documentation
- **[CUSTOMIZATION.md](./CUSTOMIZATION.md)** - Customization guide
- **[DEPLOYMENT.md](./DEPLOYMENT.md)** - Deployment instructions

---

**Last Updated:** January 2026  
**Version:** 47  
**Status:** ✅ Production Ready  

Need help? Create an issue on [GitHub](https://github.com/moekyawaung-tech/portfolio-v47) or email [moekyawaung@programmer.net](mailto:moekyawaung@programmer.net)
