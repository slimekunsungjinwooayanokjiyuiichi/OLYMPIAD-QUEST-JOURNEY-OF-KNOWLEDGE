# 🚀 DEPLOYMENT CHECKLIST - Run These Commands

## ✅ STEP 1: Initialize Git Repository

Open your terminal and run these commands one by one:

```bash
# Navigate to your project folder
cd /path/to/olympiad-quest

# Initialize git
git init

# Add all files
git add .

# First commit
git commit -m "🏆 Olympiad Quest v3.0 - AI-Powered IMO & ISO Prep"
```

## ✅ STEP 2: Create GitHub Repository

1. Go to **https://github.com/new**
2. Repository name: `olympiad-quest`
3. Description: `AI-Powered Olympiad Preparation App for IMO & ISO`
4. Make it **Public** (or Private if preferred)
5. **DO NOT** initialize with README (we already have one)
6. Click **Create repository**

## ✅ STEP 3: Push to GitHub

```bash
# Add GitHub as remote (replace YOUR_USERNAME)
git remote add origin https://github.com/YOUR_USERNAME/olympiad-quest.git

# Rename branch to main
git branch -M main

# Push to GitHub
git push -u origin main
```

## ✅ STEP 4: Deploy to Vercel

### Method A: Via Vercel Dashboard (Easiest)

1. Go to **https://vercel.com/new**
2. Click **"Import Git Repository"**
3. Select your `olympiad-quest` repository
4. Framework Preset: **Vite** (auto-detected)
5. Click **"Deploy"**
6. Wait 2-3 minutes
7. ✅ **DONE!** Your app is live!

### Method B: Via Vercel CLI

```bash
# Install Vercel CLI
npm install -g vercel

# Login
vercel login

# Deploy
vercel --prod
```

## ✅ STEP 5: Get Your Live URL

After deployment, Vercel gives you a URL like:
- `https://olympiad-quest.vercel.app`
- `https://olympiad-quest-[random].vercel.app`

**Copy this URL** - you'll need it for domain setup!

## ✅ STEP 6: Test Your Deployment

Open your live URL and test:
- [ ] Homepage loads
- [ ] Settings page works
- [ ] Topics page shows all 44 topics
- [ ] Enter Gemini API key
- [ ] Generate questions for a topic
- [ ] Take a quiz
- [ ] Check analytics
- [ ] Test on mobile

---

## 🌐 CUSTOM DOMAIN SETUP

### Option 1: Free Subdomain (Already Done!)

Your Vercel URL `olympiad-quest.vercel.app` is already a working domain!

### Option 2: Buy Custom Domain

**Recommended Domain Registrars:**
- **Namecheap** - https://www.namecheap.com (~$10/year)
- **GoDaddy** - https://www.godaddy.com (~$12/year)
- **Google Domains** - https://domains.google (~$12/year)
- **Cloudflare** - https://www.cloudflare.com (~$10/year, best value)

**Suggested Domain Names:**
- `olympiadquest.com`
- `olympiad-quest.com`
- `olympiadprep.com`
- `questolympiad.com`
- `imo-iso-prep.com`

### Option 3: Connect Custom Domain to Vercel

After buying your domain:

1. Go to **Vercel Dashboard** → Your Project → **Settings** → **Domains**
2. Enter your domain (e.g., `olympiadquest.com`)
3. Click **Add**
4. Vercel shows DNS instructions:

#### For Apex Domain (olympiadquest.com):
```
Type: A
Name: @
Value: 76.76.21.21
```

#### For WWW Subdomain (www.olympiadquest.com):
```
Type: CNAME
Name: www
Value: cname.vercel-dns.com
```

5. Go to your domain registrar's DNS settings
6. Add the records above
7. Wait 5-30 minutes for DNS propagation
8. ✅ Your custom domain is live!

### Option 4: Free Domain Options

**Freenom** (free .tk, .ml, .ga domains):
- Go to https://www.freenom.com
- Search for free domain
- Register (free for 1 year)
- Connect to Vercel same way as paid domain

**GitHub Pages** (free .github.io subdomain):
```bash
# Install gh-pages
npm install -D gh-pages

# Add to package.json:
"scripts": {
  "deploy": "gh-pages -d dist"
}

# Deploy
npm run deploy
```
Your app will be at: `https://YOUR_USERNAME.github.io/olympiad-quest/`

---

## 🔑 AFTER DEPLOYMENT: Configure App

1. Open your live URL
2. Click **Settings** (⚙️ icon)
3. Get Gemini API key:
   - Go to https://aistudio.google.com/app/apikey
   - Sign in with Google
   - Click "Create API Key"
   - Copy the key (starts with `AIza` or `AQ`)
4. Paste key in Settings → Validate & Save
5. ✅ Start using the app!

---

## 📊 DEPLOYMENT STATUS

After deploying, check:
- ✅ Build size: ~85KB gzipped
- ✅ Load time: < 2 seconds
- ✅ Mobile responsive: Yes
- ✅ PWA installable: Yes
- ✅ SEO optimized: Yes
- ✅ HTTPS: Automatic (Vercel)
- ✅ CDN: Global (Vercel)
- ✅ Cost: $0/month

---

## 🔄 UPDATES

Every time you push to GitHub, Vercel auto-deploys:

```bash
# Make changes
git add .
git commit -m "Update: added new feature"
git push origin main

# Vercel auto-deploys in ~2 minutes!
```

---

## 🆘 TROUBLESHOOTING

### Build Failed on Vercel
```bash
# Test locally first
npm run build

# If it works locally, check Vercel logs
```

### 404 on Page Refresh
- Already fixed in vercel.json
- If still happening, redeploy

### API Key Not Working
- Verify key starts with `AIza` or `AQ`
- Check key is not expired
- Try different API mode in Settings

### Domain Not Working
- Wait 30 minutes for DNS propagation
- Check DNS records are correct
- Clear browser cache

---

## 📞 NEED HELP?

- **Vercel Docs**: https://vercel.com/docs
- **Vercel Support**: https://vercel.com/support
- **Gemini API**: https://ai.google.dev/docs

---

## ✅ FINAL CHECKLIST

Before going live:
- [ ] Code pushed to GitHub
- [ ] Deployed to Vercel
- [ ] Live URL works
- [ ] Tested on desktop
- [ ] Tested on mobile
- [ ] Gemini API key configured
- [ ] All features working
- [ ] Custom domain set up (optional)
- [ ] Shared with users!

---

**🎉 CONGRATULATIONS! Your Olympiad Quest app is LIVE!**

Share your URL: `https://your-app.vercel.app`

Good luck with your Olympiad preparation! 🏆
