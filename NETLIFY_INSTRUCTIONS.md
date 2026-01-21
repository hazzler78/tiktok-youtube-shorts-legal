# Netlify Drop Instructions

## Step-by-Step Guide

### Method 1: Drag the Legal Folder (Recommended)

1. **Open Netlify Drop**
   - Go to: https://app.netlify.com/drop
   - No account needed!

2. **Find your legal folder**
   - Navigate to: `d:\Cursor\program\TikTokYouTubeShort\legal\`
   - Make sure you see these files:
     - `terms-of-service.html`
     - `privacy-policy.html`
     - `index.html` (optional)

3. **Drag the ENTIRE folder**
   - Drag the `legal` folder into the Netlify Drop area
   - Wait for upload (you'll see progress)

4. **Get your URLs**
   - Netlify will show you a site URL like: `https://amazing-name-12345.netlify.app`
   - Your actual URLs will be:
     - Terms: `https://amazing-name-12345.netlify.app/legal/terms-of-service.html`
     - Privacy: `https://amazing-name-12345.netlify.app/legal/privacy-policy.html`

5. **Test the URLs**
   - Click on each URL to verify they work
   - You should see the HTML pages load correctly

### Method 2: Create a ZIP file

If dragging the folder doesn't work:

1. **Create a ZIP** of the `legal` folder
2. **Extract it** to a temporary location
3. **Drag the extracted folder** to Netlify Drop

### Common Issues

**404 Error?**
- Make sure you dragged the **folder**, not individual files
- The URL must include `/legal/` in the path
- Wait 1-2 minutes for Netlify to finish deploying

**Wrong URL format?**
- Netlify URLs should be: `https://[site-name].netlify.app/legal/[filename].html`
- Don't forget the `/legal/` part!

**Files not showing?**
- Make sure all HTML files are inside the `legal` folder
- Check that file names match exactly (case-sensitive)

## Alternative: GitHub Pages

If Netlify doesn't work, use GitHub Pages:

1. Create a new GitHub repository
2. Upload the `legal` folder
3. Go to Settings > Pages
4. Enable GitHub Pages
5. Your URLs will be:
   - `https://[username].github.io/[repo-name]/legal/terms-of-service.html`
   - `https://[username].github.io/[repo-name]/legal/privacy-policy.html`
