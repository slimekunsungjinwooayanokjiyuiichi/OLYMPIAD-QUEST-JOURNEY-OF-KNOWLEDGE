# 🏆 Olympiad Quest - Quick Start Guide

## ✅ What You Have

A **production-ready**, AI-powered Olympiad preparation app with:

- 📚 **44 Topics** (IMO & ISO for Standards 4 & 7)
- 🤖 **AI Question Generation** (Google Gemini 3.5/3.6/3.7/3.8 Flash)
- 🎯 **Daily Challenges** (auto-refresh every 24 hours)
- 📝 **Exam System** (topic exams, mock tests, mega tests)
- 🎮 **Gamification** (50 levels, 11 chapters, 50+ achievements)
- 🧠 **AI Tutor** (chat-based doubt solving)
- 📊 **Analytics** (brain regions, IQ/EQ scores, progress tracking)
- 📱 **Mobile-Responsive** (works on all devices)
- 🔌 **Multi-API Support** (SDK, Interactions API, Direct REST)
- 🔑 **Dual Key Format** (AQ new + AIza legacy)

## 🚀 Deploy to Vercel in 3 Steps

### 1. Push to GitHub

```bash
git init
git add .
git commit -m "Olympiad Quest v3.0 - Production Ready"
git remote add origin https://github.com/YOUR_USERNAME/olympiad-quest.git
git push -u origin main
```

### 2. Import to Vercel

1. Go to [vercel.com/new](https://vercel.com/new)
2. Import your GitHub repository
3. Click "Deploy"
4. Wait ~2 minutes

### 3. Done! 🎉

Your app is live at `https://olympiad-quest.vercel.app`

---

## 🔑 First-Time Setup

1. Open your deployed app
2. Go to **Settings** (⚙️ icon)
3. Get free API key from [Google AI Studio](https://aistudio.google.com/app/apikey)
4. Paste key (starts with `AIza` or `AQ`)
5. Click "Validate & Save"
6. Start practicing! 🎯

---

## 📱 Test Your Deployment

### Core Features to Test

- [ ] **Settings**: API key validation works
- [ ] **Topics**: Questions generate successfully
- [ ] **Daily Challenge**: 20 mixed questions load
- [ ] **Quiz**: Answer questions, see explanations
- [ ] **AI Tutor**: Chat with AI study buddy
- [ ] **Analytics**: View progress and brain scores
- [ ] **Journey**: Check level, chapters, achievements
- [ ] **Mobile**: Test on phone, bottom nav works

### Quick Test Commands

```bash
# Test locally first
npm install
npm run dev
# Open http://localhost:5173

# Test production build
npm run build
npm run preview
# Open http://localhost:4173
```

---

## 🎯 Key Features

### AI Question Generation
- **25-50 questions per topic** (on-demand)
- **Daily auto-refresh** (new questions every 24h)
- **4 difficulty levels** (Easy, Medium, Hard, Expert)
- **Detailed explanations** for every answer
- **Zero static content** (all AI-generated)

### Testing System
- **Daily Challenge**: 20 questions, 30 min timer
- **Topic Exams**: 30 questions per topic
- **Mock Tests**: Full-length practice
- **Mega Tests**: Olympiad-level difficulty
- **Progressive Difficulty**: Unlock harder levels

### Gamification
- **50 Levels**: Novice → Champion
- **11 Story Chapters**: Anime-style journey
- **XP System**: +10 per correct answer
- **Achievements**: 50+ unlockable badges
- **Streak Counter**: Daily practice rewards
- **Leaderboard**: Compete with others

### Analytics
- **Brain Regions**: Track 10 areas of activation
- **IQ/EQ Scores**: Calculated from performance
- **Topic Mastery**: See strong/weak areas
- **Time Tracking**: Monitor study habits
- **AI Reports**: Daily personalized insights

---

## 🔧 Configuration

### API Settings (In App)

**Model Selection**:
- Gemini 3.5 Flash (Default, recommended)
- Gemini 3.6 Flash
- Gemini 3.7 Flash
- Gemini 3.8 Flash (Most intelligent)

**API Mode**:
- SDK (Default, with fallbacks)
- Interactions API (New /v1beta/interactions)
- Direct REST API (Traditional endpoint)

**API Key Formats**:
- ✅ AQ (New authentication key)
- ✅ AIza (Legacy traffic key)

---

## 📊 Build Stats

```
dist/index.html                    3.47 kB │ gzip: 1.43 kB
dist/assets/index-*.css           28.87 kB │ gzip: 6.23 kB
dist/assets/index-*.js           249.26 kB │ gzip: 73.44 kB
dist/assets/confetti-*.js         10.70 kB │ gzip: 4.29 kB

Total: ~292 KB (gzipped: ~85 KB)
```

**Performance**:
- First load: < 2 seconds
- Question generation: 5-15 seconds
- Offline support: Questions cached locally

---

## 🐛 Common Issues

### "API Key Required" Warning
→ Go to Settings → Add Gemini API key

### "Failed to generate questions"
→ Check internet connection
→ Verify API key is correct
→ Try different API mode in Settings

### Questions Not Refreshing
→ Click "Refresh Questions" button
→ Questions auto-refresh every 24 hours

### Build Errors
```bash
rm -rf node_modules package-lock.json
npm install
npm run build
```

---

## 📚 Documentation

- **README.md** - Complete feature documentation
- **DEPLOYMENT.md** - Detailed deployment guide
- **vercel.json** - Vercel configuration
- **public/manifest.json** - PWA configuration

---

## 💰 Cost

**$0/month** - Completely free!

- Vercel Free Tier: Unlimited deployments
- Gemini API Free Tier: 15 RPM, 1M tokens/min
- No backend required
- No database costs

---

## 🎓 For Students

1. **Start Daily**: Complete Daily Challenge every day
2. **Track Progress**: Check Analytics weekly
3. **Ask AI**: Use AI Tutor for difficult concepts
4. **Build Streaks**: Consistency unlocks achievements
5. **Review Weak Areas**: Focus on topics below 70%

---

## 🎯 For Parents/Teachers

1. **Monitor Progress**: Analytics dashboard shows performance
2. **Set Goals**: Use Journey page for chapter targets
3. **Review Weak Areas**: Analytics highlights topics needing attention
4. **Encourage Consistency**: Daily streaks build habits
5. **Celebrate Achievements**: Unlock badges motivate students

---

## 🔒 Privacy & Security

- ✅ **Client-side only**: All processing in browser
- ✅ **No backend**: Direct API calls to Google
- ✅ **LocalStorage**: Data stored locally (clearable)
- ✅ **API key protection**: Keys never leave browser
- ✅ **No analytics**: Zero tracking or data collection
- ✅ **No accounts**: No user registration required

---

## 📱 Browser Support

- ✅ Chrome/Edge 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

---

## 🚀 Next Steps

1. **Deploy to Vercel** (see instructions above)
2. **Test all features** (use checklist)
3. **Share with students** (send URL)
4. **Collect feedback** (iterate and improve)
5. **Deploy updates** (git push auto-deploys)

---

## 📞 Support

**Deployment Issues**: See DEPLOYMENT.md
**App Issues**: Check README.md troubleshooting
**API Issues**: Verify key in Settings, try different mode

---

## 🎉 You're Ready!

Your Olympiad Quest app is **production-ready** and ready to deploy!

**Quick Deploy**:
```bash
git push origin main
# Import to Vercel
# Done! 🚀
```

**Good luck with your Olympiad preparation! 🏆**

---

*Version 3.0 | Built with React + Vite + Tailwind + Gemini AI*
