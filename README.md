# Karmayogi Asset Registry and Booking System

<p align="center">
  <img src="https://assets.doptimize.com/images/Karmyogi-assets-logo.png" alt="Karmayogi Logo" width="200"/>
</p>

<p align="center">
  <b>A unified platform for managing government training resources</b>
</p>

<p align="center">
  <a href="#overview">Overview</a> •
  <a href="#key-features">Key Features</a> •
  <a href="#architecture">Architecture</a> •
  <a href="#tech-stack">Tech Stack</a> •
  <a href="#getting-started">Getting Started</a> •
  <a href="#implementation-timeline">Timeline</a> •
  <a href="#contribution">Contribution</a>
</p>

## Overview

The Karmayogi Asset Registry and Booking System centralizes the management of government training assets, facilitating efficient discovery, booking, and utilization across institutions. This platform transforms isolated resource management into a collaborative ecosystem, enhancing resource utilization and training delivery.

### Problem

Government training institutions currently face:
- Asset management in isolated, inconsistent formats
- Limited visibility of resources across departments
- Manual and inefficient booking processes
- Difficulty in discovering suitable training venues
- Lack of utilization metrics and analytics

### Solution

Our platform provides:
- **Unified Asset Registry**: Comprehensive database of all resources
- **Advanced Search & Filters**: Location, capacity, features, availability
- **Smart Booking System**: Real-time reservations with conflict prevention
- **Analytics Dashboard**: Utilization insights and optimization opportunities
- **Multi-institution Collaboration**: Resource sharing across departments

## Key Features

<div align="center">
  <table>
    <tr>
      <td align="center" width="33%">
        <img src="https://assets.doptimize.com/images/asset-management-icon.svg" width="60" height="60"/><br/>
        <b>Asset Management</b><br/>
        Comprehensive tracking of all training resources
      </td>
      <td align="center" width="33%">
        <img src="https://assets.doptimize.com/images/booking-system-icon.svg" width="60" height="60"/><br/>
        <b>Booking System</b><br/>
        Streamlined reservation process
      </td>
      <td align="center" width="33%">
        <img src="https://assets.doptimize.com/images/analytics-icon.svg" width="60" height="60"/><br/>
        <b>Analytics & Reporting</b><br/>
        Data-driven resource optimization
      </td>
    </tr>
    <tr>
      <td align="center">
        <img src="https://assets.doptimize.com/images/user-management-icon.svg" width="60" height="60"/><br/>
        <b>User Management</b><br/>
        Role-based access controls
      </td>
      <td align="center">
        <img src="https://assets.doptimize.com/images/search-discovery-icon.svg" width="60" height="60"/><br/>
        <b>Search & Discovery</b><br/>
        Powerful asset filtering
      </td>
      <td align="center">
        <img src="https://assets.doptimize.com/images/api-integration-icon.svg" width="60" height="60"/><br/>
        <b>API Integration</b><br/>
        Extensible for future needs
      </td>
    </tr>
  </table>
</div>

## Architecture

The system follows a modern three-tier architecture:

```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│  Frontend   │     │   Backend   │     │  Database   │
│  (React)    │◄───►│  (Node.js)  │◄───►│ (PostgreSQL)│
└─────────────┘     └─────────────┘     └─────────────┘
```

- **Frontend**: React application with responsive design
- **Backend**: RESTful API services with Node.js/Express
- **Database**: PostgreSQL with Drizzle ORM
- **Authentication**: JWT-based with role-based access controls
- **Deployment**: Docker containers for consistent environments

## Tech Stack

### Frontend
- **React** - Component-based UI library
- **Tailwind CSS** - Utility-first CSS framework
- **shadcn/ui** - High-quality UI components
- **TanStack Query** - Data fetching and state management
- **React Hook Form** - Form handling with validation
- **Wouter** - Lightweight routing
- **Recharts** - Flexible charting library

### Backend
- **Node.js** - JavaScript runtime
- **Express** - Web framework
- **Drizzle ORM** - Type-safe SQL toolkit
- **PostgreSQL** - Relational database
- **Passport.js** - Authentication middleware
- **Zod** - Schema validation

### DevOps
- **Docker** - Containerization
- **GitHub Actions** - CI/CD pipeline
- **Jest** - Testing framework

## Getting Started

### Prerequisites
- Node.js 18 or higher
- PostgreSQL 15 or higher
- Git

### Installation

1. Clone the repository
```bash
git clone https://github.com/sidgureja7803/GovernmentAssetRegistry.git
cd karmayogi-assets
```

2. Install dependencies
```bash
npm install
```

3. Set up environment variables
```bash
cp .env.example .env
# Edit .env with your database credentials
```

4. Run database migrations
```bash
npm run db:push
```

5. Start the development server
```bash
npm run dev
```

6. Open your browser and navigate to `http://localhost:5000`

## Implementation Timeline

Our 8-week implementation plan:

<table>
  <tr>
    <th>Week</th>
    <th>Milestone</th>
    <th>Deliverables</th>
  </tr>
  <tr>
    <td>1</td>
    <td>Project Setup</td>
    <td>Environment configuration, requirements analysis, schema design</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Core Infrastructure</td>
    <td>Database implementation, authentication, basic API endpoints</td>
  </tr>
  <tr>
    <td>3-4</td>
    <td>Asset Management</td>
    <td>Asset CRUD operations, search functionality, categorization</td>
  </tr>
  <tr>
    <td>5</td>
    <td>Booking System</td>
    <td>Calendar interface, booking workflow, availability checking</td>
  </tr>
  <tr>
    <td>6</td>
    <td>User Management</td>
    <td>Access controls, profiles, administrative functions</td>
  </tr>
  <tr>
    <td>7</td>
    <td>Analytics & Reporting</td>
    <td>Dashboard metrics, data visualization, report generation</td>
  </tr>
  <tr>
    <td>8</td>
    <td>Testing & Deployment</td>
    <td>Quality assurance, documentation, production deployment</td>
  </tr>
</table>

## Project Structure

```
├── client/              # Frontend React application
│   ├── src/
│   │   ├── components/  # UI components
│   │   ├── hooks/       # Custom React hooks
│   │   ├── lib/         # Utility functions
│   │   └── pages/       # Page components
├── server/              # Backend Express application
│   ├── routes.ts        # API routes
│   └── storage.ts       # Database operations
└── shared/              # Shared code between client and server
    └── schema.ts        # Database schema definitions
```

## Contribution

We welcome contributions from the community. To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements

- Ministry of Personnel, Public Grievances and Pensions
- Department of Personnel and Training
- All government training institutions contributing to this initiative

---

<p align="center">
  Made with ❤️ for the <b>Digital India</b> initiative
</p>
