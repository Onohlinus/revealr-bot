# Free Deployment Guide for Anonymous Confessions Platform

This guide shows you how to deploy your confession platform to free hosting services.

## Option 1: Vercel (Recommended)

### Step 1: Prepare for Vercel
1. Download all your project files
2. Upload to GitHub (create a new repository)
3. Sign up at [vercel.com](https://vercel.com) with your GitHub account

### Step 2: Deploy
1. Click "New Project" in Vercel dashboard
2. Import your GitHub repository
3. Vercel will automatically detect it's a Node.js project
4. Click "Deploy"

**Build Settings:**
- Build Command: `npm run build`
- Output Directory: `dist`
- Install Command: `npm install`

## Option 2: Render

### Step 1: Setup
1. Sign up at [render.com](https://render.com)
2. Connect your GitHub repository
3. Create a new "Web Service"

### Step 2: Configuration
- **Build Command:** `npm install && npm run build`
- **Start Command:** `npm start`
- **Environment:** Node.js
- **Plan:** Free

## Option 3: Railway

### Step 1: Setup
1. Sign up at [railway.app](https://railway.app)
2. Connect GitHub repository
3. Deploy from repo

### Step 2: Configuration
- **Start Command:** `npm start`
- **Build Command:** `npm run build`

## Important Notes

### Environment Variables
For Telegram bot functionality, add this environment variable to your hosting platform:
- `TELEGRAM_BOT_TOKEN=your_bot_token_here`

### Free Tier Limitations
- **Vercel:** Great for this project, handles both frontend and backend
- **Render:** 750 hours/month free, perfect for personal projects  
- **Railway:** $5 credit monthly, good performance

### File Structure for Export
Make sure you have these files:
```
├── client/          # React frontend
├── server/          # Express backend  
├── shared/          # Shared schemas
├── package.json     # Dependencies
├── vercel.json      # Vercel config
├── README.md        # Documentation
└── tsconfig.json    # TypeScript config
```

## Quick Deploy Commands

After uploading to GitHub, you can deploy via CLI:

**Vercel:**
```bash
npx vercel
```

**Railway:**
```bash
npx @railway/cli deploy
```

Choose Vercel for easiest deployment with best free tier support.