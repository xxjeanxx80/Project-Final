# 🌸 Beauty Booking Hub - Spa Management Platform

[![Next.js](https://img.shields.io/badge/Next.js-13.0+-black?style=for-the-badge&logo=next.js)](https://nextjs.org/)
[![NestJS](https://img.shields.io/badge/NestJS-10.0+-red?style=for-the-badge&logo=nestjs)](https://nestjs.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0+-blue?style=for-the-badge&logo=typescript)](https://www.typescriptlang.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15+-blue?style=for-the-badge&logo=postgresql)](https://www.postgresql.org/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

A comprehensive spa booking and management platform built with modern web technologies. This platform connects customers with spa service providers, featuring location-based search, real-time booking management, and secure payment processing.

## ✨ Key Features

### 🎯 Customer Experience
- **User Authentication**: Secure JWT-based login/registration system
- **Spa Discovery**: Browse and search spas with advanced filtering
- **Location-Based Search**: Find spas near your location using interactive maps
- **Service Booking**: 3-step booking flow with real-time availability checking
- **Payment Processing**: Multiple payment methods (Cash, Credit Card, PayPal)
- **Booking Management**: View, cancel, and reschedule appointments

### 🏢 Business Management
- **Spa Management**: Complete CRUD operations for spa profiles
- **Service Catalog**: Manage services, pricing, and availability
- **Staff Management**: Assign staff to services and manage schedules
- **Booking Dashboard**: Real-time booking overview and management
- **Financial Reports**: Revenue tracking and commission calculations
- **Customer Management**: View customer history and preferences

### 🔧 Technical Highlights
- **Modular Architecture**: 20+ well-organized backend modules
- **Type Safety**: End-to-end TypeScript with PostgreSQL ENUM support
- **Real-time Features**: Live availability checking and notifications
- **Responsive Design**: Mobile-first UI with Tailwind CSS
- **Interactive Maps**: Location-based search with Leaflet integration

## 🛠️ Tech Stack

### Frontend
| Technology | Version | Purpose |
|------------|---------|---------|
| **Next.js** | 13+ | React Framework with App Router |
| **TypeScript** | 5.0+ | Type-safe JavaScript |
| **Tailwind CSS** | 3.3+ | Utility-first CSS Framework |
| **Radix UI** | Latest | Accessible UI Components |
| **Lucide React** | Latest | Icon Library |
| **Axios** | Latest | HTTP Client |
| **Leaflet** | 1.9.4 | Interactive Maps |
| **React Hook Form** | - | Form Management (removed, using controlled components) |

### Backend
| Technology | Version | Purpose |
|------------|---------|---------|
| **NestJS** | 10+ | Node.js Framework |
| **TypeScript** | 5.0+ | Type-safe JavaScript |
| **TypeORM** | Latest | Object-Relational Mapping |
| **PostgreSQL** | 15+ | Primary Database |
| **JWT** | Latest | Authentication Tokens |
| **Bcrypt** | Latest | Password Hashing |
| **Passport** | Latest | Authentication Middleware |
| **Multer** | Latest | File Upload Handling |
| **Class-validator** | Latest | Input Validation |

### Infrastructure & Tools
| Technology | Purpose |
|------------|---------|
| **Vercel** | Frontend Deployment |
| **Render** | Backend & Database Hosting |
| **Git & GitHub** | Version Control |
| **Swagger** | API Documentation |
| **Figma** | UI/UX Design |

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ 
- PostgreSQL 15+
- npm or pnpm

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/your-username/beauty-booking-hub.git
cd beauty-booking-hub
```

2. **Install dependencies**
```bash
# Frontend
cd Fontend
npm install

# Backend  
cd ../Backend
npm install
```

3. **Environment Setup**
```bash
# Backend environment
cd Backend
cp .env.example .env
# Configure database connection and JWT secrets

# Frontend environment
cd ../Fontend
cp .env.local.example .env.local
# Configure API base URL
```

4. **Database Setup**
```bash
# Run migrations
cd Backend
npm run migration:run

# Seed database (optional)
npm run seed:run
```

5. **Start Development Servers**
```bash
# Backend (http://localhost:3001)
cd Backend
npm run start:dev

# Frontend (http://localhost:3000)
cd ../Fontend
npm run dev
```

## 📁 Project Structure

```
beauty-booking-hub/
├── Backend/                    # NestJS API Server
│   ├── src/
│   │   ├── modules/           # Business Logic Modules (20+)
│   │   │   ├── auth/          # Authentication & Authorization
│   │   │   ├── bookings/      # Booking Management
│   │   │   ├── spas/          # Spa Management
│   │   │   ├── users/         # User Management
│   │   │   ├── services/      # Service Catalog
│   │   │   ├── payments/      # Payment Processing
│   │   │   └── ...            # Other modules
│   │   ├── common/            # Shared Components
│   │   ├── config/            # Configuration Files
│   │   └── main.ts            # Application Entry Point
│   ├── package.json
│   └── tsconfig.json
├── Fontend/                    # Next.js Frontend Application
│   ├── app/                   # App Router Pages
│   │   ├── (auth)/            # Authentication Pages
│   │   ├── (customer)/        # Customer Dashboard
│   │   ├── (owner)/           # Spa Owner Dashboard
│   │   └── (admin)/           # Admin Dashboard
│   ├── components/            # Reusable React Components
│   │   ├── ui/                # UI Components (Radix)
│   │   ├── auth-modal.tsx     # Authentication Modal
│   │   ├── booking-modal.tsx  # Booking Flow
│   │   └── spa-map-view.tsx   # Interactive Maps
│   ├── hooks/                 # Custom React Hooks
│   ├── lib/                   # Utilities & API Clients
│   └── package.json
├── docs/                      # Documentation Files
│   ├── CONG_NGHE_SU_DUNG.md   # Technology Stack Analysis
│   ├── FLOW_LOGIN_TO_BOOKING.md # System Flow Documentation
│   └── PHAN_TICH_MO_HINH_KIEN_TRUC.md # Architecture Analysis
└── README.md                  # This File
```

## 📚 Documentation

### 📖 Technical Documentation
- **[Technology Stack Analysis](./CONG_NGHE_SU_DUNG.md)** - Detailed analysis of technologies used and their benefits
- **[System Flow Documentation](./FLOW_LOGIN_TO_BOOKING.md)** - Complete flow from login to booking with code references
- **[Architecture Analysis](./PHAN_TICH_MO_HINH_KIEN_TRUC.md)** - In-depth architectural analysis and design decisions

### 🔧 API Documentation
- **Swagger UI**: Available at `http://localhost:3001/api` when backend is running
- **API Endpoints**: RESTful API with comprehensive validation and error handling

### 📊 Database Schema
- **PostgreSQL with TypeORM**: Entities with relationships and constraints
- **Migration System**: Version-controlled database schema changes
- **ENUM Types**: Type-safe status fields for data integrity

## 🏗️ Architecture Overview

### System Architecture
```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Frontend      │    │    Backend      │    │    Database     │
│   (Next.js)     │◄──►│   (NestJS)      │◄──►│  (PostgreSQL)   │
│                 │    │                 │    │                 │
│ • React UI      │    │ • REST API      │    │ • ACID Trans.   │
│ • TypeScript    │    │ • JWT Auth      │    │ • Type Safety   │
│ • Tailwind CSS  │    │ • TypeORM       │    │ • ENUM Types    │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

### Key Architectural Decisions
- **Monolithic Layered Architecture**: Optimal for team size and business requirements
- **Type Safety First**: End-to-end TypeScript with PostgreSQL ENUM support
- **Modular Design**: 20+ well-organized modules with clean separation of concerns
- **ACID Transactions**: Strong consistency for booking and payment operations

## 🎯 Key Technical Features

### 🔐 Security
- JWT-based authentication with refresh tokens
- Role-based authorization (Customer, Owner, Admin)
- Password hashing with bcrypt
- Input validation and sanitization
- SQL injection prevention with TypeORM

### 🗺️ Location-Based Features
- Interactive maps with Leaflet & OpenStreetMap
- GPS-based spa search with radius filtering
- Geospatial queries with PostgreSQL
- Real-time distance calculations

### 💼 Business Logic
- Real-time availability checking
- Complex pricing calculations with discounts
- Commission tracking and reporting
- Multi-step booking workflow
- Notification system for booking updates

## 🧪 Testing

```bash
# Backend Unit Tests
cd Backend
npm run test

# Backend E2E Tests
npm run test:e2e

# Frontend Tests (if configured)
cd Fontend
npm run test
```

## 📈 Performance Optimizations

### Frontend
- **Code Splitting**: Dynamic imports for map components
- **Image Optimization**: Next.js Image component with lazy loading
- **Caching**: API response caching with proper invalidation
- **Bundle Optimization**: Tree shaking and minification

### Backend
- **Database Indexing**: Optimized queries for spa search and booking
- **Connection Pooling**: Efficient database connection management
- **Caching Layer**: Redis integration for frequently accessed data
- **Query Optimization**: Efficient TypeORM queries with proper joins

## 🚀 Deployment

### Production Deployment
- **Frontend**: Vercel (automatic deployments from main branch)
- **Backend**: Render (Docker-based deployment)
- **Database**: Render PostgreSQL with automated backups
- **Monitoring**: Application logs and error tracking

### Environment Variables
```bash
# Backend (.env)
DATABASE_URL=postgresql://...
JWT_SECRET=your-jwt-secret
JWT_REFRESH_SECRET=your-refresh-secret

# Frontend (.env.local)
NEXT_PUBLIC_API_URL=http://localhost:3001
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Team

- **Project Developer**: [Your Name]
- **Technologies**: Next.js, NestJS, PostgreSQL, TypeScript
- **Architecture**: Monolithic Layered Architecture
- **Documentation**: Comprehensive technical documentation included

## 🙏 Acknowledgments

- **NestJS Team** - Excellent framework documentation
- **Vercel Team** - Amazing deployment platform
- **Tailwind CSS** - Utility-first CSS framework
- **OpenStreetMap** - Free map data for location features

---

**📞 For Academic Review**: This project demonstrates enterprise-grade development practices with comprehensive documentation, modern architecture patterns, and production-ready features. Please refer to the documentation files in the `/docs` directory for detailed technical analysis.

**🌟 Key Learning Outcomes**:
- Modern full-stack development with TypeScript
- Database design with PostgreSQL and TypeORM
- Authentication and authorization systems
- Location-based services and map integration
- Business logic implementation for booking systems
- API design and documentation best practices
- Performance optimization techniques
- Deployment and DevOps practices
