---
name: timezone
description: Move a DETONATE REAL man's time zone, when he has moved or it was set wrong. Runs at once or books it for the next allowed time. Shows the change and waits for a yes.
---

# DETONATE move a man's time zone (REAL)

1. Load the `detonate:rules` skill and follow it for the rest of the session. Run `whoami` (`mcp__plugin_detonate_detonate-real__whoami`): it must say REAL. If not, stop and say so.
2. Call `get_procedure` with `name: "timezone"`.
3. If its `contract_version` is not `1`, stop and say exactly: "This plugin is out of date. Run /plugin marketplace update detonate-claude, then /reload-plugins." Do nothing else.
4. Follow the steps it returned, in order. Nothing is written without a yes.
