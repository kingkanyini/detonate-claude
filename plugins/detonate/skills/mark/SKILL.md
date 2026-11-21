---
name: mark
description: Mark a stuck wordless step done for a DETONATE REAL man who did the work and whose app would not record it. Shows the evidence first and waits for a yes.
---

# DETONATE mark a stuck step done (REAL)

1. Load the `detonate:rules` skill and follow it for the rest of the session. Run `whoami` (`mcp__plugin_detonate_detonate-real__whoami`): it must say REAL. If not, stop and say so.
2. Call `get_procedure` with `name: "mark"`.
3. If its `contract_version` is not `1`, stop and say exactly: "This plugin is out of date. Run /plugin marketplace update detonate-claude, then /reload-plugins." Do nothing else. If `get_procedure` answers that there is no `mark` procedure, stop and say exactly: "The connector has not got the mark procedure yet. Type /mcp, pick plugin:detonate:detonate-real, press Reconnect, then try again." Do nothing else.
4. Follow the steps it returned, in order. Nothing is written without a yes.
