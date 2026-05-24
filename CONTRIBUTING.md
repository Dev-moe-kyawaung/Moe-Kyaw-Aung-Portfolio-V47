# 🤝 Contributing Guide

Thank you for your interest in contributing to Moe-Kyaw-Aung Portfolio V47!

---

## How to Contribute

### 1. Reporting Bugs

**Found a bug?** Please open an issue with:

- **Clear description** of the problem
- **Steps to reproduce** the bug
- **Expected behavior** vs actual behavior
- **Screenshots** if applicable
- **Browser/OS information**

**Example:**
```
Bug: Carousel doesn't advance on mobile
Steps: 
1. Open portfolio on iPhone
2. Click next button on testimonials
3. Slide doesn't change

Expected: Slide should advance
Actual: Nothing happens

Browser: Safari 14.1 on iOS 14.5
```

### 2. Suggesting Features

**Have an idea?** Please open an issue with:

- **Clear feature description**
- **Use case/benefit**
- **Proposed implementation** (optional)
- **Examples** from other projects

### 3. Submitting Code

#### Fork the Repository

```bash
# Fork on GitHub website
# Clone your fork
git clone https://github.com/YOUR_USERNAME/portfolio-v47.git
cd portfolio-v47
```

#### Create Feature Branch

```bash
# Create new branch
git checkout -b feature/your-feature-name

# Or for bug fixes
git checkout -b fix/bug-description

# Or for documentation
git checkout -b docs/documentation-update
```

#### Make Changes

1. **Code Quality**
   - Follow existing code style
   - Add comments for complex logic
   - Keep functions small and focused

2. **File Organization**
   - One feature per commit
   - Logical grouping
   - Clear file structure

3. **Testing**
   - Test in multiple browsers
   - Check responsive design
   - Verify functionality

#### Commit Changes

```bash
# Stage changes
git add .

# Commit with clear message
git commit -m "feat: add dark mode toggle"
git commit -m "fix: correct carousel timing issue"
git commit -m "docs: update installation guide"

# Commit message format: type: description
# Types: feat, fix, docs, style, refactor, perf, test
```

#### Push & Create Pull Request

```bash
# Push to your fork
git push origin feature/your-feature-name

# Create pull request on GitHub
# - Clear title
# - Detailed description
# - Reference related issues
# - Describe testing done
```

---

## Code Style Guidelines

### HTML Standards

```html
<!-- Use semantic HTML5 elements -->
<section>
    <h2>Section Title</h2>
    <p>Description text</p>
</section>

<!-- Proper indentation (4 spaces) -->
<div class="container">
    <div class="item">
        <p>Content</p>
    </div>
</div>

<!-- Self-closing tags without slash -->
<img src="image.jpg" alt="Description">
<input type="text">

<!-- Always include alt text for images -->
<img src="image.jpg" alt="Descriptive text for accessibility">
```

### CSS Standards

```css
/* Use CSS variables for colors */
.element {
    color: var(--color-primary);
    background-color: var(--color-dark);
}

/* Proper spacing and indentation */
.class-name {
    property: value;
    another-property: value;
}

/* Comment your CSS */
/* Main heading styles */
h1 {
    font-size: 48px;
}

/* Mobile responsive media queries */
@media (max-width: 768px) {
    .class-name {
        font-size: 32px;
    }
}

/* Use consistent naming */
.component-name { }
.component-name__element { }
.component-name--modifier { }
```

### JavaScript Standards

```javascript
// Use descriptive variable names
const navigationMenu = document.getElementById('mobileMenu');

// Use const for constants, let for variables
const MAX_ITEMS = 10;
let currentIndex = 0;

// Clear function names
function handleMenuToggle() {
    // Implementation
}

// Arrow functions for callbacks
element.addEventListener('click', () => {
    // Handler code
});

// Comments for complex logic
// IntersectionObserver for scroll-triggered animations
const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            entry.target.classList.add('visible');
        }
    });
});

// Use console sparingly in production
console.log('Development log');

// Error handling
try {
    // Code that might fail
} catch (error) {
    console.error('Error description:', error);
}
```

---

## Commit Message Format

**Use semantic commits:**

```
<type>(<scope>): <subject>

<body>

<footer>
```

**Types:**
- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation
- `style:` Formatting/styling
- `refactor:` Code refactoring
- `perf:` Performance improvement
- `test:` Adding/updating tests
- `chore:` Build process/dependencies

**Examples:**
```
feat(carousel): add keyboard navigation support
fix(form): correct email validation regex
docs(readme): update installation instructions
perf: optimize particle animation rendering
style: improve code formatting and consistency
```

---

## Pull Request Guidelines

### Before Submitting

- [ ] Branch is up to date with main
- [ ] Commits are clean and descriptive
- [ ] Code follows style guidelines
- [ ] No console errors/warnings
- [ ] Tested on multiple browsers
- [ ] Responsive design verified
- [ ] Documentation updated (if needed)

### PR Description Template

