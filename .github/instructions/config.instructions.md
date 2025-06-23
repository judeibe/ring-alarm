---
applyTo: "next.config.* ,tailwind.config.* ,tsconfig.json ,*.config.ts"
---
# Quoin • Configuration Files

- Keep all config in **ESM** format (`export default { … }`).  
- Group env var reads under `env` key; never inline `process.env` elsewhere.  
- Document every custom Webpack rule with a comment.  
- Tailwind: extend theme only—do not override core utilities.  
