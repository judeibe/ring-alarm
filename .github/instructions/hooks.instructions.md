---
applyTo: "**/src/hooks/**"
---
# Quoin • Custom Hook Conventions

- File name must mirror hook name, e.g. `useDebounce.ts`.  
- First line comment: purpose + example usage.  
- Never call other hooks conditionally; expose cancellable async helpers where needed.  
- Memoize expensive calculations with `useMemo`; avoid stale closures via deps array.  
