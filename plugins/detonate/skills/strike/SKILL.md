---
name: strike
description: Undo one of a DETONATE REAL man's strikes, by its day. Never spends his free pass. Shows the change and waits for a yes.
---

# DETONATE undo a man's strike (REAL)

1. Load the `detonate:rules` skill and follow it for the rest of the session. Run `whoami` (`mcp__plugin_detonate_detonate-real__whoami`): it must say REAL. If not, stop and say so.
2. Call `get_procedure` with `name: "strike"`.
3. If its `contract_version` is not `1`, stop and say exactly: "This plugin is out of date. Run /plugin marketplace update detonate-claude, then /reload-plugins." Do nothing else.
4. Follow the steps it returned, in order. Nothing is written without a yes.