```markdown
## Description
Brief description of what this PR does

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Performance improvement
- [ ] Code refactoring

## Testing
- Browser(s) tested: Chrome, Firefox, Safari
- Device(s) tested: Desktop, Tablet, Mobile
- Steps to test:
  1. Open site
  2. Perform action
  3. Verify result

## Screenshots (if applicable)
- Before
- After

## Related Issues
Closes #(issue number)

## Checklist
- [ ] Code follows style guidelines
- [ ] No new warnings generated
- [ ] Tests pass locally
- [ ] Documentation updated
- [ ] Changes are responsive
```

---

## Development Workflow

### Local Setup

```bash
# Clone repository
git clone https://github.com/YOUR_USERNAME/portfolio-v47.git
cd portfolio-v47

# Create feature branch
git checkout -b feature/new-feature

# Start local server
python -m http.server 8000

# Open browser
open http://localhost:8000
```

### During Development

1. **Make small, focused commits**
   ```bash
   git add specific-file.html
   git commit -m "feat: add new section"
   ```

2. **Test frequently**
   - After each change
   - In multiple browsers
   - On different screen sizes

3. **Keep code clean**
   - Remove console.logs
   - Fix linting warnings
   - Update comments

### Before Submitting PR

```bash
# Pull latest changes
git fetch origin
git merge origin/main

# Run final tests
# - Open in browser
# - Check DevTools console
# - Test all features

# Clean up commits if needed
git rebase -i HEAD~3  # Interactive rebase last 3 commits

# Push to your fork
git push origin feature/new-feature
```

---

## Testing Requirements

### Browser Compatibility
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

### Device Testing
- Desktop (1920x1080, 1366x768)
- Tablet (768x1024)
- Mobile (375x667, 414x896)

### Functionality Testing
- All buttons clickable
- Forms validatable
- Links working
- Animations smooth
- Responsive design working

### Performance Testing
- No console errors
- Images loading properly
- Fast initial load
- Smooth scrolling

---

## Documentation Requirements

For new features, update:

1. **README.md**
   - Add feature to overview
   - Include in features list

2. **FEATURES.md**
   - Document feature details
   - Add code examples

3. **Inline comments**
   - Comment new functions
   - Explain complex logic

4. **CHANGELOG.md**
   - Add entry under Unreleased
   - Include issue references

---

## Common Contribution Scenarios

### Adding a New Section

1. **HTML Structure**
   ```html
   <section id="new-section">
       <h2 class="section-title scroll-fade">Title</h2>
       <div class="content">
           <!-- Content here -->
       </div>
   </section>
   ```

2. **CSS Styling**
   ```css
   #new-section {
       padding: 80px 20px;
   }
   
   #new-section .content {
       max-width: 1200px;
       margin: 0 auto;
   }
   ```

3. **JavaScript (if needed)**
   ```javascript
   // Add event listeners
   document.getElementById('new-section').addEventListener('click', () => {
       // Handle interaction
   });
   ```

4. **Documentation**
   - Update README.md
   - Document in FEATURES.md
   - Add inline comments

### Fixing a Bug

1. **Identify the issue**
   - Reproduce consistently
   - Document steps
   - Find root cause

2. **Implement fix**
   - Minimal changes
   - Don't refactor unrelated code
   - Test thoroughly

3. **Verify fix**
   - Test original issue
   - Check for regressions
   - Test edge cases

4. **Document fix**
   - Clear commit message
   - Reference issue number
   - Update CHANGELOG.md

### Improving Performance

1. **Identify bottleneck**
   - Use DevTools
   - Measure metrics
   - Profile code

2. **Implement optimization**
   - Make targeted change
   - Measure improvement
   - Verify functionality

3. **Document improvement**
   - Note performance gain
   - Explain technique
   - Add comments

---

## Getting Help

- **GitHub Discussions:** Ask questions publicly
- **Issues:** Report bugs or request features
- **Email:** [moekyawaung@programmer.net](mailto:moekyawaung@programmer.net)

---

## Community Code of Conduct

### Be Respectful

- Treat everyone with respect
- Be welcoming to newcomers
- Listen to different perspectives
- Accept constructive criticism

### Be Constructive

- Provide helpful feedback
- Suggest improvements kindly
- Help others learn
- Collaborate positively

### Be Inclusive

- Use inclusive language
- Welcome diverse contributions
- Support underrepresented groups
- Create safe spaces

---

## Recognition

Contributors will be:
- Added to CONTRIBUTORS.md
- Mentioned in releases
- Featured in project updates

---

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

## FAQ

**Q: Can I contribute without coding?**
A: Yes! Documentation, translations, bug reports, and feedback are valuable contributions.

**Q: How long will review take?**
A: Usually 2-7 days depending on complexity.

**Q: Can I work on multiple features?**
A: Yes, but keep PRs focused. One feature per PR is preferred.

**Q: What if my PR is rejected?**
A: Feedback will be provided. You can revise and resubmit.

---

## Resources

- **[Git Basics](https://git-scm.com/book/en/v2)**
- **[GitHub Guides](https://guides.github.com/)**
- **[HTML Standards](https://html.spec.whatwg.org/)**
- **[CSS Best Practices](https://developer.mozilla.org/en-US/docs/Web/CSS)**
- **[JavaScript Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript)**

---

Thank you for contributing! 🙏

Your efforts help make this project better for everyone.

**Last Updated:** January 2026  
**Version:** 47
