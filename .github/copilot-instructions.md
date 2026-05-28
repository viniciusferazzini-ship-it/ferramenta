# Copilot Instructions for Ferramenta de Preços

## Project Overview

Ferramenta de Preços is a full-stack web application for managing and analyzing pricing data. Built with a modern monorepo structure using pnpm workspaces.

## Architecture

### Monorepo Structure
- **packages/api**: Express.js backend with TypeScript
- **packages/web**: Next.js frontend with React
- **packages/shared**: Shared TypeScript types and utilities

### Tech Stack
- **Backend**: Node.js, Express, PostgreSQL, Prisma ORM
- **Frontend**: React, Next.js, TypeScript, Tailwind CSS
- **Database**: PostgreSQL with Prisma migrations
- **Package Manager**: pnpm

## Database Schema

### Core Tables
1. **users** - User accounts and authentication
2. **products** - Product catalog
3. **pricing_tiers** - Pricing tier definitions
4. **pricing_rules** - Dynamic pricing rules
5. **price_history** - Historical price tracking

## Shared Types

All shared types are in `packages/shared/types/`:
- `User`
- `Product`
- `PricingTier`
- `PricingRule`
- `PriceHistory`

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register user
- `POST /api/auth/login` - Login user
- `POST /api/auth/logout` - Logout user

### Products
- `GET /api/products` - List products
- `POST /api/products` - Create product
- `GET /api/products/:id` - Get product details
- `PUT /api/products/:id` - Update product

### Pricing
- `GET /api/pricing` - Get pricing configuration
- `POST /api/pricing/calculate` - Calculate price
- `GET /api/pricing/history` - Get price history

## Frontend Routes

- `/` - Home/Dashboard
- `/auth/login` - Login page
- `/auth/register` - Registration page
- `/products` - Product list
- `/products/:id` - Product detail
- `/pricing` - Pricing configuration
- `/analytics` - Analytics dashboard
- `/settings` - User settings

## Development Guidelines

1. **Type Safety**: Always use TypeScript, maintain strict mode
2. **Code Organization**: Follow folder structure conventions
3. **Git Workflow**: Create feature branches from `main`
4. **Testing**: Write tests for new features
5. **Documentation**: Update this file when architecture changes

## Commands

```bash
# Install dependencies
pnpm install

# Development
pnpm dev

# Build
pnpm build

# Test
pnpm test

# Lint
pnpm lint

# Database migrations
cd packages/api && pnpm prisma migrate dev
```
