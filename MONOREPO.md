
# Monorepo Structure Documentation

> **Note:** This documentation should be updated as the monorepo evolves. For questions or contributions, see the main `README.md` or contact the maintainers.

This document provides an overview of the structure and shared packages in the `ring-alarm` monorepo. It is intended to guide development, onboarding, and maintenance.

## Table of Contents

- [Monorepo Structure Documentation](#monorepo-structure-documentation)
  - [Table of Contents](#table-of-contents)
  - [Top-level Structure](#top-level-structure)
  - [Relationships](#relationships)
  - [Package Details](#package-details)
    - [apps/api](#appsapi)
    - [apps/web](#appsweb)
    - [packages/api](#packagesapi)
    - [packages/eslint-config](#packageseslint-config)
    - [packages/jest-config](#packagesjest-config)
    - [packages/typescript-config](#packagestypescript-config)
    - [packages/ui](#packagesui)
  - [Tooling](#tooling)

## Top-level Structure

- **apps/**: Contains deployable applications.
  - **api/**: Backend service (NestJS). Handles business logic, API endpoints, and server-side operations.
  - **web/**: Frontend application (Next.js). Provides the user interface and client-side logic.
- **packages/**: Contains shared and reusable code.
  - **api/**: Shared API types, DTOs, and entities for use across backend and frontend.
  - **eslint-config/**: Shared ESLint configurations for consistent code linting.
  - **jest-config/**: Shared Jest configurations for unit and integration testing.
  - **typescript-config/**: Shared TypeScript configurations for all packages and apps.
  - **ui/**: Shared React UI components (e.g., Button, Card, Code) for use in frontend apps.
- **Other Key Files**:
  - `pnpm-workspace.yaml`: Defines workspace packages for pnpm.
  - `turbo.json`: Turborepo configuration for task running and caching.
  - `tsconfig.json`: Base TypeScript config.
  - `README.md`: Project overview and instructions.

## Relationships

- Apps depend on shared packages for types, configs, and UI components.
- Shared configs (eslint, jest, tsconfig) ensure consistency across all packages and apps.
- The UI package is intended for use in the web app and potentially other React-based apps.

## Package Details

### apps/api

- **Type**: NestJS backend
- **Purpose**: Handles API requests, business logic, and server-side operations.
- **Depends on**: packages/api, packages/typescript-config, packages/jest-config, packages/eslint-config

### apps/web

- **Type**: Next.js frontend
- **Purpose**: Provides the user interface and client-side logic.
- **Depends on**: packages/ui, packages/api (for types), packages/typescript-config, packages/jest-config, packages/eslint-config

### packages/api

- **Purpose**: Provides shared API types, DTOs, and entities for both backend (NestJS) and frontend (Next.js) to ensure type safety and consistency.
- **Used by**: apps/api, apps/web

### packages/eslint-config

- **Purpose**: Centralized ESLint configuration for code quality and consistent linting rules across all apps and packages.
- **Used by**: apps/api, apps/web, all packages

### packages/jest-config

- **Purpose**: Centralized Jest configuration for unit and integration testing, ensuring consistent test setup and behavior.
- **Used by**: apps/api, apps/web, all packages

### packages/typescript-config

- **Purpose**: Centralized TypeScript configuration for type safety and consistent TS settings across the monorepo.
- **Used by**: apps/api, apps/web, all packages

### packages/ui

- **Purpose**: Shared React UI components (e.g., Button, Card, Code) for use in frontend applications.
- **Used by**: apps/web (and any future React-based apps)

## Tooling

- **pnpm**: Used for managing dependencies across the monorepo.
- **Turborepo**: Used for task running, caching, and orchestrating builds/tests.
- **TypeScript**: Used throughout for type safety.
- **Jest**: Used for testing.
- **ESLint**: Used for linting.
