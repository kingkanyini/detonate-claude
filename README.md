# DETONATE for Claude Code

The DETONATE connector for Otherside admins. It lets Claude bring men into DETONATE from GoHighLevel or a CSV, check a cohort against GoHighLevel, and run the daily sweep. Claude acts as you, signed in with your own DETONATE admin login.

This repo holds no passwords, keys or tokens. On its own it can do nothing: only an Otherside admin who has been switched on for the connector can sign in.

## Set it up (once)

You need Claude Code and git.

1. In Claude Code, type:
   ```
   /plugin marketplace add kingkanyini/detonate-claude
   /plugin install detonate@detonate-claude
   ```
2. Type `/mcp`, pick **plugin:detonate:detonate-real**, choose **Authenticate**, and sign in with your DETONATE admin login in the browser. Press **Approve**.
3. Still in `/mcp`, pick **plugin:detonate:leadconnector** and sign in to GoHighLevel the same way.
4. In Claude's privacy settings, switch off **Help improve Claude**.
5. Turn on updates: `/plugin`, then **Marketplaces**, pick **detonate-claude**, choose **Enable auto-update**.

On Windows, if step 1 says it can't reach GitHub, run this once in a terminal and try again: `setx CLAUDE_CODE_PLUGIN_PREFER_HTTPS 1`, then restart Claude Code.

Before you touch real men, do the practice lesson on staging (ask Kanyini for the Practice folder).

## Use it

Open Claude Code in any folder and type one of these:

| Type | What happens |
|---|---|
| `/detonate:intake` | Brings a cohort's men in from GoHighLevel |
| `/detonate:csv` | Loads men from a GoHighLevel CSV export you saved in the folder you opened Claude in |
| `/detonate:reconcile` | Checks a cohort in DETONATE against GoHighLevel. Changes nothing |
| `/detonate:sweep` | The daily check: who hasn't set up, who's gone quiet, new REBORN picks |

Claude asks before each DETONATE tool the first time. Reading is safe to allow for the session. Answer every change each time.

## What keeps it safe

- Claude checks it is on DETONATE REAL and signed in as you before anything else.
- Nothing changes until Claude has shown you what it will do and you've said yes. Risky changes need a second yes.
- Accounts are made with invitations **held**. Nobody gets an email until someone presses **Approve** on the DETONATE page. At most 100 invitations go out an hour.
- One email per man per 15 minutes, unless you say yes twice.
- A man already in DETONATE is never made twice.
- GoHighLevel is read only for Claude.
- If Claude or the connector is down, the DETONATE admin pages work as always.

## Updates

If Claude says "This plugin is out of date", type `/plugin marketplace update detonate-claude`, then `/reload-plugins`.
