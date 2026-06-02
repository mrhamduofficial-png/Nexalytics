# Nexalytics AI - Production-Grade SaaS Platform

## Overview

Nexalytics AI is an enterprise-grade SaaS platform that empowers businesses to grow with AI-powered analytics, CRM, marketing planning, and business intelligence. Built with modern technology stack for scalability, security, and performance.

## 🎯 Key Features

- **AI-Powered Analytics**: Real-time business metrics and KPI tracking
- **CRM System**: Lead management and customer relationship management
- **Marketing Planner**: AI-generated marketing strategies and budget allocation
- **Content Generator**: Blog articles, emails, social media content
- **Task Manager**: Project management and task tracking
- **Reporting System**: Automated daily/weekly/monthly reports with export options
- **AI Assistant**: Business, marketing, and content consultation
- **Multi-tenant Architecture**: Support for agencies and multi-business management
- **Subscription Management**: Flexible pricing plans with Stripe integration
- **Admin Dashboard**: Complete platform monitoring and management

## 🏗️ Architecture Overview

### Tech Stack

**Frontend:**
- Next.js 15 (App Router)
- TypeScript
- TailwindCSS
- ShadCN UI Components
- Zustand (State Management)
- React Query (Data Fetching)
- Axios (HTTP Client)

**Backend:**
- Node.js + Express.js
- TypeScript
- Prisma ORM
- PostgreSQL
- JWT Authentication
- Role-Based Access Control (RBAC)

**Infrastructure:**
- Vercel (Frontend Deployment)
- Supabase (Database & Auth)
- Stripe (Payments)
- SendGrid (Email)

## 📁 Project Structure

```
Nexalytics/
├── frontend/               # Next.js Application
│   ├── public/
│   ├── src/
│   │   ├── app/           # App Router Pages
│   │   ├── components/    # Reusable Components
│   │   ├── hooks/         # Custom React Hooks
│   │   ├── lib/           # Utilities & Helpers
│   │   ├── services/      # API Services
│   │   ├── store/         # Zustand Stores
│   │   ├── types/         # TypeScript Types
│   │   └── styles/        # Global Styles
│   ├── .env.local
│   ├── next.config.js
│   ├── tailwind.config.ts
│   └── tsconfig.json
│
├── backend/               # Express.js API
│   ├── src/
│   │   ├── routes/        # API Routes
│   │   ├── controllers/   # Request Handlers
│   │   ├── services/      # Business Logic
│   │   ├── middleware/    # Express Middleware
│   │   ├── utils/         # Helper Functions
│   │   ├── types/         # TypeScript Types
│   │   ├── config/        # Configuration
│   │   └── index.ts       # Entry Point
│   ├── .env
│   ├── tsconfig.json
│   ├── jest.config.js
│   └── Dockerfile
│
├── database/              # Prisma & Migrations
│   ├── schema.prisma      # Database Schema
│   ├── migrations/        # Database Migrations
│   └── seed.ts            # Seed Script
│
├── docs/                  # Documentation
│   ├── API.md
│   ├── DEPLOYMENT.md
│   ├── ARCHITECTURE.md
│   └── DATABASE.md
│
└── docker-compose.yml     # Local Development
```

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- PostgreSQL 14+
- npm or yarn

### Installation

```bash
# Clone repository
git clone https://github.com/mrhamduofficial-png/Nexalytics.git
cd Nexalytics

# Backend Setup
cd backend
npm install
cp .env.example .env
npm run dev

# Frontend Setup (in new terminal)
cd ../frontend
npm install
cp .env.local.example .env.local
npm run dev
```

### Database Setup

```bash
cd database
npx prisma migrate dev --name init
npx prisma db seed
```

## 📊 Database Schema

Key entities:
- **Users**: Authentication and profiles
- **Businesses**: Business information and settings
- **Leads**: CRM lead management
- **Tasks**: Task and project management
- **Reports**: Generated reports and analytics
- **Subscriptions**: Subscription plans and billing
- **Notifications**: User and admin notifications
- **AI Conversations**: AI assistant interactions

## 🔐 Security Features

- JWT-based authentication
- Role-Based Access Control (Admin, Manager, User)
- Environment variable management
- SQL injection prevention (Prisma ORM)
- CORS protection
- Rate limiting
- Input validation and sanitization
- Encrypted passwords (bcrypt)

## 📈 Deployment

### Frontend (Vercel)
```bash
vercel --prod
```

### Backend (Docker/Railway/Render)
```bash
docker build -t nexalytics-api .
docker run -p 3001:3001 nexalytics-api
```

### Database (Supabase)
- PostgreSQL hosted on Supabase
- Automated backups
- Real-time capabilities

## 📚 API Documentation

See `/docs/API.md` for complete API reference.

### Main Endpoints
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/dashboard/overview` - Dashboard metrics
- `GET /api/leads` - List leads
- `POST /api/leads` - Create lead
- `GET /api/reports` - Generate reports
- `POST /api/ai/assistant` - AI consultation
- `GET /api/subscriptions` - Get subscription info

## 📝 License

MIT License - See LICENSE file for details

## 🤝 Contributing

Contributions welcome! Please see CONTRIBUTING.md for guidelines.

## 📞 Support

For support, email: support@nexalytics.ai
