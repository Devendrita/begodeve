# UX Designer Portfolio

A clean, minimalist portfolio showcasing thoughtful, human-centered design work. Built with semantic HTML, accessible design patterns, and thoughtful interactions.

## 🌐 Live Site

Visit the portfolio at: `https://[your-username].github.io/[repository-name]`

## ✨ Features

- **Fully accessible** - WCAG 2.1 compliant with semantic HTML, ARIA labels, and keyboard navigation
- **Responsive design** - Works seamlessly on mobile, tablet, and desktop
- **Smooth interactions** - Custom cursor, scroll animations, and thoughtful transitions
- **Case studies** - Four detailed project showcases with real-world impact
- **Performance optimized** - Minimal dependencies, fast load times

## 📁 Project Structure

```
portfolio/
├── index.html              # Main portfolio page
├── images/                 # All portfolio images
│   ├── loyalty-screens.jpg
│   ├── alsa-ticket-machines.jpg
│   ├── mental-models.jpg
│   ├── zebra-island.jpg
│   └── about-image.jpg
├── css/                    # (Optional) External stylesheets
├── js/                     # (Optional) External JavaScript
└── README.md              # You are here
```

## 🚀 Quick Start

### Option 1: Deploy to GitHub Pages (Recommended)

1. **Create a GitHub account** at [github.com](https://github.com) if you don't have one

2. **Create a new repository**
   - Click the '+' icon → New repository
   - Name it something like `portfolio` or `ux-portfolio`
   - Make it Public
   - Don't initialize with README (we already have one)

3. **Upload your files**
   - Click 'uploading an existing file'
   - Drag and drop ALL files from this folder
   - Commit changes

4. **Enable GitHub Pages**
   - Go to repository Settings
   - Scroll to "Pages" section
   - Under "Source", select `main` branch
   - Click Save
   - Your site will be live at `https://[username].github.io/[repository-name]`

### Option 2: Run Locally

Simply open `index.html` in your web browser. No server needed!

## 🎨 Customization Guide

### Update Your Information

**Contact Links** (Line 565-577 in index.html):
```html
<a href="mailto:your-email@example.com">your-email@example.com</a>
<a href="https://linkedin.com/in/yourprofile">LinkedIn</a>
```

**Case Study Links**:
Replace placeholder URLs in each case study:
- `case-study-loyalty.html`
- `case-study-ticket-machines.html`
- `case-study-mental-models.html`
- `case-study-onboarding.html`

**Colors** (Line 15-20 in index.html):
```css
:root {
    --text: #1a1a1a;      /* Main text color */
    --bg: #fafafa;        /* Background color */
    --accent: #4a90e2;    /* Links and accents */
    --subtle: #e8e8e8;    /* Borders and subtle elements */
}
```

### Add More Case Studies

Copy an existing `<article>` block and update:
- Image path
- Heading ID
- Title, meta, and description
- Link URL

## 🎯 Understanding Git (Designer's Guide)

Think of Git like layers in design software, but for code:

### The Visual Model

```
YOUR COMPUTER                    GITHUB (Cloud)
┌─────────────┐                 ┌─────────────┐
│             │                 │             │
│  Working    │   git add →     │  Staging    │   git commit →    
│  Directory  │                 │  Area       │   
│             │                 │             │
│  (Your      │                 │  (Ready to  │   git push →  ┌──────────┐
│   files)    │                 │   save)     │               │ GitHub   │
│             │                 │             │               │ Repository│
└─────────────┘                 └─────────────┘               └──────────┘
```

### Key Commands (What They Actually Do)

**git add .**  
Think: "Mark all my changes to be saved"  
Like: Selecting all layers you want to export

**git commit -m "message"**  
Think: "Save a snapshot with a label"  
Like: Creating a named version in your design file history

**git push**  
Think: "Upload my saved versions to the cloud"  
Like: Syncing to Dropbox/Google Drive

**git pull**  
Think: "Download the latest version from the cloud"  
Like: Getting the latest file from a shared folder

### Your First Commit (Step-by-Step)

```bash
# 1. Tell Git who you are (one-time setup)
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"

# 2. Create a new repository
git init

# 3. Add all your files
git add .

# 4. Save your first version
git commit -m "Initial portfolio launch"

# 5. Connect to GitHub
git remote add origin https://github.com/[username]/[repository-name].git

# 6. Upload everything
git push -u origin main
```

### Making Changes Later

```bash
# 1. Make your edits in index.html or other files

# 2. Check what changed
git status

# 3. Add your changes
git add .

# 4. Save with a descriptive message
git commit -m "Updated case study descriptions"

# 5. Upload to GitHub
git push
```

### Common Scenarios

**Scenario: You updated a case study**
```bash
git add index.html
git commit -m "Updated loyalty program case study"
git push
```

**Scenario: You added new images**
```bash
git add images/
git commit -m "Added new project screenshots"
git push
```

**Scenario: You want to see your history**
```bash
git log --oneline
# Shows all your saved versions
```

## ♿ Accessibility Features

- Semantic HTML5 elements
- ARIA labels and landmarks
- Skip to main content link
- Keyboard navigation support
- Focus indicators
- Screen reader friendly
- Reduced motion support
- High contrast ratios (WCAG AA+)
- Responsive text sizing

## 🔧 Technical Details

- **No build process** - Just HTML, CSS, and vanilla JavaScript
- **No dependencies** - Works offline, no npm/node required
- **Browser support** - Modern browsers (Chrome, Firefox, Safari, Edge)
- **Mobile-first** - Responsive design from 320px to 4K

## 📝 License

This portfolio template is free to use and customize for your own work.

## 💡 Tips

1. **Update regularly** - Keep your case studies current
2. **Test accessibility** - Use browser DevTools Lighthouse audits
3. **Optimize images** - Compress your JPGs before uploading (aim for < 500KB each)
4. **Custom domain** - You can point your own domain to GitHub Pages
5. **Analytics** - Add Google Analytics if you want to track visitors

## 🆘 Troubleshooting

**Site not showing up?**
- Wait 5-10 minutes after enabling GitHub Pages
- Check that index.html is in the root folder
- Verify repository is set to Public

**Images not loading?**
- Check file names match exactly (case-sensitive)
- Ensure images are in the `images/` folder
- Verify image paths start with `images/`

**Want to start over?**
- You can delete the repository and start fresh
- Git never loses data unless you force it to

## 📧 Questions?

Feel free to reach out or check [GitHub's documentation](https://docs.github.com/en/pages)

---

Built with ❤️ and attention to detail
