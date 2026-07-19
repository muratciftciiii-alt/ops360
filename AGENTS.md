# OPS360 Agent Guide

## Project Overview

OPS360 is a Turkish-language operations management interface for personnel, tasks, deliveries, installations, calendars, documents, notifications, and operational reporting. Sales and accounting are intentionally outside the product scope.

## Technology

- TanStack Start with React 19 and TypeScript
- TanStack Router file-based routing
- Tailwind CSS 4 plus project design tokens in `src/styles.css`
- Lucide React icons
- Netlify deployment through the TanStack Start Vite plugin

## Architecture

- `src/routes/`: Page routes. Module folders expose their own index routes.
- `src/components/layout/`: Shared application shell, sidebar, and top navigation.
- `src/components/ui/`: Reusable visual primitives and page patterns.
- `src/features/`: Feature-level compositions such as the dashboard.
- `src/lib/backend/`: Provider-neutral contracts for future authentication, data, permissions, and AI integrations.
- `public/`: Static assets.

## Conventions

- Use Turkish for all user-facing copy.
- Keep sales and accounting functionality out of the application.
- Use PascalCase for components and camelCase for hooks and functions.
- Prefer reusable components over route-local duplication.
- Keep colors, spacing, shadows, and theme behavior in CSS variables.
- Preserve light and dark mode support when adding interfaces.
- Ensure every new page works with the responsive `AppShell`.
- Keep backend integrations behind interfaces in `src/lib/backend` so providers can be replaced without rewriting UI code.

## Non-Obvious Decisions

- Dashboard values are presentation placeholders only; no business calculations are implemented.
- Module pages intentionally use a polished empty state until a persistent data source is connected.
- Theme preference is the only locally persisted UI preference and is stored in `localStorage`.
- Authentication controls are visual and validation-ready, but no identity provider is connected yet.

## Commands

- `npm run dev`: Start the local Vite development server.
- `npm run build`: Create the production build used by Netlify.
