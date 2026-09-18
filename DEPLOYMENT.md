# 🚀 Vercel Deployment Guide

Complete step-by-step guide to deploy Olympiad Quest to Vercel.

## 📋 Prerequisites

1. **GitHub Account** - [Sign up](https://github.com/signup)
2. **Vercel Account** - [Sign up with GitHub](https://vercel.com/signup)
3. **Node.js 18+** - [Download](https://nodejs.org/)
4. **Git** - [Download](https://git-scm.com/)
5. **Gemini API Key** - [Get free key](https://aistudio.google.com/app/apikey)

---

## 🎯 Method 1: Deploy via Vercel Dashboard (Easiest)

### Step 1: Push to GitHub

```bash
# Initialize git repository (if not already done)
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit: Olympiad Quest v3.0"

# Create GitHub repository
# Go to https://github.com/new
# Create new repo named "olympiad-quest"

# Add remote and push
git remote add origin https://github.com/YOUR_USERNAME/olympiad-quest.git
git branch -M main
git push -u origin main
```

### Step 2: Import to Vercel

1. Go to [vercel.com/new](https://vercel.com/new)
2. Click "Import Git Repository"
3. Select your `olympiad-quest` repository
4. Vercel auto-detects Vite framework
5. Click "Deploy"
6. Wait ~2 minutes for build
7. ✅ Your app is live!

### Step 3: Access Your App

- **URL**: `https://olympiad-quest.vercel.app` (or your chosen name)
- **Dashboard**: [vercel.com/dashboard](https://vercel.com/dashboard)

---

## 🎯 Method 2: Deploy via Vercel CLI

### Step 1: Install Vercel CLI

```bash
npm install -g vercel
```

### Step 2: Login to Vercel

```bash
vercel login
# Follow browser authentication
```

### Step 3: Deploy

```bash
# Navigate to project
cd olympiad-quest

# Deploy to preview
vercel

# Answer prompts:
# ? Set up and deploy? → Y
# ? Which scope? → (select your account)
# ? Link to existing project? → N
# ? What's your project's name? → olympiad-quest
# ? In which directory is your code located? → ./
# ? Want to override the settings? → N

# Deploy to production
vercel --prod
```

### Step 4: Get Live URL

```bash
vercel ls
# Shows your deployed URLs
```

---

## 🎯 Method 3: Deploy from Local Directory (No GitHub)

### Step 1: Prepare Project

```bash
# Install dependencies
npm install

# Test build locally
npm run build

# Verify dist/ folder exists
ls dist/
```

### Step 2: Deploy with Vercel CLI

```bash
# Install Vercel CLI
npm install -g vercel

# Login
vercel login

# Deploy
vercel --prod

# Follow prompts (same as Method 2)
```

---

## 🔧 Post-Deployment Configuration

### Custom Domain

1. Go to [Vercel Dashboard](https://vercel.com/dashboard)
2. Select your project
3. Click "Settings" → "Domains"
4. Add your domain (e.g., `olympiadquest.com`)
5. Follow DNS instructions:
   - Add A record: `76.76.21.21`
   - Or CNAME: `cname.vercel-dns.com`

### Environment Variables (Not Required)

This app doesn't need environment variables! Users enter their Gemini API key directly in the app's Settings page.

### Analytics (Optional)

```bash
# Enable Vercel Analytics
vercel analytics enable
```

---

## 📱 Testing Your Deployment

### 1. Test Core Features

- [ ] Open the app URL
- [ ] Navigate to Settings
- [ ] Enter Gemini API key
- [ ] Go to Topics → Select a topic
- [ ] Verify questions generate successfully
- [ ] Try Daily Challenge
- [ ] Test AI Study Buddy
- [ ] Check Analytics dashboard

### 2. Test on Mobile

- [ ] Open on mobile device
- [ ] Test bottom navigation
- [ ] Verify responsive design
- [ ] Test quiz interactions

### 3. Test Performance

- [ ] Check page load speed (< 2 seconds)
- [ ] Verify smooth animations
- [ ] Test offline behavior

---

## 🔄 Updating Your Deployment

### Automatic Updates (GitHub)

Every push to `main` branch auto-deploys:

```bash
# Make changes
git add .
git commit -m "Update features"
git push origin main
# Vercel auto-deploys!
```

### Manual Updates (CLI)

```bash
# Deploy to preview
vercel

# Deploy to production
vercel --prod
```

---

## 🐛 Troubleshooting Deployment

### Build Fails

**Error**: `Module not found`
```bash
# Clear cache and reinstall
rm -rf node_modules package-lock.json
npm install
npm run build
```

**Error**: `TypeScript errors`
```bash
# Check TypeScript
npm run typecheck

# Fix errors and rebuild
npm run build
```

### 404 on Page Refresh

This shouldn't happen with our `vercel.json` configuration. If it does:

1. Check `vercel.json` exists in root
2. Verify rewrites are configured
3. Redeploy: `vercel --prod`

### API Calls Fail

**Issue**: Gemini API errors in production

**Solutions**:
1. Verify API key is correct in Settings
2. Check browser console for CORS errors
3. Try different API mode (SDK → Interactions → Direct)
4. Verify API key has no restrictions

### Slow Performance

**Issue**: App loads slowly

**Solutions**:
1. Enable Vercel Edge Network (automatic)
2. Check bundle size: `npm run build`
3. Optimize images (if any added)
4. Enable compression (automatic on Vercel)

---

## 📊 Monitoring

### Vercel Analytics

1. Go to Dashboard → Your Project → Analytics
2. View:
   - Page views
   - Performance metrics
   - Web Vitals
   - Geographic distribution

### Deployment Logs

1. Dashboard → Deployments
2. Click on any deployment
3. View build logs or function logs

---

## 🔒 Security Best Practices

### API Key Security

- ✅ Keys stored in browser localStorage only
- ✅ Never sent to your server
- ✅ Users can clear keys anytime
- ✅ No server-side storage

### Content Security

- ✅ All content AI-generated
- ✅ No user-uploaded content
- ✅ No database required
- ✅ Stateless architecture

---

## 💰 Cost Analysis

### Vercel Free Tier

- ✅ Unlimited deployments
- ✅ Unlimited bandwidth
- ✅ Automatic HTTPS
- ✅ Global CDN
- ✅ Serverless functions (100GB-hours/month)
- ✅ Perfect for this app!

### Gemini API Free Tier

- ✅ 15 RPM (requests per minute)
- ✅ 1 million tokens per minute
- ✅ More than enough for personal use
- ✅ Paid tier available for high volume

### Total Cost: $0/month

This app runs completely free on Vercel + Gemini free tiers!

---

## 🎓 Advanced Configuration

### Preview Deployments

Every PR gets a preview URL:

```bash
# Create feature branch
git checkout -b new-feature

# Make changes and push
git push origin new-feature

# Create PR on GitHub
# Vercel auto-creates preview URL
```

### Branch Protection

1. GitHub → Settings → Branches
2. Add rule for `main` branch
3. Require pull request reviews
4. Require status checks

### Custom Build Settings

Edit `vercel.json`:

```json
{
  "buildCommand": "npm run build",
  "outputDirectory": "dist",
  "framework": "vite"
}
```

---

## 📞 Support

### Vercel Support

- [Documentation](https://vercel.com/docs)
- [Community](https://github.com/vercel/vercel/discussions)
- [Status](https://www.vercel-status.com/)

### App Support

- Check README.md troubleshooting section
- Review Settings page for API configuration
- Verify Gemini API key validity

---

## ✅ Deployment Checklist

Before going live:

- [ ] Test all features locally
- [ ] Build succeeds without errors
- [ ] Push to GitHub
- [ ] Deploy to Vercel
- [ ] Test production URL
- [ ] Verify mobile responsiveness
- [ ] Test Gemini API integration
- [ ] Check all pages load correctly
- [ ] Verify analytics (if enabled)
- [ ] Set up custom domain (optional)
- [ ] Share with users! 🎉

---

## 🎉 You're Live!

Your Olympiad Quest app is now deployed and ready for students worldwide!

**Share your app**: `https://your-app.vercel.app`

**Next steps**:
1. Share with students/teachers
2. Collect feedback
3. Iterate and improve
4. Deploy updates regularly

---

**Happy Deploying! 🚀**
