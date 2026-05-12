# Welcome to the Astra IQ / ShopZoon Team 🙌

Hey برو 👋  
Welcome to **ShopZoon** — the main product we are building under the **Astra IQ** GitHub organization.

ShopZoon is an e-commerce platform built for the Iraqi market. The goal is simple: help merchants launch, manage, and grow online stores without needing technical knowledge.

Right now, our focus is **ShopZoon only**.

---

## What We Are Building

ShopZoon is a Shopify-like platform adapted for local merchants, local operations, and real business needs in Iraq.

The product includes:

- Store management
- Product catalog management
- Inventory management
- Storefront APIs
- Admin dashboards
- Checkout and order flows
- Template-driven storefronts
- Merchant/project onboarding
- Deployment workflows
- Developer-friendly APIs for custom storefronts

We are not trying to build every SoftRuby idea at once.  
The current mission is to make **ShopZoon real, usable, and production-ready**.

---

## Product Direction

ShopZoon should feel:

- Serious
- Reliable
- Modern
- Local-market aware
- Easy for merchants
- Flexible for developers
- Strong enough to become infrastructure

The first priority is not building a giant platform.  
The first priority is building a strong commerce core that real stores can use.

---

## Current GitHub Scope

Our active repositories are under:

```txt
https://github.com/Astra-Iq
```

Current ShopZoon repositories:

```txt
Astra-Iq/kinetic
Astra-Iq/Admin-UI-Engine
```

### `Astra-Iq/kinetic`

This is the backend/API side of ShopZoon.

It contains the core API, business logic, modules, integrations, and backend infrastructure needed to power ShopZoon.

Key responsibilities:

- ShopZoon backend API
- Projects / merchants
- Store data models
- Products and taxonomy
- Inventory logic
- Orders and checkout logic
- API contracts
- OpenAPI export
- Authentication integration
- Shared backend packages
- Common error handling

### `Astra-Iq/Admin-UI-Engine`

This is the admin dashboard engine.

It powers the internal and merchant-facing dashboard experience for managing ShopZoon stores.

Key responsibilities:

- Dashboard UI
- CRUD screens
- Forms
- Tables
- Relations management
- Store management views
- Polaris-style admin experience
- API-driven dashboard generation
- Authentication UI integration
- Localization-ready frontend structure

---

## Current Tech Stack

### Backend

Used in `Astra-Iq/kinetic`:

- Rust
- Axum
- SQLx
- PostgreSQL
- Tokio
- Utoipa / OpenAPI tooling
- Validator
- JWT authentication
- Reqwest
- AWS S3-compatible storage SDK
- Shared internal crates

Backend principles:

- Type-safe APIs
- Clear module boundaries
- Explicit errors
- Strong validation
- OpenAPI-first compatibility
- Production-ready database access
- No unnecessary abstraction

---

### Admin Dashboard

Used in `Astra-Iq/Admin-UI-Engine`:

- Vue 3
- Vite
- TypeScript
- Vue Router
- Vue I18n
- TanStack Vue Query
- TanStack Vue Table
- Zod
- ofetch
- Logto Vue SDK
- Polaris Vue components

Frontend principles:

- Clean admin UX
- API-driven screens
- Reusable CRUD patterns
- Strong form validation
- Predictable data fetching
- No Axios
- Merchant-friendly workflows

---

## What We Are Not Working On Right Now

These are not current focus areas:

- Smart home infrastructure
- IoT dashboards
- Generic SoftRuby platform features
- Multi-product ecosystem planning
- Unrelated SaaS ideas
- Over-engineered project management tools
- Premature marketplace features

These may return later.  
For now, everything should serve **ShopZoon**.

---

## Engineering Values

At Astra IQ, we care about building software that is practical, clean, and maintainable.

We believe:

- Software should solve real business problems.
- Developers should understand the system quickly.
- APIs should be predictable.
- Dashboards should reduce work, not add confusion.
- Infrastructure should be boring where possible.
- Complexity must earn its place.
- Small teams can ship serious products.

---

## How To Think About ShopZoon

ShopZoon has two users:

### 1. Merchants

Merchants need simple tools to run their store.

They care about:

