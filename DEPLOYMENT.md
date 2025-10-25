# Deployment Guide: Velutan Battle Map

This guide will walk you through deploying your battle tracker to **velutanbattlemap.com** using GitHub Pages (the cheapest option at ~$1/year).

## 📋 Prerequisites

- ✅ GitHub repository created: https://github.com/ardaaboz/rpg-battle-tracker
- ✅ Code pushed to GitHub (main branch)
- ⏳ Domain name to purchase: velutanbattlemap.com ($1/year at IONOS)

## 🌐 Step 1: Purchase Domain at IONOS

1. Go to https://www.ionos.com/
2. Search for "velutanbattlemap.com"
3. Purchase the domain (should be ~$1 for first year)
4. **Don't buy hosting** - we'll use GitHub Pages for free!

## 🚀 Step 2: Enable GitHub Pages

1. Go to your repository: https://github.com/ardaaboz/rpg-battle-tracker
2. Click **Settings** tab
3. Scroll down to **Pages** section (left sidebar)
4. Under **Source**, select:
   - Branch: `main`
   - Folder: `/ (root)`
5. Click **Save**
6. Wait 2-3 minutes for deployment
7. Your site will be live at: `https://ardaaboz.github.io/rpg-battle-tracker/`

## 🔗 Step 3: Configure Custom Domain

### In GitHub:

1. Still in **Settings → Pages**
2. Under **Custom domain**, enter: `velutanbattlemap.com`
3. Click **Save**
4. Check **Enforce HTTPS** (wait a few minutes if it's grayed out)

### In IONOS DNS Settings:

1. Log into your IONOS account
2. Go to **Domains & SSL**
3. Click on **velutanbattlemap.com**
4. Go to **DNS Settings**
5. Add these records:

**For the root domain (velutanbattlemap.com):**
```
Type: A
Name: @
Value: 185.199.108.153
TTL: 3600

Type: A
Name: @
Value: 185.199.109.153
TTL: 3600

Type: A
Name: @
Value: 185.199.110.153
TTL: 3600

Type: A
Name: @
Value: 185.199.111.153
TTL: 3600
```

**For www subdomain:**
```
Type: CNAME
Name: www
Value: ardaaboz.github.io
TTL: 3600
```

6. Save changes
7. Wait 15-60 minutes for DNS propagation

## ✅ Step 4: Verify Deployment

1. Visit https://velutanbattlemap.com
2. Check that:
   - Site loads correctly
   - HTTPS is working (green padlock)
   - All images and CSS load
   - All functionality works

## 🔄 Updating Your Site

Whenever you make changes:

1. Make your changes locally
2. Commit and push to GitHub:
   ```bash
   git add .
   git commit -m "Description of changes"
   git push
   ```
3. GitHub Pages automatically rebuilds in 1-2 minutes
4. Your site updates automatically!

## 💰 Cost Breakdown

| Service | Cost |
|---------|------|
| Domain (velutanbattlemap.com) | ~$1/year |
| GitHub Pages Hosting | FREE |
| SSL Certificate | FREE |
| Bandwidth | FREE (unlimited) |
| **TOTAL** | **~$1/year** |

## 🎯 Alternative: Cloudflare Pages (Optional)

If you want faster global performance:

1. Sign up at https://pages.cloudflare.com/
2. Connect your GitHub repository
3. Deploy with one click
4. Configure DNS (Cloudflare provides better CDN)
5. Still FREE + your $1 domain

**Benefits:**
- Faster worldwide (better CDN)
- Better analytics
- More deployment options

## 🐛 Troubleshooting

### Site not loading after DNS setup
- **Wait longer**: DNS can take up to 24 hours (usually 15-60 minutes)
- Check DNS propagation: https://www.whatsmydns.net/
- Clear browser cache (Ctrl+F5)

### HTTPS not working
- Wait 10-15 minutes after enabling in GitHub
- Make sure "Enforce HTTPS" is checked
- DNS must be fully propagated first

### Images not loading
- Check that image paths are relative (not absolute)
- Verify images are in the repository
- Check browser console for errors

### Custom domain shows 404
- Make sure you added both A records and CNAME
- Verify GitHub Pages is set to "main" branch, root folder
- Check that custom domain is saved in GitHub settings

## 📧 Need Help?

- **GitHub Pages Docs**: https://docs.github.com/en/pages
- **IONOS Support**: https://www.ionos.com/help
- **Repository Issues**: https://github.com/ardaaboz/rpg-battle-tracker/issues

## 🎉 You're Done!

Your battle tracker is now live at **velutanbattlemap.com** for just $1/year!

Share it with your gaming group and enjoy!

---

### Quick Reference Commands

```bash
# Clone repository
git clone https://github.com/ardaaboz/rpg-battle-tracker.git

# Make changes
cd rpg-battle-tracker
# Edit files...

# Push updates
git add .
git commit -m "Update description"
git push

# Site updates automatically in 1-2 minutes!
```
