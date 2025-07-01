---
applyTo: "**/src/components/**"
---
# Quoin • UI Component Guidelines

- Library stack: **shadcn/ui**, **lucide-react**, **TailwindCSS**.  
- One component per file; colocate variant sub-components.  
- Keep components ≤200 LOC; move logic to hooks if bigger.  
- Accept a minimal, flat props object—group complex props into typed objects.  
- Export **stories** in the same folder (`*.stories.tsx`) for Storybook.  
