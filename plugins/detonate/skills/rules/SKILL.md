---
name: rules
description: The house rules and GoHighLevel field map for DETONATE REAL, served by DETONATE itself. Load this BEFORE any call to a DETONATE (detonate-real) or GoHighLevel (leadconnector) tool, and before running /detonate:intake, /detonate:csv, /detonate:reconcile, /detonate:sweep, /detonate:correct, /detonate:reinstate, /detonate:clear or /detonate:timezone. Follow it for the rest of the session.
---

# DETONATE REAL (production): house rules

This plugin connects Claude Code to **DETONATE REAL**, the production app at `https://detonate.me`. These are real men. Every account made and every email sent here is real.

The DETONATE tools are `mcp__plugin_detonate_detonate-real__<tool>`; DETONATE's rules name them by `<tool>` alone. The GoHighLevel tools are `mcp__plugin_detonate_leadconnector__<tool>`.

## First, every session

1. Run `whoami`. It must say REAL (production). If it says anything else, stop and tell the person. Do nothing else.
2. Call `get_procedure` with `name: "rules"`. If its `contract_version` is not `1`, stop and say exactly: "This plugin is out of date. Run /plugin marketplace update detonate-claude, then /reload-plugins." Do nothing else.
3. Follow every step it returns for the rest of the session. They are the house rules and the GoHighLevel field map, kept in one place by DETONATE. When a skill or a procedure says "the field map", it means the field map in that answer.
4. Keep the `rules_key` from that answer. Every DETONATE tool that creates, changes or emails needs it. If a tool says `rules_not_loaded`, call `get_procedure` with `name: "rules"` again and carry on.

## If something goes wrong

Tell the person what the tool said, word for word, including its `fix`. Then stop. The full card is in the DETONATE connector guide: https://detonate-connector-mcp.vercel.app
