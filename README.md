# Dedalus CPQ - Configure, Price, Quote Platform

Enterprise web platform for CPQ (Configure, Price, Quote) management for Dedalus Healthcare Systems Group.

## 🎯 Features

- Quote creation and management
- Multi-product quotes with SKU pricing
- Dynamic pricing engine with margin rules
- Role-based approval workflow
- Billing and engagement calculation
- PDF proposal generation
- Complete audit trail
- Admin panel for configuration

## 📚 Project Structure

```
dedalus-cpq/
├── apps/
│   ├── api/                 # NestJS Backend
│   └── web/                 # Next.js Frontend
├── packages/
│   ├── shared/              # Shared types and utilities
│   └── ui/                  # Shared React components
├── prisma/                  # Database schema and migrations
├── docker/                  # Docker configuration
└── docs/                    # Documentation
```

## 🛠 Tech Stack

- **Frontend**: Next.js, React, TypeScript, TailwindCSS
- **Backend**: NestJS, Node.js, TypeScript
- **Database**: PostgreSQL + Prisma ORM
- **Authentication**: JWT
- **Validation**: Zod
- **Forms**: React Hook Form
- **Tables**: TanStack Table
- **PDF**: PDFKit
- **Deployment**: Docker, AWS-ready

## 🚀 Quick Start

```bash
# Install dependencies
pnpm install

# Start PostgreSQL
docker-compose up -d

# Setup database
cd apps/api && pnpm prisma migrate dev

# Seed initial data
pnpm prisma db seed

# Run development servers
pnpm dev
```

## 📖 Documentation

See [docs/](./docs/) for detailed documentation.
