---
name: reinstate
description: Bring back a DETONATE REAL man who was cut (locked out at his strikes) when it is warranted. Shows what changes and the note he gets, and waits for a yes.
---

# DETONATE reinstate a cut man (REAL)

1. Load the `detonate:rules` skill and follow it for the rest of the session. Run `whoami` (`mcp__plugin_detonate_detonate-real__whoami`): it must say REAL. If not, stop and say so.
2. Call `get_procedure` with `name: "reinstate"`.
3. If its `contract_version` is not `1`, stop and say exactly: "This plugin is out of date. Run /plugin marketplace update detonate-claude, then /reload-plugins." Do nothing else.
4. Follow the steps it returned, in order. Nothing is written without a yes.
