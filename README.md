# Legal Documents

This folder contains the Terms of Service and Privacy Policy documents required for TikTok Developer Portal registration.

## Files

- `terms-of-service.html` - Terms of Service document
- `privacy-policy.html` - Privacy Policy document

## Hosting Options

You need to host these files publicly so TikTok can verify them. Here are some options:

### GitHub Pages (Recommended - Free)

1. Create a GitHub repository
2. Upload these HTML files to a `legal/` folder
3. Enable GitHub Pages in Settings > Pages
4. Your URLs will be:
   - `https://yourusername.github.io/repo-name/legal/terms-of-service.html`
   - `https://yourusername.github.io/repo-name/legal/privacy-policy.html`

### Netlify Drop (Quick & Easy)

**Important:** When using Netlify Drop, you need to drag the **entire `legal/` folder**, not individual files.

1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. **Drag and drop the entire `legal/` folder** (make sure it contains all HTML files)
3. Wait for deployment (usually 10-30 seconds)
4. Your URLs will be:
   - `https://[random-name].netlify.app/legal/terms-of-service.html`
   - `https://[random-name].netlify.app/legal/privacy-policy.html`
   
   **Note:** Replace `[random-name]` with the actual site name Netlify gives you.
   
5. **Test the URLs** - Click on them to make sure they work before using in TikTok Developer Portal

**Troubleshooting:**
- If you get 404, make sure you dragged the **folder**, not individual files
- Wait a minute for Netlify to finish deploying
- Check that the URL includes `/legal/` in the path
- Try refreshing the page

### Your Own Web Server

Upload these files to your web server and use your domain URLs.

## Usage

When registering your TikTok app, you'll be asked for:
- **Terms of Service URL**: Use the URL to `terms-of-service.html`
- **Privacy Policy URL**: Use the URL to `privacy-policy.html`

Make sure these URLs are publicly accessible before submitting your app registration.
