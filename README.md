# 🏆 Olympiad Quest

**AI-Powered Olympiad Preparation App for IMO & ISO (Standards 4 & 7)**

A comprehensive, production-ready web application that uses Google Gemini AI to generate unlimited practice questions for International Mathematics Olympiad (IMO) and International Science Olympiad (ISO) preparation.

## 🌟 Features

### 📚 Complete Topic Coverage
- **44 Topics** across IMO & ISO for Standards 4 & 7
- **IMO Standard 4**: 10 topics (Number Sense, Fractions, Geometry, etc.)
- **IMO Standard 7**: 12 topics (Integers, Algebra, Triangles, etc.)
- **ISO Standard 4**: 10 topics (Plants, Animals, Human Body, etc.)
- **ISO Standard 7**: 12 topics (Nutrition, Heat, Acids, Light, etc.)

### 🤖 AI-Powered Question Generation
- **Dynamic Question Generation**: AI creates 25-50 unique questions per topic
- **Daily Auto-Refresh**: New questions generated every 24 hours
- **Multiple Difficulty Levels**: Easy, Medium, Hard, Expert
- **Detailed Explanations**: Step-by-step solutions for every question
- **Zero Static Content**: All questions are AI-generated on-demand

### 🎯 Comprehensive Testing System
- **Daily Challenge**: 20 mixed questions, auto-refreshes daily
- **Topic Exams**: 30 questions per topic, refreshes every 10 days
- **Mock Tests**: Full-length practice tests
- **Mega Tests**: Olympiad-level difficulty simulations
- **Progressive Difficulty**: Unlock harder levels as you improve

### 🎮 Gamification & Progression
- **50 Levels**: Progress from Novice Learner to Olympiad Champion
- **11 Story Chapters**: Anime-style journey with XP-based unlocks
- **50+ Achievements**: Unlock badges for milestones
- **Brain Awakening System**: Track 10 brain regions activation
- **Leaderboard**: Compete with other students
- **Streak System**: Daily practice rewards

### 🧠 Advanced AI Features
- **AI Study Buddy**: Chat with AI tutor for doubts and explanations
- **Smart Analytics**: Track accuracy, time spent, weak areas
- **AI Daily Report**: Personalized learning insights
- **Adaptive Difficulty**: Questions adjust based on performance
- **Bookmarking**: Save difficult questions for review

### 🎨 Modern UI/UX
- **Anime-Themed Design**: Purple/blue gradients, neon effects
- **Glassmorphism Cards**: Modern, clean interface
- **Mobile-Responsive**: Works perfectly on all devices
- **Smooth Animations**: Confetti celebrations, floating elements
- **Dark Mode**: Easy on the eyes for long study sessions

## 🚀 Deployment Guide

