# Testing Strategy

The private project includes Vitest, Testing Library, and Playwright setup. The recommended strategy is layered.

## Unit Tests

Target pure utilities and formatting logic:

- WhatsApp phone normalization;
- WhatsApp URL builder;
- Paddle environment helpers;
- date/time formatting;
- KPI calculation helpers.

## Component Tests

Target reusable UI and dashboard-specific widgets:

- KPI cards;
- revenue chart empty/loading states;
- appointment dialogs;
- support dialog;
- subscription banners;
- email verification banner.

## Integration Tests

Target hooks and Supabase data access with mocks:

- appointment CRUD hook behavior;
- client creation flow;
- inventory color retrieval;
- subscription status query;
- profile loading.

## E2E Tests

Target full user journeys through Playwright:

- register/login/logout;
- onboarding completion;
- create client;
- create appointment;
- complete appointment;
- add inventory color;
- open public catalog;
- start upgrade checkout;
- open customer portal.

## Critical Tests to Add Next

1. Cross-tenant RLS denial tests.
2. Paddle webhook signature verification tests.
3. Subscription cancellation/resume regression tests.
4. Public catalog data exposure tests.
5. Email queue failure/retry tests.
