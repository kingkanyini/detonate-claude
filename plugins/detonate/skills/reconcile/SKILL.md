---
name: reconcile
description: Check one DETONATE REAL cohort against the GoHighLevel contacts filed under its number (Detonate Cohort Number). Lists men in both, missing from DETONATE, not in GoHighLevel, mismatched and late. Changes nothing.
---

# DETONATE check against GoHighLevel (REAL)

1. Load the `detonate:rules` skill and follow it for the rest of the session. Run `whoami` (`mcp__plugin_detonate_detonate-real__whoami`): it must say REAL. If not, stop and say so.
2. Call `get_procedure` with `name: "reconcile"`.
3. If its `contract_version` is not `1`, stop and say exactly: "This plugin is out of date. Run /plugin marketplace update detonate-claude, then /reload-plugins." Do nothing else.
4. Read the cohort field from the field map in the rules: `contact.detonate_cohort_number` (Detonate Cohort Number), found by its id as the map says.
5. Follow the steps it returned, in order.
