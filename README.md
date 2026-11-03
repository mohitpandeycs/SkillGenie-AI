# 🧞‍♂️ SkillGenie: AI-Powered Career & Skills Advisor

[![React](https://img.shields.io/badge/React-18.2.0-blue.svg)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-18.x-green.svg)](https://nodejs.org/)
[![TailwindCSS](https://img.shields.io/badge/TailwindCSS-3.2.7-blue.svg)](https://tailwindcss.com/)
[![Meta Muse Code](https://img.shields.io/badge/AI%20Development-Meta%20Muse%20Code-0866FF.svg)](https://ai.meta.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 🚀 Live Demo

**Frontend:** [SkillGenie Live](https://skillgenie-frontend.vercel.app)  
**Backend API:** [SkillGenie API](https://skillgenie-backend.vercel.app)

## 📖 Overview

SkillGenie is an AI-powered career guidance platform that helps students and professionals plan their career development through personalized learning roadmaps.

It analyzes individual skills, interests, experience and career goals to provide career recommendations, identify skill gaps, suggest learning resources and offer industry insights.

### 🎯 What Makes SkillGenie Special?

- **AI-Powered Guidance**: Intelligent career analysis and personalized recommendations.
- **Real-Time Market Intelligence**: Job market analysis and salary projections.
- **Personalized Learning**: Learning roadmaps based on individual goals.
- **Industry Opportunities**: Access to internships, jobs and freelance opportunities.
- **24/7 AI Mentor**: An AI assistant for career guidance and technical questions.

## 🌟 Features

### 🎯 Core Features

- **AI-Powered Roadmaps**: Personalized learning paths based on your goals and learning style.
- **Market Analytics**: Job market analysis with 5-8 year growth projections.
- **Smart Skill Matching**: Matches your existing skills with trending careers.
- **Interactive Learning**: Chapter-by-chapter learning with resource recommendations.
- **Gamified Experience**: Points, badges and leaderboards to keep you motivated.
- **AI Chat Mentor**: AI assistance for career guidance and technical questions.

### 📊 Advanced Analytics

- **Progress Tracking**: Detailed analytics on learning patterns and skill development.
- **Market Insights**: Industry demand analysis and salary projections.
- **Career Forecasting**: AI-powered career growth predictions.
- **Skill Gap Analysis**: Identifies missing skills for your target roles.

### 💼 Career Services

- **Job Matching**: AI-powered job recommendations with match scores.
- **Freelance Opportunities**: Curated opportunities based on your skill level.
- **Internship Programs**: Discover relevant internship opportunities.
- **Events & Hackathons**: Find networking events and competitions.

## 🚀 Quick Start

### Prerequisites

- Node.js 18.x or higher
- npm or yarn package manager
- Git

### Installation

**1. Clone the repository**

```bash
git clone https://github.com/mohitpandeycs/SkillGenie.git
cd SkillGenie
```

**2. Install frontend dependencies**

```bash
cd skillgenie
npm install
```

**3. Install backend dependencies**

```bash
cd ../backend
npm install
```

**4. Set up environment variables**

**Backend Configuration:**

```bash
cd backend
cp .env.example .env
```

Edit the `.env` file:

```env
# Server Configuration
NODE_ENV=development
PORT=5000

# AI Services
YOUTUBE_API_KEY=your-youtube-api-key-here
GOOGLE_SEARCH_API_KEY=your-google-search-api-key-here
GOOGLE_SEARCH_ENGINE_ID=your-search-engine-id

# JWT Configuration
JWT_SECRET=your-super-secret-jwt-key-here
JWT_EXPIRE=7d

# Firebase Configuration (Optional)
FIREBASE_PROJECT_ID=your-firebase-project-id
FIREBASE_PRIVATE_KEY=your-firebase-private-key
```

Configure any additional AI provider credentials required by your backend implementation.

**Frontend Configuration:**

```bash
cd skillgenie
cp .env.example .env.local
```

Edit the `.env.local` file:

```env
REACT_APP_API_URL=http://localhost:5000
REACT_APP_FIREBASE_API_KEY=your-firebase-api-key
```

**5. Start the development servers**

Frontend (Terminal 1):

```bash
cd skillgenie
npm start
```

Backend (Terminal 2):

```bash
cd backend
npm run dev
```

**6. Open your browser**

- Frontend: http://localhost:3000
- Backend API: http://localhost:5000

## 🏗️ Project Structure

```text
SkillGenie/
├── skillgenie/                 # React Frontend
│   ├── public/
│   ├── src/
│   │   ├── components/         # Reusable UI components
│   │   │   ├── Navbar.js
│   │   │   ├── Footer.js
│   │   │   └── Sidebar.js
│   │   ├── pages/              # Main application pages
│   │   │   ├── LandingPage.js
│   │   │   ├── Auth.js
│   │   │   ├── Dashboard.js
│   │   │   ├── Questionnaire.js
│   │   │   ├── AIAnalysis.js
│   │   │   ├── Roadmap.js
│   │   │   ├── Chat.js
│   │   │   ├── Quiz.js
│   │   │   └── Career.js
│   │   ├── App.js
│   │   ├── index.js
│   │   └── index.css
│   ├── tailwind.config.js
│   └── package.json
├── backend/                    # Node.js Backend
│   ├── routes/                 # API routes
│   │   ├── auth.js
│   │   ├── users.js
│   │   ├── roadmaps.js
│   │   ├── quizzes.js
│   │   ├── chat.js
│   │   ├── careers.js
│   │   └── analytics.js
│   ├── server.js               # Main server file
│   ├── .env.example            # Environment variables template
│   └── package.json
└── README.md
```

## 🔌 API Documentation

### 🌐 Base URL

- **Development:** `http://localhost:5000`
- **Production:** `https://skillgenie-backend.vercel.app`

### 🔐 Authentication

All protected routes require a Bearer token in the Authorization header:

```text
Authorization: Bearer <your-jwt-token>
```

### 📋 Core Endpoints

**Authentication**

```http
POST /api/auth/register
POST /api/auth/login
POST /api/auth/google
POST /api/auth/verify
```

**AI Services**

```http
POST /api/ai/analyze               # AI career analysis
POST /api/ai/chat                  # Chat with AI mentor
POST /api/ai/roadmap/generate      # Generate learning roadmap
POST /api/ai/roadmap/enhance       # Enhance existing roadmap
GET  /api/ai/skills/trending       # Get trending skills
```

**User Management**

```http
GET  /api/users/profile
PUT  /api/users/profile
GET  /api/users/progress
POST /api/users/questionnaire
```

**Content & Resources**

```http
GET /api/content/youtube           # YouTube recommendations
GET /api/content/courses           # Course recommendations
GET /api/content/articles          # Article recommendations
GET /api/content/projects          # Project ideas
```

**Analytics & Insights**

```http
GET /api/analytics/market          # Market analysis data
GET /api/analytics/salary          # Salary insights
GET /api/analytics/demand          # Skill demand analytics
GET /api/analytics/growth          # Career growth projections
```

### 📨 Example API Calls

**Generate AI Roadmap**

```javascript
const response = await fetch('/api/ai/roadmap/generate', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
    'Authorization': 'Bearer ' + token
  },
  body: JSON.stringify({
    domain: 'Full Stack Development',
    experience: 'beginner',
    timeframe: '6 months',
    goals: ['Build web applications', 'Learn React', 'Master Node.js']
  })
});
```

**Chat with AI Mentor**

```javascript
const response = await fetch('/api/ai/chat', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
    'Authorization': 'Bearer ' + token
  },
  body: JSON.stringify({
    message: 'What should I learn to become a full-stack developer?',
    context: 'career_guidance'
  })
});
```

## 🔒 Security Features

- **JWT Authentication**: Secure token-based authentication.
- **Rate Limiting**: API protection against abuse.
- **Input Validation**: Request validation.
- **CORS Configuration**: Controlled cross-origin requests.
- **Helmet Security**: HTTP security headers.
- **Environment Variables**: Secure configuration management.

## 🚀 Development with Meta Muse Code

Meta Muse Code was used as an AI development assistant throughout the development of SkillGenie.

It helped with:

- Understanding and navigating the project codebase.
- Planning and implementing application features.
- Building React components and backend API routes.
- Debugging errors and improving existing code.
- Working across multiple files and maintaining project context.
- Breaking larger development tasks into manageable steps.

Its long-context and agentic coding capabilities were particularly useful when working on interconnected application features.

## 🚀 Deployment

### Vercel Deployment

**Frontend Deployment**

```bash
cd skillgenie
npm run build
vercel --prod
```

**Backend Deployment**

```bash
cd backend
vercel --prod
```

### Environment Variables Setup

Add the required environment variables in your Vercel dashboard.

**Frontend Variables:**

```env
REACT_APP_API_URL=https://your-backend-domain.vercel.app
REACT_APP_FIREBASE_API_KEY=your-firebase-api-key
```

**Backend Variables:**

```env
NODE_ENV=production
YOUTUBE_API_KEY=your-youtube-api-key-here
GOOGLE_SEARCH_API_KEY=your-google-search-api-key-here
JWT_SECRET=your-super-secret-jwt-key-here
```

Add any additional AI provider credentials required by your backend.

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/amazing-feature`).
3. Commit your changes (`git commit -m 'Add amazing feature'`).
4. Push to the branch (`git push origin feature/amazing-feature`).
5. Open a Pull Request.

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Meta** for Muse Code and React.
- **React Team** for the frontend framework.
- **Node.js** for backend development.
- **TailwindCSS** for the utility-first CSS approach.
- **Framer Motion** for smooth animations.
- **Lucide** for icons.
- **Recharts** for data visualization.

## 👨‍💻 Project Lead

**Mohit Pandey** - Full Stack Developer specializing in AI-powered applications.

- Experience in React, Node.js and AI integration.
- Passionate about making career guidance more accessible through technology.

## 📞 Support & Contact

### Get Help

- **GitHub Issues:** [Report bugs or request features](https://github.com/mohitpandeycs/SkillGenie/issues)
- **Documentation:** Check the repository for setup guides.

### Connect With Me

- **GitHub:** [@mohitpandeycs](https://github.com/mohitpandeycs)
- **LinkedIn:** [@mohitpandeycs](https://linkedin.com/in/mohitpandeycs)

---

<div align="center">

## 🌟 Built with ❤️ by the SkillGenie Team

*Empowering careers through AI-driven intelligence.*

[![GitHub Repo](https://img.shields.io/badge/GitHub-SkillGenie-blue?style=for-the-badge&logo=github)](https://github.com/mohitpandeycs/SkillGenie)
[![MIT License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](https://opensource.org/licenses/MIT)

[⭐ Star this repo](https://github.com/mohitpandeycs/SkillGenie) • [🐛 Report Bug](https://github.com/mohitpandeycs/SkillGenie/issues) • [💡 Request Feature](https://github.com/mohitpandeycs/SkillGenie/issues/new)

</div>