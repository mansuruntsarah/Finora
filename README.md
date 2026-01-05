# 💰 Finora - AI-Powered Personal Finance Management Platform

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js Version](https://img.shields.io/badge/Node.js-%3E%3D18.0.0-green)](https://nodejs.org/)
[![React Version](https://img.shields.io/badge/React-18.3+-blue)](https://reactjs.org/)
[![Express.js](https://img.shields.io/badge/Express.js-4.19+-lightgrey)](https://expressjs.com/)

---

## 📋 Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Project Architecture](#project-architecture)
- [Prerequisites](#prerequisites)
- [Installation & Setup](#installation--setup)
- [Running the Application](#running-the-application)
- [Project Structure](#project-structure)
- [API Documentation](#api-documentation)
- [Database Models](#database-models)
- [Configuration](#configuration)
- [Features in Detail](#features-in-detail)
- [Contributing](#contributing)
- [License](#license)
- [Support](#support)

---

## 🎯 Overview

**Finora** is a comprehensive, AI-powered personal finance management platform designed to help users take control of their financial lives. Built with modern web technologies and powered by Google's Generative AI, Finora provides intelligent financial insights, budget planning, debt tracking, and personalized recommendations.

Whether you're a student managing pocket money, a professional planning investments, or someone looking to optimize their finances, Finora adapts to your needs with its intelligent AI assistant and comprehensive financial tools.

### Mission
To democratize financial literacy and empowerment by providing accessible, intelligent, and personalized financial management tools for everyone.

---

## ✨ Key Features

### 💳 **Expense & Income Management**
- Track all expenses and income sources in real-time
- Categorize transactions automatically with AI assistance
- Add bulk expenses and schedule recurring transactions
- Detailed transaction history with filtering and search

### 💡 **Budget Planning & Analysis**
- Create and manage multiple budgets
- Visual budget tracking with progress indicators
- Smart budget recommendations based on spending patterns
- Alert system for budget overruns

### 🎯 **Savings Goals**
- Set and track multiple financial goals
- Visual progress tracking with milestone celebrations
- Goal recommendation engine
- Deadline management and progress notifications

### 📊 **Comprehensive Dashboard**
- Real-time financial overview
- Interactive charts and visualizations (Chart.js)
- Key financial metrics at a glance
- Spending trends and analytics

### 🤖 **AI-Powered Features**
- **Smart Transaction Categorization**: Automatically categorize expenses
- **Financial Insights**: AI-generated financial advice and recommendations
- **Predictive Scenarios**: What-if analysis for financial planning
- **Personality Quiz**: Discover your financial personality and get tailored advice
- **Finance Knowledge Base**: AI-powered educational content about personal finance

### 💳 **Debt Management**
- Track multiple debts with interest calculations
- Payment planning and prioritization strategies
- Debt payoff timeline visualization
- Interest savings calculator

### 📱 **Bills & Recurring Payments**
- Manage and track bills
- Set payment reminders
- Automatic bill notifications
- Payment history tracking

### 😊 **Emotional Check-ins**
- Track emotional state related to finances
- Understand spending patterns during emotional states
- Wellness recommendations
- Financial stress management insights

### 📚 **Financial Education**
- Comprehensive finance lessons and tutorials
- Interactive financial personality quiz
- Income opportunity discovery
- Financial literacy tracking

### 🔔 **Smart Notifications**
- Real-time alerts for budget milestones
- Upcoming bill reminders
- Goal achievement notifications
- Custom notification preferences

### 👤 **User Profile & Settings**
- Comprehensive user profile management
- Customizable financial preferences
- Security settings and password management
- Account management and data management

---

## 🛠 Tech Stack

### **Frontend**
- **Framework**: React 18.3+ with Hooks
- **Build Tool**: Vite 7.2+ (Lightning-fast build tool)
- **Styling**: Tailwind CSS 3.4 with PostCSS
- **State Management**: React Context API
- **HTTP Client**: Axios 1.13+
- **Routing**: React Router DOM 6.26+
- **UI Animations**: Framer Motion 12.23
- **Data Visualization**: Chart.js 4.4
- **3D Graphics**: Three.js & React Three Fiber (future 3D features)
- **Icons**: Lucide React 0.555
- **Notifications**: React Hot Toast 2.6

### **Backend**
- **Runtime**: Node.js (v18+)
- **Framework**: Express.js 4.19+
- **Database**: MongoDB 8.6+ with Mongoose ODM
- **AI Integration**: Google Generative AI (Gemini API)
- **Authentication**: bcryptjs 2.4 for password hashing
- **Environment**: dotenv 16.4 for configuration
- **API Features**: CORS enabled, JSON middleware
- **Development**: Nodemon 3.1 for hot reload

### **Infrastructure**
- **Port Configuration**: 
  - Frontend: 5173 (Vite dev server)
  - Backend: 5000 (Express API)
- **API Proxying**: Vite proxy configuration for seamless client-server communication

---

## 🏗 Project Architecture

```
Finora (Root)
├── client/                          # React Frontend Application
│   ├── src/
│   │   ├── pages/                   # Page components (20+ routes)
│   │   ├── App.jsx                  # Main routing component
│   │   ├── main.jsx                 # React entry point
│   │   ├── index.css                # Global styles
│   │   └── ...
│   ├── public/                      # Static assets
│   ├── vite.config.js               # Vite configuration with API proxy
│   ├── tailwind.config.js           # Tailwind CSS config
│   ├── postcss.config.js            # PostCSS config
│   └── package.json                 # Frontend dependencies
│
├── server/                          # Node.js/Express Backend
│   ├── src/
│   │   ├── app.js                   # Express app configuration
│   │   ├── server.js                # Alternative server entry
│   │   ├── secret.js                # Secret/API key management
│   │   ├── config/
│   │   │   └── db.js                # MongoDB connection
│   │   ├── models/                  # Mongoose schemas (12+ models)
│   │   │   ├── User.js
│   │   │   ├── Transaction.js
│   │   │   ├── Goal.js
│   │   │   ├── Budget.js
│   │   │   ├── Debt.js
│   │   │   ├── Bill.js
│   │   │   └── ... (more models)
│   │   ├── routes/                  # API endpoints (14+ routers)
│   │   │   ├── auth.js
│   │   │   ├── profile.js
│   │   │   ├── expenses.js
│   │   │   ├── budget.js
│   │   │   └── ... (more routes)
│   │   ├── middlewares/
│   │   │   ├── auth.js              # Authentication middleware
│   │   │   └── error.js             # Error handling middleware
│   │   ├── seeds/
│   │   │   └── lessons.js           # Database seeding
│   │   └── services/
│   │       └── notificationService.js
│   ├── package.json                 # Backend dependencies
│   └── ... (test files, config files)
│
├── package.json                     # Root package configuration
└── README.md                        # This file
```

### Architecture Pattern: **Full-Stack MERN (Modified)**
- **M**ongoose - MongoDB object modeling
- **E**xpress - Backend framework
- **R**eact - Frontend library
- **N**ode.js - Runtime environment

---

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js**: v18.0.0 or higher ([Download](https://nodejs.org/))
- **npm**: v9.0.0 or higher (comes with Node.js)
- **MongoDB**: Local instance or MongoDB Atlas account ([Create Account](https://www.mongodb.com/cloud/atlas))
- **Git**: For version control ([Download](https://git-scm.com/))

### Required API Keys
- **Google Generative AI (Gemini API)**: Get your key from [Google AI Studio](https://makersuite.google.com/app/apikey)

### System Requirements
- **OS**: Windows, macOS, or Linux
- **RAM**: Minimum 2GB (recommended 4GB)
- **Disk Space**: ~500MB for node_modules and dependencies

---

## 📦 Installation & Setup

### Step 1: Clone the Repository
```bash
git clone <repository-url>
cd Finora
```

### Step 2: Configure Environment Variables

#### Backend Configuration (`.env` in `/server`)
```bash
cd server
cat > .env << EOF
# Database Configuration
MONGODB_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/finora

# API Configuration
PORT=5000
NODE_ENV=development

# Google Generative AI
GOOGLE_API_KEY=your_google_gemini_api_key_here

# JWT Secret (if using JWT authentication)
JWT_SECRET=your_secret_key_here
EOF
```

#### Frontend Configuration (Optional - `.env` in `/client`)
```bash
cd ../client
cat > .env << EOF
VITE_API_BASE_URL=http://localhost:5000/api
VITE_APP_NAME=Finora
EOF
```

### Step 3: Install Dependencies

#### Backend Dependencies
```bash
cd server
npm install
```

#### Frontend Dependencies
```bash
cd ../client
npm install
```

---

## 🚀 Running the Application

### Development Environment

#### Terminal 1: Start MongoDB (if using local instance)
```bash
# For Linux/macOS
mongod

# Or use MongoDB Atlas (no local startup needed)
```

#### Terminal 2: Start Backend Server
```bash
cd server
npm run dev
```

Expected output:
```
[nodemon] starting `node src/app.js`
API server running on http://localhost:5000
```

#### Terminal 3: Start Frontend Development Server
```bash
cd client
npm run dev
```

Expected output:
```
  ➜  Local:   http://localhost:5173/
  ➜  press h + enter to show help
```

### Access the Application
- **Frontend**: http://localhost:5173
- **Backend API**: http://localhost:5000/api

### Production Build

#### Build Frontend
```bash
cd client
npm run build
```
Output will be in `client/dist/`

#### Start Backend in Production
```bash
cd server
npm start
```

---

## 📁 Project Structure in Detail

### Frontend Page Components (`/client/src/pages/`)

| Page | Purpose |
|------|---------|
| `login.jsx` | User login with authentication |
| `Signup.jsx` | New user registration |
| `Dashboard.jsx` | Main financial overview dashboard |
| `profile.jsx` | User profile & settings |
| `addnewexpense.jsx` | Add new expense transactions |
| `AutoExpense.jsx` | AI-powered automatic expense tracking |
| `Transactions.jsx` | View all transactions with filters |
| `BudgetPlanner.jsx` | Create and manage budgets |
| `SavingsGoals.jsx` | Set and track savings goals |
| `Income.jsx` | Manage income sources |
| `IncomeSources.jsx` | Detailed income source tracking |
| `IncomeOpportunities.jsx` | AI-suggested income opportunities |
| `DebtTracker.jsx` | Comprehensive debt management |
| `Bills.jsx` | Bill tracking and management |
| `EmotionalState.jsx` | Emotional financial tracking |
| `FinancialPersonalityQuiz.jsx` | Financial personality assessment |
| `FinanceKnowledge.jsx` | Finance education & lessons |
| `PredictiveScenarios.jsx` | What-if financial scenarios |
| `Notifications.jsx` | View all notifications |

### Backend API Routes (`/server/src/routes/`)

| Route | Endpoint Prefix | Purpose |
|-------|-----------------|---------|
| `auth.js` | `/api/auth` | Authentication & authorization |
| `profile.js` | `/api/profile` | User profile management |
| `dashboard.js` | `/api/dashboard` | Dashboard data aggregation |
| `expenses.js` | `/api/expenses` | Expense CRUD operations |
| `budget.js` | `/api/budget` | Budget management |
| `goals.js` | `/api/goals` | Savings goals management |
| `emotions.js` | `/api/emotions` | Emotional check-ins |
| `income.js` | `/api/income` | Income tracking |
| `transactions.js` | `/api/transactions` | Transaction history |
| `debts.js` | `/api/debts` | Debt management |
| `bills.js` | `/api/bills` | Bill tracking |
| `notifications.js` | `/api/notifications` | Notification management |
| `quiz.js` | `/api/quiz` | Financial personality quiz |
| `knowledge.js` | `/api/knowledge` | Finance educational content |
| `jobs.js` | `/api/jobs` | Income opportunity suggestions |
| `ai.js` | `/api/ai` | AI-powered features & suggestions |

### Database Models (`/server/src/models/`)

| Model | Purpose | Key Fields |
|-------|---------|-----------|
| `User.js` | User accounts & profiles | email, password, name, preferences |
| `Transaction.js` | Financial transactions | amount, category, date, type |
| `Budget.js` | User budgets | category, limit, spent, period |
| `Goal.js` | Savings goals | name, target, current, deadline |
| `Income.js` | Income records | source, amount, frequency, date |
| `Debt.js` | Debt tracking | creditor, amount, interest, dueDate |
| `Bill.js` | Bill records | name, amount, dueDate, frequency |
| `EmotionCheckin.js` | Emotional state | emotion, spending, date, notes |
| `QuizResult.js` | Quiz responses | userId, answers, personality |
| `FinanceLesson.js` | Educational content | title, content, category, level |
| `KnowledgeProgress.js` | Learning progress | userId, lessonId, completed |
| `Notification.js` | User notifications | message, type, read, date |
| `aiTransaction.js` | AI-categorized transactions | - |
| `Contact.js` | User contacts | - |

---

## 📡 API Documentation

### Authentication Endpoints

#### Register User
```http
POST /api/auth/signup
Content-Type: application/json

{
  "email": "user@example.com",
  "password": "securePassword123",
  "name": "John Doe"
}

Response: 201 Created
{
  "success": true,
  "user": { id, email, name },
  "token": "jwt_token_here"
}
```

#### Login User
```http
POST /api/auth/login
Content-Type: application/json

{
  "email": "user@example.com",
  "password": "securePassword123"
}

Response: 200 OK
{
  "success": true,
  "user": { id, email, name },
  "token": "jwt_token_here"
}
```

### Expense Endpoints

#### Create Expense
```http
POST /api/expenses
Authorization: Bearer <token>
Content-Type: application/json

{
  "amount": 50.00,
  "category": "Food",
  "description": "Lunch",
  "date": "2024-01-15"
}

Response: 201 Created
{ id, amount, category, description, date, userId }
```

#### Get All Expenses
```http
GET /api/expenses?month=2024-01&category=Food
Authorization: Bearer <token>

Response: 200 OK
[ { expenses array } ]
```

#### Get Expense by ID
```http
GET /api/expenses/:id
Authorization: Bearer <token>

Response: 200 OK
{ id, amount, category, description, date }
```

#### Update Expense
```http
PUT /api/expenses/:id
Authorization: Bearer <token>
Content-Type: application/json

{ amount, category, description, date }

Response: 200 OK
{ updated expense object }
```

#### Delete Expense
```http
DELETE /api/expenses/:id
Authorization: Bearer <token>

Response: 200 OK
{ success: true }
```

### Budget Endpoints

#### Create Budget
```http
POST /api/budget
Authorization: Bearer <token>
Content-Type: application/json

{
  "category": "Food",
  "limit": 500,
  "period": "monthly"
}

Response: 201 Created
```

#### Get User Budgets
```http
GET /api/budget
Authorization: Bearer <token>

Response: 200 OK
[ { budgets array } ]
```

#### Update Budget
```http
PUT /api/budget/:id
Authorization: Bearer <token>
```

#### Delete Budget
```http
DELETE /api/budget/:id
Authorization: Bearer <token>
```

### Goals Endpoints

#### Create Goal
```http
POST /api/goals
Authorization: Bearer <token>
Content-Type: application/json

{
  "name": "Emergency Fund",
  "targetAmount": 10000,
  "deadline": "2025-12-31",
  "description": "Build 6-month emergency fund"
}
```

#### Get All Goals
```http
GET /api/goals
Authorization: Bearer <token>
```

#### Update Goal Progress
```http
PUT /api/goals/:id
Authorization: Bearer <token>

{ currentAmount, status }
```

### AI Endpoints

#### Get AI Financial Insights
```http
POST /api/ai/insights
Authorization: Bearer <token>
Content-Type: application/json

{
  "type": "spending_analysis"
}

Response: 200 OK
{
  "insight": "AI-generated insight about finances",
  "recommendations": [ "recommendation 1", "recommendation 2" ]
}
```

#### Get Predictive Scenarios
```http
POST /api/ai/predict
Authorization: Bearer <token>
Content-Type: application/json

{
  "scenario": "increase_savings",
  "amount": 100
}
```

---

## 🗄 Database Schema

### User Model
```javascript
{
  _id: ObjectId,
  email: String (unique),
  password: String (hashed),
  name: String,
  avatar: String (optional),
  preferences: {
    currency: String,
    notifications: Boolean,
    theme: String
  },
  createdAt: Date,
  updatedAt: Date
}
```

### Transaction Model
```javascript
{
  _id: ObjectId,
  userId: ObjectId (ref: User),
  amount: Number,
  category: String,
  type: String (income/expense),
  description: String,
  date: Date,
  tags: [String],
  createdAt: Date
}
```

### Budget Model
```javascript
{
  _id: ObjectId,
  userId: ObjectId (ref: User),
  category: String,
  limit: Number,
  spent: Number,
  period: String (daily/weekly/monthly/yearly),
  startDate: Date,
  endDate: Date,
  createdAt: Date
}
```

### Goal Model
```javascript
{
  _id: ObjectId,
  userId: ObjectId (ref: User),
  name: String,
  description: String,
  targetAmount: Number,
  currentAmount: Number,
  deadline: Date,
  status: String (active/completed/abandoned),
  priority: String (high/medium/low),
  createdAt: Date
}
```

---

## ⚙️ Configuration

### Environment Variables Reference

#### Backend (.env in `/server`)
```env
# Database
MONGODB_URI=mongodb+srv://user:pass@cluster.mongodb.net/finora

# Server
PORT=5000
NODE_ENV=development

# Google Generative AI
GOOGLE_API_KEY=sk-...

# Authentication
JWT_SECRET=your_jwt_secret_key
JWT_EXPIRE=7d

# CORS
CORS_ORIGIN=http://localhost:5173
```

#### Frontend (Optional .env in `/client`)
```env
VITE_API_BASE_URL=http://localhost:5000/api
VITE_API_TIMEOUT=30000
VITE_APP_NAME=Finora
```

### Vite Configuration (`/client/vite.config.js`)
- Port: 5173
- API Proxy: `/api` → `http://localhost:5000`
- Auto-refresh on file changes
- Optimized builds with Rollup

### Tailwind CSS Configuration
- Custom color schemes for financial dashboard
- Dark mode support
- Responsive design utilities
- Custom spacing and typography

---

## 💡 Features in Detail

### 1. **Smart Expense Tracking**
- Automatic categorization using AI
- Receipt scanning (future feature)
- Bulk import from bank statements
- Real-time expense notifications

### 2. **Intelligent Budget Management**
- Dynamic budget recommendations based on history
- Spending pattern analysis
- Budget variance alerts
- Multi-currency support

### 3. **Goal Planning & Tracking**
- SMART goal creation
- Progress visualization
- Automated savings suggestions
- Milestone achievements and celebrations

### 4. **AI-Powered Insights**
- Spending analysis and trends
- Personalized financial recommendations
- Predictive scenario modeling
- Financial personality assessment

### 5. **Financial Education**
- Curated finance lessons
- Beginner to advanced content
- Interactive quizzes
- Progress tracking

### 6. **Debt Management**
- Multiple debt tracking
- Interest calculation
- Payment strategy recommendations
- Payoff timeline visualization

### 7. **Emotional Finance Tracking**
- Connect emotions to spending
- Stress pattern analysis
- Wellness recommendations
- Mental health finance integration

### 8. **Real-time Notifications**
- Budget milestone alerts
- Bill payment reminders
- Goal progress notifications
- Custom alert preferences

---

## 🤝 Contributing

We welcome contributions to Finora! Here's how to get started:

### Development Setup
```bash
# 1. Fork the repository
# 2. Clone your fork
git clone https://github.com/yourusername/Finora.git

# 3. Create a feature branch
git checkout -b feature/amazing-feature

# 4. Make your changes and commit
git commit -m 'Add amazing feature'

# 5. Push to your fork
git push origin feature/amazing-feature

# 6. Open a Pull Request
```

### Coding Standards
- Follow ESLint configuration
- Use meaningful variable names
- Add comments for complex logic
- Write descriptive commit messages
- Test your changes locally

### Reporting Bugs
Please use the GitHub Issues tab to report bugs with:
- Clear description of the issue
- Steps to reproduce
- Expected vs actual behavior
- Screenshots if applicable
- Environment details (OS, Node version, etc.)

---

## 📜 License

This project is licensed under the **MIT License** - see the LICENSE file for details.

### MIT License Summary
You are free to:
- ✅ Use commercially
- ✅ Modify the code
- ✅ Distribute the software
- ✅ Use privately

Subject to:
- ℹ️ License and copyright notice

---

## 💬 Support

### Getting Help
- **Documentation**: Check the README and inline code comments
- **Issues**: Browse existing or create new issues on GitHub
- **Email**: [Your contact email]

### Community
- Share your feedback and feature requests
- Connect with other users
- Contribute to discussions

### Resources
- [Express.js Documentation](https://expressjs.com/)
- [React Documentation](https://react.dev/)
- [MongoDB Documentation](https://docs.mongodb.com/)
- [Google Generative AI API](https://ai.google.dev/)
- [Vite Documentation](https://vitejs.dev/)

---

## 🚀 Roadmap

### Upcoming Features
- [ ] Mobile app (React Native)
- [ ] Voice-based expense logging
- [ ] Advanced investment tracking
- [ ] Cryptocurrency portfolio tracking
- [ ] Tax optimization recommendations
- [ ] Social features (compare with friends - anonymously)
- [ ] Bank integration (Plaid)
- [ ] Advanced AI predictions (ML models)
- [ ] Multi-language support
- [ ] Advanced reporting and exports

### Performance Improvements
- [ ] Database query optimization
- [ ] Frontend code splitting
- [ ] Image optimization
- [ ] Caching strategies

---

## 📊 Project Statistics

- **Total Pages**: 20+
- **API Endpoints**: 50+
- **Database Models**: 12+
- **Routes**: 14+
- **Frontend Dependencies**: 20+
- **Backend Dependencies**: 8+

---

## 🎉 Acknowledgments

- Built with ❤️ using modern web technologies
- Powered by Google's Generative AI
- Inspired by leading fintech solutions
- Community contributions and feedback

---

## ✉️ Contact & Social

- **Email**: contact@finora.dev
- **GitHub**: [GitHub Link]
- **Twitter**: [@FinoraApp](https://twitter.com)
- **LinkedIn**: [LinkedIn Profile]

---

<div align="center">

### Made with ❤️ for better financial management

**Finora** - Your AI-Powered Financial Companion

[⬆ Back to Top](#-finora---ai-powered-personal-finance-management-platform)

</div>
