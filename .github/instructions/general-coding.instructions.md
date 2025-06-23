---
applyTo: "**/*.ts,**/*.tsx,**/*.js,**/*.jsx"
---
# Quoin • General Coding Standards

- **Language** : Prefer **TypeScript 5.x** with `strict` mode enabled.  
- **Modules** : Use **ES2020** imports/exports; no default exports except `next.config.*`.  
- **Style** : 2-space indentation, single quotes, trailing commas, Prettier enforced.  
- **Naming** :  
  - `PascalCase` for types, interfaces, React components.  
  - `camelCase` for variables/functions.  
  - Prefix private class fields with `#`.  
- **Error handling** : Always wrap async I/O in `try / catch` and surface domain-specific errors.  
- **Comments** : Start file-level descriptions with `/// <file-overview>`.  
- **Dependency boundaries** : No direct imports across **feature modules** (`src/features/*`)—use exported facades.  
- **AI notice** : Append `// Generated-by-AI, validated by dev.` to code you accept from Copilot.  
