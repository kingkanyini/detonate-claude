---
name: csv
description: Load men into DETONATE REAL from a CSV export (the GoHighLevel export) the person put in the folder Claude Code was started in. One run per cohort number, accounts made with invitations held for Approve. Use when the person drops a CSV in the folder or asks to load men from a file.
---

# DETONATE load from a CSV (REAL)

1. Load the `detonate:rules` skill and follow it for the rest of the session. Run `whoami` (`mcp__plugin_detonate_detonate-real__whoami`): it must say REAL. If not, stop and say so.
2. Call `get_procedure` with `name: "csv"`.
3. If its `contract_version` is not `1`, stop and say exactly: "This plugin is out of date. Run /plugin marketplace update detonate-claude, then /reload-plugins." Do nothing else.
4. Read the field map in the rules. The CSV's columns are matched to the map's **CSV column** labels, any case. Never guess a column.
5. Read only a CSV in the folder Claude Code was started in. Never write it, or any file made from it, anywhere else. Never paste a whole row into the chat.
6. Follow the steps it returned, in order, one at a time. Never skip a yes the steps ask for.
