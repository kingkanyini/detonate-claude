---
name: reconcile
description: Check one DETONATE REAL cohort against the GoHighLevel contacts filed under its number (Detonate Cohort). Lists men in both, missing from DETONATE, not in GoHighLevel, mismatched and late. Changes nothing.
---

# DETONATE check against GoHighLevel (REAL)

1. Load the `detonate:rules` skill and follow it for the rest of the session. Run `whoami` (`mcp__plugin_detonate_detonate-real__whoami`): it must say REAL. If not, stop and say so.
2. Call `get_procedure` with `name: "reconcile"`.
3. If its `contract_version` is not `1`, stop and say exactly: "This plugin is out of date. Run /plugin marketplace update detonate-claude, then /reload-plugins." Do nothing else.
4. Read the Detonate Cohort field from the field map in the rules. If its key still says `TO FILL`, find the field by its label and tell the person which field you read.
5. Follow the steps it returned, in order.
