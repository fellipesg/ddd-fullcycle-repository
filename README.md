# DDD Repositories — Orders & Aggregates

Full Cycle DDD challenge focused on **repository implementations** for domain aggregates (Customer, Product, Order), including persistence with Sequelize/SQLite and automated tests.

## Highlights

- Repository interfaces in the domain layer
- Sequelize implementations in infrastructure
- Order repository covering aggregate persistence (order + items)
- Factories, value objects, and domain services (e.g. order total)
- Jest suite validating repository behavior

## Stack

| Layer | Tech |
|-------|------|
| Language | TypeScript |
| ORM | Sequelize + sequelize-typescript |
| DB | SQLite |
| Tests | Jest + SWC |

## Prerequisites

- Node.js 18+
- npm

## Setup

```bash
git clone https://github.com/fellipesg/ddd-fullcycle-repository.git
cd ddd-fullcycle-repository
npm install
```

## Tests

```bash
npm test
```

Optional typecheck:

```bash
npm run tsc
```

## Project layout

```
src/
├── domain/
│   ├── @shared/            # Repository contracts, event bus
│   ├── customer/
│   ├── product/
│   └── checkout/           # Order entity, factory, service
└── infrastructure/
    ├── customer/repository/sequelize/
    ├── product/repository/sequelize/
    └── order/repository/…  # Order repository + specs
```

## What this demonstrates

- Repository pattern as the persistence boundary for aggregates
- Mapping between rich domain models and relational tables
- Testing repositories with a real SQLite database
- Keeping domain free of ORM details

## License

Educational project — Full Cycle course challenge.
