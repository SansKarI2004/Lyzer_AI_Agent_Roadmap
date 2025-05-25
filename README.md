# Roadmap AI - Product Roadmap Generator

A comprehensive AI-powered platform for generating, managing, and collaborating on product roadmaps with intelligent chat functionality and calendar integration.

## Features

- 🤖 **AI-Powered Roadmap Generation** - Generate detailed product roadmaps using Lyzr AI Agent
- 💬 **Interactive Chat** - Chat with your roadmaps to make real-time modifications
- 📅 **Calendar Integration** - Visualize your roadmap timeline with an integrated calendar
- 📊 **Dashboard Analytics** - Track progress and team assignments
- 📄 **PDF Export** - Export roadmaps to PDF for sharing
- 🔄 **Real-time Updates** - Live collaboration and updates

## Tech Stack

- **Frontend**: React, TypeScript, Tailwind CSS, Vite
- **Backend**: Node.js, Express, TypeScript
- **Database**: In-memory storage (easily replaceable with PostgreSQL)
- **AI Integration**: Lyzr AI Agent API
- **UI Components**: Radix UI, shadcn/ui
- **Deployment**: Vercel

## Environment Variables

Create a `.env` file in the root directory with the following variables:

```env
LYZR_API_KEY=your_lyzr_api_key_here
NODE_ENV=production
```

## Local Development

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd roadmap-ai
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env
   # Add your LYZR_API_KEY to the .env file
   ```

4. **Start the development server**
   ```bash
   npm run dev
   ```

5. **Open your browser**
   Navigate to `http://localhost:5000`

## Deployment to Vercel

### Quick Deploy

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/yourusername/roadmap-ai)

### Manual Deployment

1. **Install Vercel CLI**
   ```bash
   npm install -g vercel
   ```

2. **Login to Vercel**
   ```bash
   vercel login
   ```

3. **Deploy to Vercel**
   ```bash
   vercel
   ```

4. **Set Environment Variables**
   In your Vercel dashboard, go to your project settings and add:
   - `LYZR_API_KEY`: Your Lyzr AI API key
   - `NODE_ENV`: `production`

5. **Deploy**
   ```bash
   vercel --prod
   ```

## GitHub Setup

1. **Initialize Git repository**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   ```

2. **Create GitHub repository**
   - Go to GitHub and create a new repository
   - Copy the repository URL

3. **Push to GitHub**
   ```bash
   git remote add origin https://github.com/yourusername/roadmap-ai.git
   git branch -M main
   git push -u origin main
   ```

4. **Connect to Vercel**
   - Go to Vercel dashboard
   - Import your GitHub repository
   - Configure environment variables
   - Deploy automatically on every push

## Project Structure

```
roadmap-ai/
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/         # Application pages
│   │   ├── lib/           # Utility functions and API calls
│   │   └── hooks/         # Custom React hooks
├── server/                # Backend Express server
│   ├── index.ts          # Server entry point
│   ├── routes.ts         # API routes
│   ├── storage.ts        # Data storage layer
│   └── vite.ts           # Vite integration
├── shared/               # Shared types and schemas
│   └── schema.ts        # Zod schemas and types
├── vercel.json          # Vercel deployment configuration
└── README.md           # This file
```

## API Endpoints

- `GET /api/roadmaps` - Get all roadmaps
- `POST /api/roadmaps` - Create new roadmap
- `GET /api/roadmaps/:id` - Get specific roadmap
- `PATCH /api/roadmaps/:id` - Update roadmap
- `DELETE /api/roadmaps/:id` - Delete roadmap
- `POST /api/roadmaps/chat` - Chat with roadmap AI

## Features Overview

### Roadmap Generation
- Input product vision, features, team capacity, and deadlines
- AI generates comprehensive roadmaps with timelines and priorities
- Support for different output formats and methodologies

### Interactive Chat
- Chat with your generated roadmaps
- Request modifications and updates in natural language
- AI provides formatted responses with roadmap changes

### Calendar View
- Visual timeline of your roadmap features and deadlines
- Color-coded events by priority and type
- Monthly view with event details
- Upcoming events section

### Dashboard
- Project progress tracking
- Team member assignments
- Meeting schedules
- Task priorities

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, email support@roadmapai.com or create an issue in the GitHub repository.