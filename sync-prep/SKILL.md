---
name: sync-prep
description: Prepare for or follow up on a recurring meeting using manually provided notes or summaries. Use when the user asks to prepare for a sync, get a meeting recap, or draft a status update. Produces a draft only — never posts or sends anything automatically.
allowed-tools: Read, Edit, Write
---

# Sync prep — meeting notes to status draft

Takes meeting context provided by the user and drafts a status update or prep doc.
Human reviews and sends manually every time — this skill does not post or send anything.

## When to use

- "Prepare me for the [X] sync" — before a recurring meeting
- "What happened in the last [X] sync" / "recap the [X] meeting" — after one
- "Draft a status update for [project]" — when grounded in real meeting notes

## Steps

1. **Get the meeting context.** Ask the user to paste or describe:
   - Meeting name / topic
   - Notes, summary, or action items from the meeting (or what they remember)
   - Any relevant background (decisions pending, blockers, attendees if relevant)

2. **Cross-check against local context** if available:
   - Check `~/Documents/drafts.md` for any prior drafts on the same topic
   - If the user has a project memory or journal file, read it and look for:
     - Anything that contradicts or adds nuance to what they just shared
     - Prior action items that may still be open

3. **Draft, don't send.** Write the result to `~/Documents/drafts.md`:
   - Newest entry on top
   - Include date and meeting name as a header
   - Plain prose, no heavy markdown — it gets copy-pasted into an email or a chat message
   - For a **prep** ask: draft what to raise, follow up on, or watch for
   - For a **recap/status** ask: draft the summary itself

4. **Surface new action items explicitly** — list them clearly at the end of the draft
   and ask the user whether to track them anywhere.

## Format for drafts.md entries

```
[YYYY-MM-DD] — [Meeting Name]
[Draft content here]

Action items surfaced:
- ...

---
```

## Notes

- No meeting platform integration — all input comes from the user directly
- If the user wants to add a memory/journal system later, update step 2 to reference it
- Always confirm the draft with the user before they copy-paste it anywhere
