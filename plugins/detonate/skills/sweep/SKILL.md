---
name: sweep
description: The daily check on DETONATE REAL cohorts. Men not set up 24 hours after their invitation, men inactive 2 days or more, new REBORN picks, then the GoHighLevel check. Proposes resends and waits for a yes.
---

# DETONATE daily sweep (REAL)

1. Load the `detonate:rules` skill and follow it for the rest of the session. Run `whoami` (`mcp__plugin_detonate_detonate-real__whoami`): it must say REAL. If not, stop and say so.
2. Call `get_procedure` with `name: "sweep"`.
3. If its `contract_version` is not `1`, stop and say exactly: "This plugin is out of date. Run /plugin marketplace update detonate-claude, then /reload-plugins." Do nothing else.
4. Follow the steps it returned, in order. Report counts first, then the men. Send nothing without a yes.
