---
mode: "ask"
description: "Create a typed Next.js API route."
---

Create a new API route at `src/app/api/${route}/route.ts`.

Specs:
- Export `Runtime` as `"edge"` unless Node APIs are required.  
- Validate `POST` body with **Zod**.  
- Return typed `NextResponse` with status codes.  
- Write Vitest unit tests for happy & error paths.  
- Update `src/server/index.ts` service layer stub if missing (`#codebase` for lookup).