- Adding products
- Managing stock
- Receiving orders
- Using coupons
- Editing store content
- Seeing useful data
- Launching fast
- Avoiding technical complexity

### 2. Developers

Developers may use ShopZoon APIs to build custom storefronts and custom commerce experiences.

They care about:

- Stable APIs
- Clear documentation
- Flexible querying
- Custom API views
- Storefront-ready data
- Clean authentication
- Predictable response formats

Good ShopZoon features should respect both sides.

---

## Contribution Workflow

### 1. Clone the repositories

```bash
git clone git@github.com:Astra-Iq/kinetic.git
git clone git@github.com:Astra-Iq/Admin-UI-Engine.git
```

### 2. Work in the correct repository

Backend changes go in:

```txt
Astra-Iq/kinetic
```

Dashboard changes go in:

```txt
Astra-Iq/Admin-UI-Engine
```

### 3. Keep scope clear

Before starting work, define:

- What problem this solves
- Who needs it
- Backend responsibility
- Dashboard responsibility
- API contract changes
- Database changes
- Migration needs
- Acceptance criteria

No vague work should enter active development.

---

## Feature Ownership Guide

| Feature | Backend | Dashboard |
|---|---|---|
| Products | `kinetic` | `Admin-UI-Engine` |
| Categories / taxonomy | `kinetic` | `Admin-UI-Engine` |
| Inventory | `kinetic` | `Admin-UI-Engine` |
| Orders | `kinetic` | `Admin-UI-Engine` |
| Coupons | `kinetic` | `Admin-UI-Engine` |
| Guests checkout | `kinetic` | `Admin-UI-Engine` only when UI is needed |
| Ratings | `kinetic` | `Admin-UI-Engine` for moderation/visibility |
| Banners | `kinetic` | `Admin-UI-Engine` |
| Wishlist | `kinetic` | `Admin-UI-Engine` optional/admin visibility |
| Custom API views | `kinetic` | `Admin-UI-Engine` for configuration UI |
| Storefront APIs | `kinetic` | Usually not dashboard-owned |
| Admin CRUD screens | API support only | `Admin-UI-Engine` |

---

## Coding Expectations

### Backend expectations

- Keep modules focused.
- Validate inputs at the boundary.
- Use shared error handling.
- Avoid leaking raw database errors.
- Keep API responses consistent.
- Write migrations carefully.
- Keep OpenAPI output accurate.
- Prefer explicit domain models over generic JSON blobs.

### Dashboard expectations

- Build reusable admin patterns.
- Keep forms predictable.
- Use typed schemas where possible.
- Avoid duplicated table/form logic.
- Use API contracts as the source of truth.
- Keep UX close to proven commerce admin patterns.
- Avoid visual noise.

---

## Product Priorities

Current priorities should stay close to the commerce core:

1. Merchant/project onboarding
2. Product management
3. Taxonomy and product attributes
4. Inventory and stock state
5. Storefront API stability
6. Cart and checkout
7. Orders
8. Coupons
9. Banners and merchandising
10. Ratings and wishlist
11. Custom API views for developer-built storefronts

Anything outside this list should be questioned before implementation.

---

## Decision Rules

When unsure, use these rules:

### Does this help stores sell?

If yes, it may belong in ShopZoon.

### Does this improve merchant workflow?

If yes, it may belong in the dashboard.

### Does this improve storefront developers?

If yes, it may belong in the backend/storefront API.

### Does this belong to future SoftRuby ecosystem ideas?

If yes, defer it.

### Does this add complexity before product-market proof?

If yes, reduce scope.

---

## Team Culture

We move with focus.

We prefer:

- Clear tasks
- Small pull requests
- Practical architecture
- Honest trade-offs
- Strong defaults
- Fast feedback
- Production mindset

We avoid:

- Building everything at once
- Premature abstractions
- Feature creep
- Unclear ownership
- Random JSON structures
- Dashboard bloat
- Copying big platforms without understanding why

---

## Final Words

Welcome aboard.

ShopZoon is the focus.  
Merchants are the customer.  
Developers are part of the platform.  
The goal is to ship something real, stable, and valuable.

Build carefully.  
Ship clearly.  
Keep the system understandable.

—  
**Astra IQ / ShopZoon Team**
