# Copilot Instructions - Dedalus CPQ MVP

## Objective

Build an enterprise web platform for CPQ / Pricing / Quotation of Dedalus Healthcare Systems Group.

## Stack

- Next.js + React + TypeScript + TailwindCSS (Frontend)
- NestJS + Node.js + TypeScript (Backend)
- PostgreSQL + Prisma ORM (Database)
- Docker (Containerization)
- AWS-ready architecture

## Monorepo Structure

```
dedalus-cpq/
  apps/
    web/
    api/
  packages/
    shared/
    ui/
  prisma/
  docker/
  docs/
```

## Core Modules

1. **Auth** - JWT authentication
2. **Users & Roles** - RBAC with 8 profiles
3. **Customers** - Customer management
4. **Quotes** - Quote creation and management
5. **Quote Products** - Product selection
6. **SKU Master** - SKU catalog and pricing
7. **Pricing Engine** - Dynamic pricing calculations
8. **Billing Engine** - Invoice and engagement calculations
9. **Approval Workflow** - Status and approval rules
10. **Audit Trail** - Complete audit logging
11. **Notifications** - Real-time alerts
12. **Proposal Generator** - PDF generation
13. **Admin Panel** - System configuration
14. **Dashboard** - Executive metrics

## RBAC Profiles

- Distribuidor
- Executivo de Contas
- Pré-vendas
- Gerente Financeiro
- Gerente de Serviços
- Diretor Comercial
- Diretor de Serviços
- Administrador

## Quote Fields

- DBR
- Cliente
- CNPJ
- País
- Moeda
- Executivo responsável
- Distribuidor
- Status
- Prazo contratual
- Margem total
- ARR / MRR / TCV
- Total BRL / Total EUR (EUR = BRL / 5.425)

## Products

AIDA, BI4H, C4P, CARE PATHWAY, COMMAND CENTER, FARMASAFE, HYDMEDIA, MEDVIEW CARDIO, MEDVIEW D, MEDVIEW ESPECIALIDADES, MEDVIEW EVO, O4C, RIS E PACS, SWIFTQUEUE, DEEP UNITY, PICASSO

## Commercial Lines

1. License Own IP
2. Membership
3. 3rd Party License
4. Serviços Profissionais
5. Suporte e Manutenção
6. Nuvem / Hardware

## SKU Grid Columns

**Read-only**: Produto, Profit Center, Material Type, PBU, Dynamics 365, Unidade, Preço de Lista, Minimum Gross, Cost Price
**Editable**: Quantidade, Desconto, Observações
**Calculated**: Preço Oferecido, Preço NET, Preço GROSS, Margin

## Pricing Rules

```ts
offeredPrice >= minimumGross
margin >= 64% (normal)
margin < 62% && >= 58% (requires Director Commercial approval)
margin < 58% (requires Director Commercial, Financial, and Services approval)
```

## Quote Status Flow

Draft → Em preenchimento → Em aprovação comercial → Em aprovação financeira → Em aprovação serviços → Aprovada → Liberada para proposta

## Design System

Dedalus Colors:
- Primary: rgb(29, 79, 145) - Dedalus Blue
- Secondary: rgb(66, 152, 181) - Azure
- Success: rgb(197, 232, 108) - Green
- Neutral: rgb(190, 198, 196) - Gray

## Key Features

- Login
- Dashboard with KPIs
- Quote CRUD
- Multi-product selection
- Dynamic SKU pricing
- Approval workflow
- Billing breakdown
- PDF proposal
- Admin panel
- Complete audit trail
