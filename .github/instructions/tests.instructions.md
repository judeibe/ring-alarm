---
applyTo: "**/*.test.ts,**/*.test.tsx,**/*.spec.ts,**/*.spec.tsx"
---
# Quoin • Testing Standards

- Framework: **Vitest** for unit tests, **Playwright** for e2e.  
- Follow **AAA** pattern (Arrange-Act-Assert).  
- Mock external services with **msw**; never hit real APIs in CI.  
- Name test suites after the unit under test; keep files alongside source with `.test.ts`.  
