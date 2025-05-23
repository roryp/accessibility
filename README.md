# WCAG Accessibility Demo

[![Accessibility Audit](https://github.com/roryp/wcag-accessibility-demo/actions/workflows/accessibility-audit.yml/badge.svg)](https://github.com/roryp/wcag-accessibility-demo/actions/workflows/accessibility-audit.yml)

An educational repository demonstrating common WCAG (Web Content Accessibility Guidelines) violations and their solutions, complete with automated accessibility testing via GitHub Actions.

## 🎯 Purpose

This repository serves as:
- **Educational resource** for learning about web accessibility
- **Testing playground** for accessibility auditing tools
- **CI/CD example** for implementing automated accessibility testing
- **Before/after comparison** showing the impact of accessibility fixes

## 📁 Repository Structure

```
├── index.html                          # Landing page with navigation
├── accessibility-issues-demo.html      # Page with intentional violations
├── accessibility-fixed-demo.html       # Corrected, accessible version
├── styles.css                         # Basic styling
├── package.json                       # Dependencies and scripts
├── .github/workflows/
│   └── accessibility-audit.yml        # Automated testing workflow
└── docs/
    └── ACCESSIBILITY_ISSUES.md        # Detailed issue breakdown
```

## 🚀 Quick Start

### View the Demo

1. **Online**: Visit the GitHub Pages site (if enabled)
2. **Locally**: 
   ```bash
   git clone https://github.com/roryp/wcag-accessibility-demo.git
   cd wcag-accessibility-demo
   npm install
   npm run serve
   ```
   Then open http://localhost:3000

### Run Accessibility Tests

```bash
# Test all pages
npm run test:all

# Test individual pages
npm run test:issues  # Should find violations
npm run test:fixed   # Should be mostly clean
npm run test:index   # Should be clean
```

## 🔍 What's Being Tested

The automated accessibility audit checks for violations of:

### WCAG 2.1 Level A & AA Guidelines
- **Perceivable**: Images, color contrast, text alternatives
- **Operable**: Keyboard navigation, focus management
- **Understandable**: Labels, language, instructions
- **Robust**: Valid markup, compatibility

### Automated Testing Tools
- **axe-core**: Industry-standard accessibility testing
- **GitHub Actions**: Continuous integration
- **Pull Request Comments**: Automated reporting

## 📊 Demo Pages

### 1. Issues Demo (`accessibility-issues-demo.html`)
Contains **20+ intentional violations** including:
- Missing `alt` attributes
- Poor color contrast
- Improper heading hierarchy
- Missing form labels
- Auto-playing media
- Non-semantic markup

### 2. Fixed Demo (`accessibility-fixed-demo.html`)
Shows the **corrected versions** with:
- Proper semantic HTML
- ARIA attributes where needed
- Keyboard accessibility
- Screen reader compatibility
- Clear visual hierarchy

### 3. Landing Page (`index.html`)
Clean, accessible navigation between demos

## 🤖 Automated Testing

### GitHub Actions Workflow

The repository includes a comprehensive accessibility testing workflow that:

1. **Runs on every push and PR**
2. **Tests all HTML pages** using axe-core
3. **Generates detailed reports** in JSON and Markdown formats
4. **Posts results as PR comments**
5. **Fails builds** if the "fixed" demo has critical issues
6. **Uploads artifacts** with full test results

### Test Criteria

- **Issues Demo**: Expected to have violations (for educational purposes)
- **Fixed Demo**: Must have 0 critical issues and ≤2 serious issues
- **Index Page**: Should be fully accessible

### Local Testing

```bash
# Install dependencies
npm install -g @axe-core/cli serve

# Start local server
npm run serve

# Run tests (in another terminal)
npm run test:all
```

## 📚 Educational Value

### For Developers
- See real examples of accessibility issues
- Understand WCAG guidelines in practice
- Learn how to implement fixes
- Experience testing tools and workflows

### For Teams
- Implement similar CI/CD accessibility testing
- Establish accessibility standards
- Create a culture of inclusive design
- Automate accessibility compliance checking

## 🛠️ Issues Demonstrated

| Issue Type | WCAG Guideline | Severity | Example |
|------------|----------------|----------|---------|
| Missing alt text | 1.1.1 | Critical | `<img src="..." >` |
| Poor contrast | 1.4.3 | Serious | Light gray on white |
| No focus indicators | 2.4.7 | Serious | `outline: none` |
| Missing labels | 3.3.2 | Critical | Unlabeled form inputs |
| Wrong heading order | 1.3.1 | Moderate | h1 → h4 → h2 |
| Auto-play media | 1.4.2 | Minor | `<audio autoplay>` |

See [ACCESSIBILITY_ISSUES.md](docs/ACCESSIBILITY_ISSUES.md) for complete details.

## 🔧 Testing Tools Integration

### Supported Tools
- **axe-core** (automated testing)
- **WAVE** (browser extension)
- **Lighthouse** (Chrome DevTools)
- **Screen readers** (NVDA, JAWS, VoiceOver)

### Browser Testing
- ✅ Chrome/Chromium
- ✅ Firefox
- ✅ Safari
- ✅ Edge

## 📈 Metrics & Reporting

The automated tests generate:
- **Violation counts** by severity level
- **WCAG guideline references**
- **Element selectors** for easy fixing
- **Before/after comparisons**
- **Trend analysis** over time

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Ensure accessibility tests pass
5. Submit a pull request

### Adding New Issues
When adding new accessibility violations to the issues demo:
1. Add clear HTML comments explaining the issue
2. Reference the specific WCAG guideline
3. Provide the fix in the fixed demo
4. Update documentation

## 📖 Resources

- [WCAG 2.1 Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)
- [axe-core Documentation](https://github.com/dequelabs/axe-core)
- [WebAIM Resources](https://webaim.org/)
- [MDN Accessibility](https://developer.mozilla.org/en-US/docs/Web/Accessibility)

## 📄 License

MIT License - see [LICENSE](LICENSE) for details.

## 🏷️ Tags

`accessibility` `wcag` `a11y` `education` `testing` `github-actions` `automation` `web-standards`

---

*Created to promote web accessibility awareness and best practices. Every user deserves an accessible web experience.*