### Prerequisites
- Node.js 18+ installed
- Google Gemini API key (free from [Google AI Studio](https://aistudio.google.com/app/apikey))

### Option 1: Deploy to Vercel (Recommended)

#### Step 1: Prepare Your Project
```bash
# Clone or download this project
cd olympiad-quest

# Install dependencies
npm install

# Test locally
npm run dev
```

#### Step 2: Deploy to Vercel

**Method A: Using Vercel CLI**
```bash
# Install Vercel CLI
npm install -g vercel

# Login to Vercel
vercel login

# Deploy
vercel

# Follow the prompts:
# - Set up and deploy? Y
# - Which scope? (select your account)
# - Link to existing project? N
# - Project name? olympiad-quest
# - Directory? ./
# - Override settings? N

# Deploy to production
vercel --prod
```

**Method B: Using Vercel Dashboard**
1. Go to [vercel.com](https://vercel.com)
2. Sign up/Login with GitHub
3. Click "Add New Project"
4. Import your GitHub repository
5. Vercel auto-detects Vite configuration
6. Click "Deploy"
7. Wait for build to complete (~2 minutes)
8. Your app is live! 🎉

#### Step 3: Configure Custom Domain (Optional)
1. Go to your Vercel project dashboard
2. Click "Settings" → "Domains"
3. Add your custom domain
4. Follow DNS configuration instructions

### Option 2: Deploy to Netlify

```bash
# Install Netlify CLI
npm install -g netlify-cli

# Build the project
npm run build

# Deploy
netlify deploy --prod --dir=dist
```

Or use Netlify's drag-and-drop:
1. Go to [netlify.com](https://netlify.com)
2. Drag the `dist` folder to the deploy area
3. Done!

### Option 3: Deploy to GitHub Pages

```bash
# Install gh-pages
npm install -D gh-pages

# Add to package.json scripts:
# "deploy": "npm run build && gh-pages -d dist"

# Deploy
npm run deploy
```

## 🔑 Getting Your Gemini API Key

1. Go to [Google AI Studio](https://aistudio.google.com/app/apikey)
2. Sign in with your Google account
3. Click "Create API Key"
4. Copy the key (starts with `AIza` or `AQ`)
5. Paste it in the app's Settings page

**Note**: The API key is stored in your browser's localStorage and never sent to any server except Google's API.

## 🛠️ Technical Stack

- **Frontend**: React 18 + TypeScript
- **Build Tool**: Vite
- **Styling**: Tailwind CSS
- **AI Integration**: Google Gemini API (3.5/3.6/3.7/3.8 Flash models)
- **State Management**: React Context + useReducer
- **Animations**: Framer Motion + CSS
- **Icons**: Lucide React + Font Awesome
- **Charts**: Recharts
- **Routing**: React Router DOM

## 📱 API Compatibility

The app supports multiple Gemini API formats:

### API Key Formats
- ✅ **AQ** (New Authentication Key) - Recommended
- ✅ **AIza** (Legacy Traffic Key) - Still supported

### API Models
- ✅ Gemini 3.5 Flash (Default, best balance)
- ✅ Gemini 3.6 Flash
- ✅ Gemini 3.7 Flash
- ✅ Gemini 3.8 Flash (Most intelligent)
- ✅ Gemini 2.5 Flash (Legacy)

### API Endpoints
- ✅ **Interactions API** (`/v1beta/interactions`) - New primary endpoint
- ✅ **Generate Content** (`/v1beta/models/:model:generateContent`) - Traditional
- ✅ **SDK Mode** - Uses @google/generative-ai with automatic fallbacks

## 🔒 Security & Privacy

- **Client-Side Only**: All processing happens in the browser
- **No Backend Required**: Direct API calls to Google
- **LocalStorage**: User data stored locally (clearable via Settings)
- **API Key Protection**: Keys never leave the browser
- **No Analytics**: Zero tracking or data collection

## 📊 Performance

- **Build Size**: ~250KB (gzipped: ~73KB)
- **First Load**: < 2 seconds on 4G
- **Question Generation**: 5-15 seconds per topic (depends on AI response)
- **Offline Support**: Questions cached in localStorage

## 🎯 Usage Tips

### For Students
1. **Start with Settings**: Add your Gemini API key first
2. **Daily Practice**: Complete the Daily Challenge every day
3. **Track Progress**: Check Analytics to see improvement
4. **Ask AI**: Use the AI Tutor for difficult concepts
5. **Build Streaks**: Consistent practice unlocks achievements

### For Parents/Teachers
1. **Monitor Progress**: Check the Analytics dashboard
2. **Set Goals**: Use the Journey page to track chapter completion
3. **Review Weak Areas**: Analytics shows topics needing attention
4. **Encourage Consistency**: Daily streaks build habits

## 🐛 Troubleshooting

### "API Key Required" Warning
- Go to Settings → Add your Gemini API key
- Key must start with `AIza` or `AQ`
- Get a free key from [Google AI Studio](https://aistudio.google.com/app/apikey)

### "Failed to generate questions"
- Check your internet connection
- Verify API key is correct in Settings
- Try switching API mode (SDK → Interactions → Direct)
- Try a different model (3.5 Flash → 3.8 Flash)

### Questions Not Refreshing
- Questions refresh every 24 hours automatically
- Click "Refresh Questions" button to force refresh
- Clear browser cache if issues persist

### Build Errors
```bash
# Clear node_modules and reinstall
rm -rf node_modules package-lock.json
npm install

# Clear build cache
rm -rf dist
npm run build
```

## 📝 Configuration

### Environment Variables (Optional)
No environment variables required! The app uses client-side configuration only.

### Vercel Configuration
The included `vercel.json` handles:
- SPA routing (all routes → index.html)
- Asset caching (1 year for /assets/*)
- Build optimization

## 🎓 Educational Value

### Aligned with Olympiad Syllabus
- **IMO**: International Mathematics Olympiad curriculum
- **ISO**: International Science Olympiad curriculum
- **Standards 4 & 7**: Age-appropriate content for 9-13 year olds

### Learning Methodology
- **Spaced Repetition**: Questions refresh to prevent memorization
- **Adaptive Difficulty**: AI adjusts to student level
- **Immediate Feedback**: Detailed explanations for every answer
- **Progress Tracking**: Visual progress bars and analytics
- **Gamification**: XP, levels, and achievements motivate practice

## 🤝 Contributing

This is a production-ready application. To customize:

```bash
# Development
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## 📄 License

This project is created for educational purposes.

## 🙏 Acknowledgments

- **Google Gemini AI**: For powerful question generation
- **React & Vite**: For modern web development
- **Tailwind CSS**: For beautiful, responsive design
- **Olympiad Community**: For curriculum guidance

## 📞 Support

For issues or questions:
1. Check the Troubleshooting section above
2. Review the Settings page for API configuration
3. Verify your Gemini API key is valid
4. Try different API modes in Settings

---

**Built with ❤️ for Olympiad aspirants**

*Version 3.0 | Last Updated: 2026*
