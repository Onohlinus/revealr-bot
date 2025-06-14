# Anonymous Confessions Platform

A Telegram bot for anonymous confessions with web viewer, content filtering, and emoji reactions.

## Features

- ✅ Anonymous confession submission via web interface
- ✅ Telegram bot integration for private submissions
- ✅ Category filtering (love, work, family, friendship, personal, secret)
- ✅ Emoji reaction system (heart, hug, support, think)
- ✅ Content filtering to remove contact information
- ✅ Real-time statistics dashboard
- ✅ Mobile-responsive design
- ✅ Reporting system for inappropriate content

## Quick Start

### Prerequisites
- Node.js 18+ installed
- npm or yarn package manager

### Installation

1. Clone or download this repository
2. Install dependencies:
```bash
npm install
```

3. (Optional) Set up Telegram Bot:
   - Create a bot via @BotFather on Telegram
   - Add your bot token to environment variables:
```bash
export TELEGRAM_BOT_TOKEN=your_bot_token_here
```

4. Start the application:
```bash
npm run dev
```

5. Open your browser to `http://localhost:5000`

## Deployment Options

### Vercel (Recommended for Free Hosting)

1. Install Vercel CLI:
```bash
npm i -g vercel
```

2. Deploy:
```bash
vercel
```

### Render

1. Connect your GitHub repository to Render
2. Set build command: `npm install`
3. Set start command: `npm start`

### Railway

1. Connect your GitHub repository to Railway
2. Set start command: `npm start`

## Environment Variables

- `TELEGRAM_BOT_TOKEN` - Your Telegram bot token (optional)
- `PORT` - Port number (default: 5000)
- `NODE_ENV` - Environment (development/production)

## Project Structure

```
├── client/          # React frontend
│   ├── src/
│   │   ├── components/  # UI components
│   │   ├── pages/       # Page components
│   │   └── lib/         # Utilities and API
├── server/          # Express backend
│   ├── index.ts     # Main server file
│   ├── routes.ts    # API routes
│   ├── storage.ts   # In-memory storage
│   ├── bot.ts       # Telegram bot
│   └── contentFilter.ts # Content filtering
├── shared/          # Shared types and schemas
└── package.json     # Dependencies and scripts
```

## API Endpoints

- `GET /api/confessions` - Get confessions with optional filtering
- `POST /api/confessions` - Submit new confession
- `POST /api/confessions/:id/reactions` - Add reaction
- `POST /api/confessions/:id/report` - Report confession
- `GET /api/stats` - Get platform statistics
- `GET /api/categories` - Get category statistics

## License

MIT License