# 🚀 Deployment Checklist

Follow these steps to get your portfolio live on GitHub Pages.

## Pre-Flight Check ✈️

Before deploying, make sure you've:

- [ ] Updated contact email in `index.html` (line 565)
- [ ] Updated social media links in `index.html` (lines 566-577)
- [ ] Customized the page title and meta description (lines 6-7)
- [ ] Replaced placeholder case study links with real URLs (or "#" temporarily)
- [ ] Tested the site locally by opening `index.html` in your browser
- [ ] Checked that all images load correctly

## Deployment Steps

### 1. Create GitHub Account
- Go to [github.com](https://github.com)
- Click "Sign up"
- Choose username (will be in your site URL)
- Verify email

### 2. Create Repository
- Click "+" icon → "New repository"
- Repository name: `portfolio` (or any name you prefer)
- Description: "UX Designer Portfolio"
- Select: **Public**
- ❌ Do NOT check "Add a README file"
- Click "Create repository"

### 3. Upload Files

**Option A: Web Interface (Easiest)**
1. On your new repository page, click "uploading an existing file"
2. Drag these files from your computer:
   - `index.html`
   - `README.md`
   - `GIT_GUIDE.md`
   - `ACCESSIBILITY.md`
   - The entire `images/` folder
3. Write commit message: "Initial portfolio launch"
4. Click "Commit changes"

**Option B: Command Line (If you're comfortable)**
```bash
cd /path/to/your/portfolio/folder
git init
git add .
git commit -m "Initial portfolio launch"
git branch -M main
git remote add origin https://github.com/USERNAME/REPO-NAME.git
git push -u origin main
```

### 4. Enable GitHub Pages
1. Go to repository **Settings** (top nav)
2. Scroll to **Pages** section (left sidebar)
3. Under "Source":
   - Branch: Select `main`
   - Folder: Select `/ (root)`
4. Click **Save**
5. Wait 2-5 minutes

### 5. Visit Your Live Site
- Your site will be at: `https://USERNAME.github.io/REPO-NAME`
- GitHub will show you the exact URL in the Pages settings
- Bookmark it!

## Post-Deployment

### Test Your Live Site
- [ ] All pages load
- [ ] All images display
- [ ] Navigation works
- [ ] Links open correctly
- [ ] Mobile responsive
- [ ] Works in incognito/private mode

### Share Your Portfolio
- [ ] Add URL to LinkedIn profile
- [ ] Add URL to resume
- [ ] Add URL to email signature
- [ ] Share on social media

### Set Up Custom Domain (Optional)
1. Buy a domain (namecheap.com, hover.com, etc.)
2. In repository Settings → Pages → Custom domain
3. Enter your domain (e.g., `yourname.com`)
4. Follow DNS configuration instructions

## Updating Your Portfolio

Every time you make changes:

**Via Web:**
1. Click on file in GitHub
2. Click pencil icon to edit
3. Make changes
4. Commit changes
5. Wait ~1 minute for site to update

**Via Command Line:**
```bash
# Make your edits locally
git add .
git commit -m "Describe what you changed"
git push
# Wait ~1 minute for GitHub Pages to update
```

## Troubleshooting

### Site not showing up?
- **Wait** - Takes 5-10 minutes first time
- **Check** - Repository must be Public
- **Verify** - index.html must be in root folder
- **Try** - Hard refresh (Cmd/Ctrl + Shift + R)

### Images not loading?
- **Check filenames** - Case sensitive! `Image.jpg` ≠ `image.jpg`
- **Verify paths** - Should be `images/filename.jpg`
- **Test locally** - Do images load when opening index.html?

### Changes not appearing?
- **Wait** - Updates take 30-60 seconds
- **Clear cache** - Hard refresh your browser
- **Check commit** - Did changes actually save to GitHub?

### 404 Error?
- **Check URL** - Should include repository name
- **Branch** - Must be deploying from `main` branch
- **Root folder** - index.html must be at root level

## Performance Optimization (Optional)

### Compress Images
Before uploading, compress your images:
- Use [TinyPNG](https://tinypng.com/) or [Squoosh](https://squoosh.app/)
- Aim for under 500KB per image
- JPGs at 80-85% quality look great

### Add Analytics
To track visitors:
1. Create [Google Analytics](https://analytics.google.com/) account
2. Get tracking code
3. Add before `</head>` in index.html
4. Commit and push

### SEO Improvements
- [ ] Update page title to include your name
- [ ] Write compelling meta description
- [ ] Add Open Graph tags for social sharing
- [ ] Submit to Google Search Console

## Maintenance Schedule

**Weekly:**
- Check for broken links
- Review analytics (if added)

**Monthly:**
- Update case studies with new work
- Refresh "Thoughts" section with new posts
- Test site on new browser versions

**Quarterly:**
- Review and update bio
- Add new projects
- Optimize images
- Check accessibility

## Next Steps

Now that your portfolio is live:

1. **Share it** - Add to all your professional profiles
2. **Monitor it** - Set up uptime monitoring (uptimerobot.com)
3. **Iterate** - Keep improving based on feedback
4. **Learn Git** - Read the GIT_GUIDE.md for deeper understanding
5. **Test accessibility** - Follow ACCESSIBILITY.md checklist

## Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Custom Domain Setup](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)
- [GitHub Desktop](https://desktop.github.com/) - GUI alternative to command line
- [VS Code](https://code.visualstudio.com/) - Great code editor

## Need Help?

- GitHub Support: [support.github.com](https://support.github.com/)
- Stack Overflow: [stackoverflow.com/questions/tagged/github-pages](https://stackoverflow.com/questions/tagged/github-pages)
- GitHub Community: [github.community](https://github.community/)

---

**Congratulations! 🎉**

You've just deployed a professional, accessible portfolio site. Keep it updated and let it work for you!
