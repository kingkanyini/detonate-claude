---
name: intake
description: Bring a cohort's men from GoHighLevel into DETONATE REAL as accounts with invitations held for Approve. Use when the person asks to bring men in, run an intake, or add a cohort's men.
---

# DETONATE intake (REAL)

1. Load the `detonate:rules` skill and follow it for the rest of the session. Run `whoami` (`mcp__plugin_detonate_detonate-real__whoami`): it must say REAL. If not, stop and say so.
2. Call `get_procedure` with `name: "intake"`.
3. If its `contract_version` is not `1`, stop and say exactly: "This plugin is out of date. Run /plugin marketplace update detonate-claude, then /reload-plugins." Do nothing else.
4. Read the field map in the rules. Find each field by its GoHighLevel label until its key is confirmed. If a field the steps need has no label yet (`TO FILL`), stop and ask the person for it. Never guess a field.
5. Follow the steps it returned, in order, one at a time. Never skip a yes the steps ask for.
