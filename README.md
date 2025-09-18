# [MoneyCare 🔗](https://money-care.vercel.app/)


MoneyCare is your AI-powered financial companion — helping you track spending, analyze habits, and optimize your finances with smart insights, real-time alerts, and automated reports. Built for simplicity, security, and smarter money management.

## 🌟 Features

### Core Functionality
- **📊 Interactive Dashboard**: Real-time overview of financial status with charts and analytics
- **💰 Transaction Management**: Track income and expenses with detailed categorization
- **🏦 Account Management**: Manage multiple accounts (Current, Savings) with real-time balances
- **📈 Budget Planning**: Set and monitor budgets with spending alerts
- **🔄 Recurring Transactions**: Automate recurring income and expense tracking

### AI-Powered Features
- **🤖 AI Insights**: Personalized financial recommendations using Google Gemini AI
- **📸 Receipt Scanning**: AI-powered receipt recognition and data extraction
- **📧 Smart Notifications**: Automated email alerts for budget thresholds and financial events
- **📊 Spending Analysis**: AI-driven spending pattern analysis and optimization suggestions

### Security & User Experience
- **🔐 Secure Authentication**: Enterprise-grade authentication with Clerk
- **🛡️ Security Protection**: Advanced rate limiting and security with Arcjet
- **📱 Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **🎨 Modern UI**: Clean, intuitive interface built with Tailwind CSS and Radix UI

## 🛠️ Technologies Used

### Frontend & Backend
- **Next.js 15**: Full-stack React framework with App Router
- **React 19**: Latest React with concurrent features
- **TypeScript**: Type-safe development
- **Tailwind CSS**: Utility-first CSS framework
- **Radix UI**: Accessible component primitives

### Database & ORM
- **PostgreSQL**: Robust relational database
- **Prisma**: Modern database ORM with type safety
- **Supabase**: PostgreSQL hosting with connection pooling

### Authentication & Security
- **Clerk**: Complete authentication solution
- **Arcjet**: Rate limiting and security protection
- **Next.js Middleware**: Route protection and security

### AI & External Services
- **Google Gemini AI**: Advanced AI for financial insights
- **Resend**: Reliable email delivery service
- **Inngest**: Background job processing

### Development Tools
- **ESLint**: Code linting and formatting
- **PostCSS**: CSS processing
- **React Hook Form**: Form state management
- **Zod**: Schema validation

## 🚀 Getting Started

### Prerequisites

- Node.js 18+ 
- npm or yarn
- PostgreSQL database (or Supabase account)
- Clerk account for authentication
- Google Cloud account for Gemini AI

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Ramprakash852/MoneyCare.git
   cd MoneyCare
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Setup**
   
   Create a `.env` file in the root directory:
   ```env
   # Database Configuration
   DATABASE_URL="your-postgresql-connection-string"
   DIRECT_URL="your-direct-postgresql-connection-string"
   
   # Clerk Authentication
   NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY="your-clerk-publishable-key"
   CLERK_SECRET_KEY="your-clerk-secret-key"
   NEXT_PUBLIC_CLERK_SIGN_IN_URL="/sign-in"
   NEXT_PUBLIC_CLERK_SIGN_UP_URL="/sign-up"
   NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL="/dashboard"
   NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL="/dashboard"
   
   # AI Services
   GEMINI_API_KEY="your-google-gemini-api-key"
   
   # Email Service
   RESEND_API_KEY="your-resend-api-key"
   
   # Security
   ARCJET_KEY="your-arcjet-api-key"
   ```

### Database Setup

1. **Run Prisma migrations**
   ```bash
   npx prisma migrate deploy
   ```

2. **Generate Prisma client**
   ```bash
   npx prisma generate
   ```

3. **Seed the database (optional)**
   ```bash
   npm run seed
   ```

### Development

1. **Start the development server**
   ```bash
   npm run dev
   ```

2. **Open your browser**
   
   Navigate to [http://localhost:3000](http://localhost:3000)

## 📁 Project Structure

```
ai-finance-platform/
├── app/                    # Next.js app directory
│   ├── (auth)/            # Authentication pages
│   ├── (main)/            # Main application pages
│   ├── api/               # API routes
│   └── globals.css        # Global styles
├── components/            # Reusable UI components
│   └── ui/               # Base UI components
├── actions/              # Server actions
├── lib/                  # Utility functions and configurations
├── prisma/               # Database schema and migrations
├── public/               # Static assets
├── emails/               # Email templates
└── hooks/                # Custom React hooks
```

## 🔧 Available Scripts

```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run start        # Start production server
npm run lint         # Run ESLint
npm run email        # Email development server
```

## 🗃️ Database Schema

### Core Models
- **Users**: User profile and authentication data
- **Accounts**: Financial accounts (Current/Savings)
- **Transactions**: Income and expense records
- **Budgets**: Budget planning and tracking

### Key Features
- UUID primary keys for security
- Cascading deletes for data integrity
- Indexed foreign keys for performance
- Enum types for data consistency

## 🔐 Authentication Flow

1. User signs up/signs in through Clerk
2. User profile is automatically created in the database
3. Protected routes redirect unauthenticated users
4. Server actions validate user permissions

## 🤖 AI Features

### Financial Insights
- Spending pattern analysis
- Budget optimization suggestions
- Expense categorization recommendations
- Financial goal tracking

### Receipt Processing
- OCR text extraction from receipt images
- Automatic transaction creation
- Merchant and amount detection

## 📧 Email Notifications

- Budget threshold alerts
- Weekly/monthly financial summaries
- Transaction confirmations
- Security notifications

## 🛡️ Security Features

- Rate limiting on all API endpoints
- CSRF protection
- Input validation and sanitization
- Secure database queries with Prisma
- Environment variable validation

## 🚀 Deployment

### Build for Production

```bash
npm run build
```

### Environment Variables

Ensure all production environment variables are set:
- Use production Clerk keys
- Configure production database
- Set up production email service
- Configure AI service limits

### Recommended Platforms
- **Vercel**: Optimal for Next.js applications
- **Netlify**: Great alternative with easy setup
- **Railway**: Good for full-stack applications
- **AWS/GCP/Azure**: Enterprise-grade hosting

## 🧪 Testing

```bash
# Run all tests
npm test

# Run tests in watch mode
npm run test:watch

# Run E2E tests
npm run test:e2e
```

## 📈 Performance

- Server-side rendering for fast initial loads
- Optimized database queries with Prisma
- Image optimization with Next.js
- Code splitting and lazy loading
- Caching strategies for improved performance

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines
- Follow TypeScript best practices
- Write tests for new features
- Follow the existing code style
- Update documentation for new features

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

- 📧 Email: support@ai-finance-platform.com
- 💬 Discord: [Community Server](https://discord.gg/your-server)
- 📚 Documentation: [Full Documentation](https://docs.ai-finance-platform.com)

## 🎯 Roadmap

- [ ] Mobile app development (React Native)
- [ ] Advanced AI financial advisory features
- [ ] Integration with banks and financial institutions
- [ ] Multi-currency support
- [ ] Investment tracking and analysis
- [ ] Tax preparation assistance
- [ ] Financial planning tools

## 🙏 Acknowledgments

- [Next.js](https://nextjs.org/) for the amazing framework
- [Clerk](https://clerk.dev/) for authentication services
- [Prisma](https://prisma.io/) for database management
- [Google](https://cloud.google.com/vertex-ai) for AI capabilities
- [Vercel](https://vercel.com/) for hosting platform

---

**Made with ❤️ for better financial management**
