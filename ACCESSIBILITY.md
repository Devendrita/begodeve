# Accessibility Checklist ♿

This portfolio has been built with WCAG 2.1 Level AA standards in mind. Here's what's included and how to test it.

## ✅ What's Already Built In

### Semantic HTML
- ✓ Proper heading hierarchy (H1 → H2 → H3)
- ✓ Semantic elements (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`)
- ✓ `<time>` elements for dates
- ✓ Descriptive `alt` attributes on images

### Keyboard Navigation
- ✓ Skip to main content link (press Tab on page load)
- ✓ All interactive elements keyboard accessible
- ✓ Focus indicators visible
- ✓ Escape key to blur elements
- ✓ Smooth scroll with focus management

### Screen Readers
- ✓ ARIA labels on navigation
- ✓ ARIA landmarks for page structure
- ✓ Progress bar with live updates
- ✓ Visually hidden text for context ("opens in new tab")
- ✓ Proper link context

### Visual Design
- ✓ High contrast ratios (4.5:1 minimum)
- ✓ Responsive text sizing
- ✓ No color-only information
- ✓ Touch targets min 44x44px
- ✓ Reduced motion support

### Forms & Interaction
- ✓ Clear link purpose
- ✓ No keyboard traps
- ✓ Consistent navigation
- ✓ Descriptive page title

## 🧪 How to Test Accessibility

### 1. Keyboard-Only Test (5 minutes)

**Unplug your mouse and try:**

```
1. Press Tab repeatedly
   → Should highlight each interactive element
   → Should show visible focus ring
   
2. Press Shift+Tab
   → Should go backwards through elements
   
3. Press Enter on links
   → Should navigate to target
   
4. Press Escape
   → Should blur current element
   
5. Try navigating entire site
   → Can you reach everything?
   → Is the tab order logical?
```

**Pass criteria:**
- Every interactive element is reachable
- Focus indicators always visible
- Tab order makes sense
- No keyboard traps

### 2. Screen Reader Test (10 minutes)

**Mac (VoiceOver):**
```
1. Press Cmd+F5 to start VoiceOver
2. Press Ctrl+Option+U for rotor
3. Use arrow keys to navigate headings
4. Listen to page structure
5. Press Cmd+F5 to stop
```

**Windows (NVDA - free):**
```
1. Download NVDA from nvaccess.org
2. Install and start NVDA
3. Press H to jump between headings
4. Press K to jump between links
5. Listen to how content is announced
```

**What to check:**
- Headings describe content accurately?
- Links make sense out of context?
- Images have meaningful descriptions?
- Form labels are clear?
- Page structure makes sense?

### 3. Visual Contrast Test (3 minutes)

**Use WebAIM Contrast Checker:**
1. Go to https://webaim.org/resources/contrastchecker/
2. Test main text: `#1a1a1a` on `#fafafa`
3. Test accent color: `#4a90e2` on `#fafafa`
4. All should pass AA (4.5:1)

**Or use browser DevTools:**
1. Right-click any text → Inspect
2. Look for contrast ratio in color picker
3. Should show checkmarks for AA/AAA

### 4. Zoom Test (2 minutes)

```
1. Press Cmd/Ctrl + Plus (+) to zoom to 200%
   → Content should remain readable
   → No horizontal scrolling on desktop
   → Nothing should overlap or cut off

2. Zoom to 400%
   → Should still be usable (mobile-like)
   
3. Reset with Cmd/Ctrl + 0
```

### 5. Mobile/Touch Test (5 minutes)

```
1. Open on phone or tablet
2. Try tapping all interactive elements
   → Touch targets at least 44x44px
   → No accidental touches
   
3. Rotate device
   → Should work in both orientations
   
4. Test with screen reader
   → iOS: Settings → Accessibility → VoiceOver
   → Android: Settings → Accessibility → TalkBack
```

### 6. Automated Testing Tools

**Lighthouse (Built into Chrome):**
```
1. Open Chrome DevTools (F12)
2. Go to Lighthouse tab
3. Select "Accessibility"
4. Click "Generate report"
5. Should score 95+ (100 is ideal)
```

**WAVE Extension:**
```
1. Install WAVE extension for Chrome/Firefox
2. Click extension icon on your page
3. Review any errors or alerts
4. Fix issues if found
```

**axe DevTools:**
```
1. Install axe DevTools extension
2. Open DevTools → axe tab
3. Click "Scan ALL of my page"
4. Review issues
```

## 🎯 WCAG 2.1 Level AA Checklist

### Perceivable

- [x] Text alternatives for non-text content
- [x] Captions for multimedia (N/A - no video/audio)
- [x] Content structured semantically
- [x] Color not sole means of conveying information
- [x] Contrast ratio at least 4.5:1 for text
- [x] Text can be resized to 200%
- [x] Images of text avoided (none used)

### Operable

- [x] All functionality keyboard accessible
- [x] No keyboard traps
- [x] Enough time to read content
- [x] No content that causes seizures (no flashing)
- [x] Skip navigation link provided
- [x] Descriptive page title
- [x] Focus order makes sense
- [x] Link purpose clear from text
- [x] Multiple ways to navigate (nav + links)
- [x] Focus indicators visible
- [x] Target size adequate (44x44px minimum)

### Understandable

- [x] Language of page declared (`lang="en"`)
- [x] Navigation consistent across pages
- [x] Consistent identification of components
- [x] Error messages clear (N/A - no forms)
- [x] Labels and instructions provided (N/A - no forms)

### Robust

- [x] Valid HTML markup
- [x] ARIA used appropriately
- [x] Name, Role, Value for components
- [x] Status messages announced to screen readers

## 🔧 Common Issues to Avoid

### ❌ Don't Do This:
```html
<!-- Bad: Generic link text -->
<a href="case-study.html">Click here</a>

<!-- Bad: Image without alt -->
<img src="photo.jpg">

<!-- Bad: Div buttons -->
<div onclick="doSomething()">Submit</div>

<!-- Bad: Color-only indication -->
<span style="color: red;">Error</span>
```

### ✅ Do This Instead:
```html
<!-- Good: Descriptive link text -->
<a href="case-study.html">Read case study: Mental Models</a>

<!-- Good: Meaningful alt text -->
<img src="photo.jpg" alt="ALSA ticket machines in transit station">

<!-- Good: Semantic button -->
<button onclick="doSomething()">Submit</button>

<!-- Good: Text + color -->
<span class="error">
  <span class="visually-hidden">Error:</span>
  Field is required
</span>
```

## 📱 Mobile Accessibility

- Touch targets: 44x44px minimum
- No hover-only interactions
- Orientation agnostic
- Zoom enabled (no maximum-scale)
- Readable at arm's length

## 🌐 Browser Support

Tested and working in:
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile Safari (iOS 14+)
- Chrome Mobile (Android 10+)

## 📚 Resources

### Testing Tools
- [WAVE](https://wave.webaim.org/) - Accessibility evaluation
- [axe DevTools](https://www.deque.com/axe/devtools/) - Automated testing
- [Lighthouse](https://developers.google.com/web/tools/lighthouse) - Built into Chrome
- [Contrast Checker](https://webaim.org/resources/contrastchecker/)

### Guidelines
- [WCAG 2.1](https://www.w3.org/WAI/WCAG21/quickref/) - Official spec
- [WebAIM](https://webaim.org/) - Practical guides
- [A11y Project](https://www.a11yproject.com/) - Community resources
- [Inclusive Components](https://inclusive-components.design/) - Pattern library

### Screen Readers
- [NVDA](https://www.nvaccess.org/) - Free for Windows
- [JAWS](https://www.freedomscientific.com/products/software/jaws/) - Popular Windows reader
- [VoiceOver](https://www.apple.com/accessibility/voiceover/) - Built into Mac/iOS
- [TalkBack](https://support.google.com/accessibility/android/answer/6283677) - Built into Android

## 💡 Pro Tips

1. **Test early, test often** - Don't wait until the end
2. **Use real assistive tech** - Automated tools catch ~40% of issues
3. **Include disabled users** - Nothing beats real user testing
4. **Make it a habit** - Accessibility should be part of your workflow
5. **Stay curious** - Learn about different disabilities and assistive tech

## 🎓 Learning Path

1. Start with keyboard-only navigation
2. Learn VoiceOver/NVDA basics
3. Understand ARIA (but use sparingly)
4. Study color contrast
5. Practice with real screen readers

## Questions?

- [WebAIM Discussion List](https://webaim.org/discussion/)
- [A11y Slack](https://web-a11y.slack.com/)
- [r/accessibility](https://www.reddit.com/r/accessibility/)

---

Remember: Accessibility isn't a feature, it's a baseline. 🌟
