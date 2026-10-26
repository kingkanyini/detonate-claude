---
name: clear
description: Clear a DETONATE REAL man's saved answers for the days he wants to redo (after a cohort move, or on his ask). Shows each day, how many saved answers, and what clearing it may knock on, and waits for a yes.
---

# DETONATE clear a day (REAL)

1. Load the `detonate:rules` skill and follow it for the rest of the session. Run `whoami` (`mcp__plugin_detonate_detonate-real__whoami`): it must say REAL. If not, stop and say so.
2. Call `get_procedure` with `name: "clear"`.
3. If its `contract_version` is not `1`, stop and say exactly: "This plugin is out of date. Run /plugin marketplace update detonate-claude, then /reload-plugins." Do nothing else.
4. Follow the steps it returned, in order. Nothing is cleared without a yes.
