# Taru2 - Multi-Role Educational Platform

A comprehensive educational platform designed for students, parents, teachers, parent organizations, and administrators. The platform features personalized learning experiences, role-based dashboards, and secure authentication.

## 🚀 Features

### Authentication & User Management
- **Multi-role support**: Students, Parents, Teachers, Parent Organizations, Admins
- **Secure authentication**: JWT tokens with HTTP-only cookies
- **Role-based access control**: Different dashboards and permissions for each role
- **User onboarding**: Multi-step registration and profile setup

### Student Learning Experience
- **Personalized Assessment**: Skill & Interest Form with 4 comprehensive steps
- **Diagnostic Testing**: Interactive assessment covering Math, Reading, Writing, Science, and Technology
- **Learning Profile**: Detailed results summary with personalized insights
- **Recommended Modules**: AI-powered module recommendations based on assessment results
- **Learning Paths**: Structured curriculum paths with milestones and progress tracking
- **Module Details**: Comprehensive module information with content breakdown
- **Progress Tracking**: Real-time progress monitoring and XP system

### Learning Content
- **Multi-category modules**: Academic, Vocational, and Life Skills
- **Diverse content types**: Videos, Quizzes, Stories, Interactive activities, Projects
- **Difficulty levels**: Beginner, Intermediate, Advanced
- **XP and Badge system**: Gamified learning experience
- **Prerequisites and dependencies**: Structured learning progression

### Dashboard Features
- **Role-specific dashboards**: Tailored interfaces for each user type
- **Progress analytics**: Visual progress tracking and statistics
- **Quick actions**: Easy access to key features
- **Notifications**: Real-time updates and alerts

## 🛠️ Technology Stack

- **Frontend**: Next.js 14, React, TypeScript, Tailwind CSS
- **Backend**: Next.js API Routes, Node.js
- **Database**: MongoDB with Mongoose ODM
- **Authentication**: JWT tokens with HTTP-only cookies
- **Styling**: Tailwind CSS with dark mode support

## 📁 Project Structure

```
taru2/
├── app/
│   ├── api/                    # API endpoints
│   │   ├── auth/              # Authentication routes
│   │   ├── assessment/        # Assessment APIs
│   │   ├── modules/           # Module management
│   │   ├── learning-paths/    # Learning path APIs
│   │   └── student/           # Student-specific APIs
│   ├── dashboard/             # Role-based dashboards
│   ├── skill-assessment/      # Skill & Interest Form
│   ├── diagnostic-assessment/ # Diagnostic Testing
│   ├── result-summary/        # Assessment Results
│   ├── recommended-modules/   # Module Recommendations
│   ├── curriculum-path/       # Learning Paths
│   └── modules/               # Module Details
├── models/                    # Database models
├── lib/                       # Utility libraries
├── scripts/                   # Database seeding
└── types/                     # TypeScript definitions
```

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ 
- MongoDB database
- npm or yarn

### Installation

1. **Clone the repository**
```bash
   git clone <repository-url>
   cd taru2
```

2. **Install dependencies**
```bash
npm install
```

3. **Environment Setup**
   Create a `.env.local` file in the root directory:
   ```env
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   ```

4. **Database Setup**
   ```bash
   # Run the seed script to populate sample data
   node scripts/seed-data.js
   ```

5. **Start the development server**
```bash
npm run dev
```

6. **Access the application**
   Open [http://localhost:3000](http://localhost:3000) in your browser

## 📚 Learning Platform Flow

### 1. Student Onboarding
1. **Registration**: Students create accounts with basic information
2. **Profile Setup**: Complete name and preferences setup
3. **Skill Assessment**: 4-step comprehensive assessment
   - Step 1: Language preferences and learning styles
   - Step 2: Academic interests and free time activities
   - Step 3: Strengths, weaknesses, and career interests
   - Step 4: Personal inspirations and goals

### 2. Diagnostic Assessment
- **15 interactive questions** covering 5 skill areas
- **Real-time scoring** and progress tracking
- **Learning style identification**
- **Skill level determination**

### 3. Personalized Learning
- **Result Summary**: Comprehensive learning profile
- **Recommended Modules**: AI-powered suggestions
- **Learning Paths**: Structured curriculum journeys
- **Module Details**: In-depth content exploration

## 🎯 Key Pages

### Assessment Pages
- **`/skill-assessment`**: Multi-step skill and interest form
- **`/diagnostic-assessment`**: Interactive diagnostic testing
- **`/result-summary`**: Assessment results and insights

### Learning Pages
- **`/recommended-modules`**: Personalized module recommendations
- **`/curriculum-path`**: Learning paths and milestones
- **`/modules/[id]`**: Detailed module information

### Dashboard Pages
- **`/dashboard/student`**: Student dashboard with quick actions
- **`/dashboard/parent`**: Parent monitoring dashboard
- **`/dashboard/teacher`**: Teacher management dashboard
- **`/dashboard/admin`**: Administrative dashboard

## 🔧 API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout
- `GET /api/auth/me` - Get current user

### Assessment
- `POST /api/assessment/skills-interests` - Submit skill assessment
- `GET /api/assessment/skills-interests` - Get assessment data
- `POST /api/assessment/diagnostic` - Submit diagnostic results

### Modules
- `GET /api/modules/recommended` - Get recommended modules
- `GET /api/modules/[id]` - Get module details
- `POST /api/modules/[id]/start` - Start a module

### Learning Paths
- `GET /api/learning-paths` - Get learning paths with progress

## 🎨 UI/UX Features

- **Responsive Design**: Works on all device sizes
- **Dark Mode Support**: Toggle between light and dark themes
- **Accessibility**: WCAG compliant design
- **Interactive Elements**: Hover effects, animations, and transitions
- **Progress Indicators**: Visual progress tracking throughout the platform
- **Voice Input Support**: Speech recognition for text inputs

## 🔒 Security Features

- **HTTP-only Cookies**: Secure token storage
- **JWT Authentication**: Stateless authentication
- **Role-based Authorization**: Protected routes and APIs
- **Input Validation**: Server-side validation for all inputs
- **Error Handling**: Comprehensive error management

## 📊 Database Models

### Core Models
- **User**: User accounts and profiles
- **Student**: Student-specific information
- **Assessment**: Skill and diagnostic assessment data
- **Module**: Learning module content and metadata
- **LearningPath**: Curriculum paths and milestones
- **StudentProgress**: Progress tracking and analytics

## 🚀 Deployment

### Production Build
```bash
npm run build
npm start
```

### Environment Variables
Ensure all required environment variables are set in production:
- `MONGODB_URI`
- `JWT_SECRET`
- `NODE_ENV=production`

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📝 License

This project is licensed under the MIT License.

## 🆘 Support

For support and questions, please contact the development team or create an issue in the repository.

---

**Taru2** - Empowering education through personalized learning experiences. 