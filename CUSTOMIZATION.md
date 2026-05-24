# 🎨 Customization Guide

## Complete Guide to Personalizing Your Portfolio

---

## 📋 Table of Contents

1. [Quick Color Changes](#quick-color-changes)
2. [Personalizing Content](#personalizing-content)
3. [Changing Fonts & Typography](#changing-fonts--typography)
4. [Customizing Images](#customizing-images)
5. [Modifying Components](#modifying-components)
6. [Advanced Customization](#advanced-customization)
7. [CSS Variables Reference](#css-variables-reference)
8. [Common Customizations](#common-customizations)

---

## 🎨 Quick Color Changes

### Method 1: CSS Variables (Easiest)

Edit the `:root` CSS variables in the `<style>` section:

```css
:root {
    /* Primary accent color - used for buttons, headings, links */
    --color-primary: #e8590c;        /* Change Orange */
    
    /* Dark background */
    --color-dark: #1a1a1a;           /* Change Dark Background */
    
    /* Light accent color (for light mode) */
    --color-warm: #FFF7ED;           /* Change Light Accent */
    
    /* Text colors */
    --color-text-dark: #333333;      /* Dark mode text */
    --color-text-light: #f5f5f5;     /* Light mode text */
    
    /* Borders and dividers */
    --color-border: #404040;         /* Border color */
    
    /* Secondary accent */
    --color-accent: #ff6b35;         /* Secondary orange */
}
```

### Popular Color Schemes

**Blue Professional:**
```css
--color-primary: #0066ff;
--color-dark: #0f1419;
--color-warm: #e8f4ff;
--color-accent: #0052cc;
```

**Green Modern:**
```css
--color-primary: #10b981;
--color-dark: #0f1f1a;
--color-warm: #ecfdf5;
--color-accent: #059669;
```

**Purple Creative:**
```css
--color-primary: #8b5cf6;
--color-dark: #1a1a2e;
--color-warm: #f5f3ff;
--color-accent: #a78bfa;
```

**Red Professional:**
```css
--color-primary: #dc2626;
--color-dark: #1a1a1a;
--color-warm: #ffe8e8;
--color-accent: #b91c1c;
```

### Apply Custom Colors

1. Open `index.html` in text editor
2. Find the `:root { }` CSS section (around line 19-36)
3. Change the hex color values
4. Save file
5. Refresh browser (Ctrl+F5)

**Example:**
```css
/* Before */
--color-primary: #e8590c;

/* After - change to blue */
--color-primary: #0066ff;
```

---

## 📝 Personalizing Content

### Section 1: Hero Section

**Find in HTML:**
```html
<section class="hero" id="home">
    <h1>MOE-KYAW-AUNG</h1>
    <p class="tagline">Android Senior Developer</p>
    <p>12 years of hands-on experience...</p>
</section>
```

**Changes to make:**
1. Replace "MOE-KYAW-AUNG" with your name
2. Change "Android Senior Developer" to your title
3. Update description paragraph

**Example:**
```html
<h1>JOHN DEVELOPER</h1>
<p class="tagline">Full Stack Engineer</p>
<p>10+ years building scalable web applications...</p>
```

### Section 2: About Me

**Find in HTML:**
```html
<section class="about" id="about">
    <h2 class="section-title scroll-fade">About Me</h2>
    <div class="about-grid scroll-fade">
        <div class="about-image">
            <img src="..." alt="Profile">
        </div>
        <div class="about-content">
            <h3>Android Developer | Tech Enthusiast...</h3>
            <p>With nearly 12 years...</p>
```

**Changes to make:**
1. Replace profile image URL
2. Update about text
3. Modify statistics (years, projects, clients)
4. Change job title/description

**Example:**
```html
<h3>Software Engineer | Problem Solver</h3>
<p>With 5+ years of professional development experience...</p>

<!-- Update stats -->
<div class="stat-item">
    <div class="stat-number">5+</div>
    <div class="stat-label">Years Experience</div>
</div>
```

### Section 3: Skills

**Find in HTML:**
```html
<section class="skills" id="skills">
    <h2 class="section-title scroll-fade">Technical Skills</h2>
    <div class="skills-grid">
        <div class="skill-category scroll-fade">
            <h3>Languages & Frameworks</h3>
            <ul class="skill-list">
                <li>Kotlin</li>
                <li>Java</li>
```

**Changes to make:**
1. Modify skill categories (or keep existing)
2. Add/remove skills from lists
3. Add new categories if needed

**Example - Add new category:**
```html
<div class="skill-category scroll-fade">
    <h3>Database & DevOps</h3>
    <ul class="skill-list">
        <li>PostgreSQL</li>
        <li>Docker</li>
        <li>Kubernetes</li>
    </ul>
</div>
```

### Section 4: Projects/Portfolio

**Find in HTML:**
```html
<section class="projects" id="projects">
    <h2 class="section-title scroll-fade">Featured Projects</h2>
    <div class="masonry-grid">
        <div class="masonry-item scroll-fade">
            <div class="masonry-image">
                <img src="..." alt="Video Player App">
            </div>
            <div class="masonry-content">
                <h3>Video Player App</h3>
                <p>Advanced video streaming...</p>
                <div class="project-tags">
                    <span class="tag">Kotlin</span>
```

**Changes to make:**
1. Replace image URLs with your project images
2. Update project titles and descriptions
3. Modify technology tags
4. Add/remove projects

**Example:**
```html
<div class="masonry-item scroll-fade">
    <div class="masonry-image">
        <img src="your-image.jpg" alt="E-Commerce App">
    </div>
    <div class="masonry-content">
        <h3>E-Commerce Platform</h3>
        <p>Full-stack e-commerce solution with payment integration.</p>
        <div class="project-tags">
            <span class="tag">React</span>
            <span class="tag">Node.js</span>
            <span class="tag">MongoDB</span>
        </div>
    </div>
</div>
```

### Section 5: Testimonials

**Find in HTML:**
```html
<section class="testimonials" id="testimonials">
    <div class="carousel-slide active">
        <p>"Moe is an exceptional Android developer..."</p>
        <div class="carousel-author">Sarah Johnson</div>
        <div class="carousel-title">CTO, Tech Startup</div>
    </div>
```

**Changes to make:**
1. Replace testimonial quotes
2. Update author names
3. Change job titles/companies
4. Add/remove testimonials (edit JavaScript too)

### Section 6: Pricing

**Find in HTML:**
```html
<section class="pricing" id="pricing">
    <div class="pricing-card scroll-fade">
        <div class="price-label">Basic Package</div>
        <div class="price"><span class="price-currency">$</span>1,500</div>
        <ul class="pricing-features">
            <li>Mobile App Development</li>
```

**Changes to make:**
1. Update package names
2. Change prices
3. Modify feature lists
4. Add/remove packages

### Section 7: Contact Information

**Find in HTML:**
```html
<section class="contact" id="contact">
    <!-- Contact Information -->
    <p style="..."><a href="tel:+959889000889">+95 9 889 000 889</a></p>
    <p style="..."><a href="mailto:moekyawaung@programmer.net">moekyawaung@programmer.net</a></p>
    <p style="...">Myanmar / Southeast Asia</p>
```

**Changes to make:**
1. Update phone number
2. Change email address
3. Modify location
4. Update social media links

### Section 8: Footer

**Find in HTML:**
```html
<footer>
    <div class="footer-grid">
        <div class="footer-column">
            <h3>Quick Links</h3>
            <ul class="footer-links">
                <li><a href="#home">Home</a></li>
```

**Changes to make:**
1. Update footer links
2. Change social media URLs
3. Modify company/copyright info
4. Add new footer sections

---

## 🔤 Changing Fonts & Typography

### Method 1: Using Google Fonts

**Current Fonts:**
```html
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Playfair+Display:wght@700&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
```

**Change fonts:**

1. Visit [Google Fonts](https://fonts.google.com/)
2. Search for desired fonts
3. Select weights you need (400, 700)
4. Click "Embed" tab
5. Copy the `<link>` tag
6. Replace in HTML `<head>` section

**Popular Font Combinations:**

**Modern Professional:**
```html
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&family=Lora:wght@700&family=Open+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet">
```

**Minimal Clean:**
```html
<link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;600&family=Abril+Fatface&family=Roboto:wght@300;400;500;600;700&display=swap" rel="stylesheet">
```

**Creative Bold:**
```html
<link href="https://fonts.googleapis.com/css2?family=Courier+Prime:wght@400;700&family=Bebas+Neue&family=Nunito:wght@300;400;600;700&display=swap" rel="stylesheet">
```

### Method 2: Update Font Family in CSS

```css
/* Find these in the <style> section */
h1, h2, h3, h4, h5, h6 {
    font-family: 'Space Mono', monospace;  /* Change this */
    font-weight: 700;
}

.font-display {
    font-family: 'Playfair Display', serif;  /* Or this */
    font-weight: 700;
}

body {
    font-family: 'Inter', sans-serif;  /* Or this */
}
```

**Example - Change to different fonts:**
```css
h1, h2, h3, h4, h5, h6 {
    font-family: 'IBM Plex Mono', monospace;  /* Changed */
}

.font-display {
    font-family: 'Abril Fatface', serif;  /* Changed */
}

body {
    font-family: 'Open Sans', sans-serif;  /* Changed */
}
```

### Typography Size Adjustments

**Change heading sizes:**
```css
h1 {
    font-size: clamp(32px, 8vw, 72px);  /* Min, responsive, max */
}

h2 {
    font-size: clamp(24px, 6vw, 48px);
}
```

**Change body text size:**
```css
body {
    font-size: 16px;  /* Change default */
    line-height: 1.6;  /* Change line spacing */
}

p {
    font-size: 1rem;
    line-height: 1.8;  /* Increase for more spacing */
}
```

---

## 🖼️ Customizing Images

### Method 1: Replace with Your Images

**Hero Background - Particle Canvas**
The hero section uses a Canvas-based particle system. To replace with static image:

```html
<!-- Find this section and modify -->
<section class="hero" id="home">
    <!-- Add background image -->
    <style>
        .hero {
            background-image: url('your-image.jpg');
            background-size: cover;
            background-position: center;
        }
    </style>
```

**Profile Image in About Section:**
```html
<div class="about-image">
    <img src="your-profile.jpg" alt="Your Name" loading="lazy">
</div>
```

**Project Images:**
```html
<div class="masonry-image">
    <img src="your-project-1.jpg" alt="Project Name">
</div>
```

**Gallery Images:**
```html
<div class="gallery-item" onclick="openLightbox(this.querySelector('img').src)">
    <img src="your-gallery-image.jpg" alt="Gallery Item" loading="lazy">
</div>
```

### Method 2: Using External Image Services

**Cloudinary (Current):**
```html
<img src="https://res.cloudinary.com/your-cloud-name/image/upload/v1234567890/image-name.jpg">
```

**Imgur:**
```html
<img src="https://imgur.com/your-image-id.jpg">
```

**Unsplash (Free):**
```html
<img src="https://source.unsplash.com/800x600/?technology">
```

**Pexels (Free):**
```html
<img src="https://images.pexels.com/photos/123456/pexels-photo-123456.jpeg">
```

### Method 3: Optimize Images

**Compressed sizes for better performance:**

```html
<!-- Use srcset for responsive images -->
<img src="image-medium.jpg"
     srcset="image-small.jpg 500w,
             image-medium.jpg 1000w,
             image-large.jpg 1500w"
     sizes="(max-width: 500px) 100vw,
            (max-width: 1000px) 50vw,
            33vw"
     alt="Description">
```

---

## 🔧 Modifying Components

### 1. Navigation Bar

**Change logo text:**
```html
<div class="logo">MKA V47</div>  <!-- Change to your name/brand -->
```

**Add/remove navigation links:**
```html
<div class="desktop-nav">
    <a href="#about">About</a>
    <a href="#skills">Skills</a>
    <a href="#projects">Projects</a>
    <!-- Add new links -->
    <a href="#blog">Blog</a>
</div>
```

### 2. Hero Section Buttons

**Change button text and links:**
```html
<div class="cta-group">
    <a href="#projects" class="btn btn-primary">View Work</a>
    <a href="#contact" class="btn">Get in Touch</a>
</div>
```

**Style buttons:**
```css
.btn {
    padding: 12px 30px;  /* Change padding */
    font-size: 12px;  /* Change size */
}

.btn-primary {
    background-color: var(--color-primary);
    color: var(--color-dark);
}
```

### 3. Social Media Icons

**Update social links in footer:**
```html
<div class="social-icons">
    <a href="https://github.com/your-username" class="social-icon">
        <i class="fab fa-github"></i>
    </a>
    <a href="https://linkedin.com/in/your-profile" class="social-icon">
        <i class="fab fa-linkedin"></i>
    </a>
    <!-- Add more -->
</div>
```

**Available icons from Font Awesome:**
```
fa-github, fa-linkedin, fa-twitter, fa-youtube, fa-facebook,
fa-instagram, fa-dribbble, fa-codepen, fa-stack-overflow,
fa-behance, fa-medium, fa-dev, fa-mastodon, fa-discord
```

---

## 🎯 Advanced Customization

### 1. Adding New Sections

**HTML structure:**
```html
<section id="new-section">
    <h2 class="section-title scroll-fade">Section Title</h2>
    <div class="content-area">
        <!-- Your content -->
    </div>
</section>
```

**CSS for new section:**
```css
#new-section {
    padding: 80px 20px;
}

#new-section .section-title {
    color: var(--color-primary);
}
```

**JavaScript for interactivity:**
```javascript
// In the <script> section
document.getElementById('new-section').addEventListener('click', () => {
    // Your code here
});
```

### 2. Modifying Animations

**Change scroll fade animation:**
```css
.scroll-fade {
    opacity: 0;
    transform: translateY(30px);  /* Change 30px to desired value */
    transition: opacity 0.6s ease, transform 0.6s ease;  /* Change 0.6s */
}
```

**Change particle animation speed:**
```javascript
// Find in hero canvas animation
const increment = finalValue / 30;  /* Change 30 - lower = faster */
const timer = setInterval(() => {
    // ...
}, 30);  /* Change 30ms interval */
```

### 3. Custom CSS Rules

**Add custom styles before closing `</style>` tag:**
```css
/* Your custom styles */
.custom-class {
    background: linear-gradient(135deg, var(--color-primary), var(--color-accent));
    padding: 20px;
    border-radius: 8px;
}

/* Responsive custom styles */
@media (max-width: 768px) {
    .custom-class {
        padding: 15px;
    }
}
```

---

## 📚 CSS Variables Reference

### Complete CSS Variables List

```css
:root {
    /* Colors */
    --color-primary: #e8590c;              /* Main accent */
    --color-dark: #1a1a1a;                 /* Dark background */
    --color-dark-lighter: #2a2a2a;         /* Slightly lighter dark */
    --color-warm: #FFF7ED;                 /* Light accent */
    --color-text-dark: #333333;            /* Dark text */
    --color-text-light: #f5f5f5;           /* Light text */
    --color-border: #404040;               /* Border color */
    --color-accent: #ff6b35;               /* Secondary accent */
    
    /* Shadows */
    --shadow-sm: 0 2px 4px rgba(0, 0, 0, 0.1);
    --shadow-md: 0 4px 12px rgba(0, 0, 0, 0.15);
    --shadow-lg: 0 12px 32px rgba(0, 0, 0, 0.2);
    
    /* Transitions */
    --transition-fast: 0.2s ease;
    --transition-base: 0.3s ease;
    --transition-slow: 0.5s ease;
}
```

### Using CSS Variables

```css
/* Apply to any element */
.element {
    background-color: var(--color-primary);
    color: var(--color-text-light);
    box-shadow: var(--shadow-md);
    transition: all var(--transition-base);
}
```

---

## 🎨 Common Customizations

### 1. Change Overall Theme

**To a blue theme:**
```css
:root {
    --color-primary: #0066ff;
    --color-accent: #0052cc;
    --color-dark: #0f1419;
    --color-warm: #e8f4ff;
}
```

### 2. Adjust Spacing

**Increase padding in sections:**
```css
section {
    padding: 120px 20px;  /* Increased from 80px */
}
```

**Change margins in text:**
```css
h2 {
    margin-bottom: 80px;  /* Increased from 60px */
}

p {
    margin-bottom: 20px;  /* Adjust as needed */
}
```

### 3. Modify Border Styles

**Change from sharp to rounded:**
```css
/* Find and change border-radius */
.btn {
    border-radius: 20px;  /* More rounded */
}

.pricing-card {
    border-radius: 12px;  /* Slightly rounded */
}
```

### 4. Add Animations to New Elements

```html
<div class="scroll-fade">
    Content that fades in on scroll
</div>
```

### 5. Create Custom Color Scheme

```css
/* Dark Red Theme */
:root {
    --color-primary: #dc2626;
    --color-accent: #b91c1c;
    --color-dark: #1a1a1a;
    --color-warm: #ffe8e8;
}

/* Update text colors for contrast */
body.light-mode {
    background-color: var(--color-warm);
    color: #8b0000;
}
```

---

## 📋 Customization Checklist

Before deploying, customize these essentials:

- [ ] Hero section name and title
- [ ] About section biography
- [ ] Profile image
- [ ] Skills and technologies
- [ ] Projects with images
- [ ] Testimonials with real feedback
- [ ] Pricing/services information
- [ ] Contact email and phone
- [ ] Social media links
- [ ] Footer information
- [ ] Color scheme (optional)
- [ ] Fonts (optional)

---

## 🔄 Rolling Back Changes

If you make a mistake:

```bash
# Using Git (if you cloned repository)
git checkout index.html  # Revert to original

# Or create backup
cp index.html index.html.backup
```

---

## 💡 Pro Tips

1. **Test Changes**
   - Refresh browser with Ctrl+F5
   - Test on mobile size
   - Check all browsers

2. **Use DevTools**
   - F12 to inspect elements
   - Change CSS in real-time to preview
   - Check console for errors

3. **Comments for Reference**
   - Keep inline comments
   - Note your custom CSS
   - Date important changes

4. **Version Control**
   - Use Git to track changes
   - Commit regularly
   - Easy to compare versions

---

## 🚀 Next Steps After Customization

1. **Test Everything**
   - Click all buttons
   - Submit forms
   - Toggle dark mode
   - Check on mobile

2. **Validate Code**
   - Run HTML validator
   - Check JavaScript console
   - Verify images load

3. **Optimize**
   - Compress images
   - Minify CSS/JS (optional)
   - Test performance

4. **Deploy**
   - See [DEPLOYMENT.md](./DEPLOYMENT.md)
   - Push to GitHub
   - Set up hosting

---

## 📞 Need Help?

- Check inline comments in `index.html`
- Review [README.md](./README.md) for overview
- See [FEATURES.md](./FEATURES.md) for details
- Check [GitHub Issues](https://github.com/moekyawaung-tech/portfolio-v47/issues)

---

**Last Updated:** January 2026  
**Version:** 47  
**Status:** ✅ Production Ready

Happy customizing! 🎨
