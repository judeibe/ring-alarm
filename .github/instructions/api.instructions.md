---
applyTo: "**/src/pages/api/**,**/src/app/api/**"
---
# Quoin • API Route Standards

- Use `export const runtime = "edge"` unless the route needs Node APIs.  
- Validate request bodies with **Zod**; respond with typed **NextResponse** objects.  
- Always set an explicit HTTP status; include `problemDetails` on errors.  
- No direct DB calls—use service layer in `src/server/**`.  
- Enable CORS only for domains in `env.NEXT_PUBLIC_ALLOWED_ORIGINS`.  
