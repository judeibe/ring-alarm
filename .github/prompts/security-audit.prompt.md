---
mode: "agent"
tools: ['codebase', 'terminalLastCommand']
description: "Audit & remediate npm vulnerabilities."
---

Run a full dependency scan with **#npmAudit**.

Steps:
1. Execute `npmAudit` on the current workspace.  
2. Summarize all *high* / *critical* CVEs with package, version, and advisory URL.  
3. Propose `npm i <pkg>@latest --save-exact` commands for each finding.  
4. Use **#terminalLastCommand** to run fixes automatically after user confirmation.  
5. Verify zero remaining vulnerabilities by re-running `npmAudit`.  

Output:
- Markdown table of issues → fixes.  
- Patch commands ready to run.
