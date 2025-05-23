# Detailed Accessibility Issues Breakdown

This document provides a comprehensive breakdown of all accessibility violations demonstrated in the `accessibility-issues-demo.html` file, along with their fixes shown in `accessibility-fixed-demo.html`.

## Issues Summary

| # | Issue | WCAG Guideline | Level | Severity | Fixed |
|---|-------|----------------|-------|----------|-------|
| 1 | Missing lang attribute | 3.1.1 | A | Serious | ✅ |
| 2 | Poor color contrast | 1.4.3 | AA | Serious | ✅ |
| 3 | No focus indicators | 2.4.7 | AA | Serious | ✅ |
| 4 | Improper heading hierarchy | 1.3.1 | A | Moderate | ✅ |
| 5 | Missing skip link | 2.4.1 | A | Minor | ✅ |
| 6 | Image without alt text | 1.1.1 | A | Critical | ✅ |
| 7 | Inappropriate alt text | 1.1.1 | A | Minor | ✅ |
| 8 | Non-descriptive links | 2.4.4 | A | Moderate | ✅ |
| 9 | Form without labels | 1.3.1, 3.3.2 | A | Critical | ✅ |
| 10 | No label association | 1.3.1 | A | Critical | ✅ |
| 11 | Color-only information | 1.4.1 | A | Serious | ✅ |
| 12 | Auto-playing media | 1.4.2 | A | Minor | ✅ |
| 13 | Empty link | 2.4.4 | A | Serious | ✅ |
| 14 | Improper button markup | 4.1.2 | A | Serious | ✅ |
| 15 | Table without headers | 1.3.1 | A | Serious | ✅ |
| 16 | Text too small | 1.4.4 | AA | Moderate | ✅ |
| 17 | Missing required indicators | 3.3.2 | A | Moderate | ✅ |
| 18 | Nested interactive elements | 4.1.2 | A | Serious | ✅ |
| 19 | Missing form validation | 3.3.1 | A | Moderate | ✅ |

## Detailed Issue Analysis

### 1. Missing Language Attribute (WCAG 3.1.1)

**Issue**: `<html>` tag missing `lang` attribute
```html
<html> <!-- Missing lang attribute -->