---
name: my-data
description: Privacy and consent for "All of my Irons in the Fire!". Use when the user says "what do you know about me?", "what have you saved?", "show my irons map", "export my data", "forget everything", "delete my data", "I don't want to use this anymore", "stop remembering", "turn off the plugin", "restore my irons", or "I'm back, here's my export". Also used for the disclosure at first-time setup and the 30-day consent check-in.
---

# My Data — see it, keep it, or forget it

All of my Irons in the Fire! remembers things between chats so it can pick up where the user left off. The user should always know what's saved, agree to it, and be able to see it or erase it in one step.

## The disclosure (first-time setup, before saving anything)

Say it in plain words, in three or four short lines:

"Before we start, here's what I'll remember so I can pick up where we left off: your name, the irons in your life and a few keywords for each, why each one matters to you, notes and ideas you ask me to save, and when we last talked about each one. I only save things you tell me or confirm, not our whole conversations. It's kept in your Claude account [or: in a file in your folder], and nobody else sees it; it isn't sent to the plugin's creator. You can say 'what do you know about me' to see it, or 'forget everything' to erase it, anytime. Okay to remember these things?"

- **Yes:** save `consent: yes` with today's date and continue setup.
- **No:** say "No problem. I'll help you right here without saving anything." Work in the current chat only; don't create a map. Don't ask again this session.

**Where it's saved.** Ask once, as part of the disclosure, only when both options exist: "I can keep it in your Claude memory, or in a file in your folder that you can open yourself. Which do you prefer?" Default to Claude memory when there's no folder (for example, in a regular chat). Save the choice as `storage`.

## "What do you know about me?"

Show the whole map in plain words, not raw fields: their name and nickname choice, each iron with its keywords, why, notes, sparks, and status, the desk list, the nudge settings, and the dates. Then: "Want to change anything, or have me forget any of it?"

**Export:** if they ask for a copy, give them the full map as a file they can keep, named `irons-in-the-fire-export-YYYY-MM-DD.md`, with a short note at the top: "Your All of my Irons in the Fire! export. Keep it anywhere. To pick back up, start a chat, say 'restore my irons,' and share this file."

## Forgetting

**One thing:** "Forget the hang gliding trip," "forget that note." Confirm in one line ("Remove the hang gliding trip and everything saved with it?"), then remove it entirely. Don't leave a "used to" trace.

**Everything:** "Forget everything," "delete my data," "I don't want to use this anymore."
1. **Offer the export first, every time:** "Before I erase anything, want a copy to keep? If you ever miss it, you can bring it back and pick up right where you left off." If yes, create the export (above) and hand it over before going further.
2. Confirm once, in plain words: "This erases everything I've saved for All of my Irons in the Fire!: your irons, whys, notes, desk list, and settings. Without a copy, it can't be undone. Go ahead?"
3. On a clear yes: delete the irons map (the memory file or the file in their folder).
4. If they have a daily nudge, ask separately: "Want me to stop your daily nudge too?" On yes, delete that scheduled task.
5. Confirm what was erased, in one line. If they want to stop using the plugin entirely, tell them they can remove it under **Customize → Plugins**.

Never delete anything without the user's clear yes in this conversation.

## Restoring from an export

"Restore my irons," "I'm back," or the user shares an export file:
1. Read the export the user provides (only that file).
2. Show a short summary: "This has 6 irons, your desk list, and your settings from March 3. Restore it?"
3. Give the disclosure again and ask permission (it's a fresh start).
4. On yes, rebuild the map from the export, set `consent` to today, and greet them: "Welcome back. Everything's right where you left it."
5. If they had a daily nudge, offer to set it up again; it isn't restored automatically.

## The 30-day consent check-in

The `fire-up` skill asks about every 30 days: "Still okay with me remembering your irons between chats?" Yes updates the `consent` date. No runs "Forgetting: Everything" above.

## Rules

- Save only what the user tells you or confirms for this plugin. Never copy whole conversations, and never read other memory files, other chats, or other files to fill in the map.
- Nothing is ever sent to Mindful Tech Projects.
- Be plain and calm about privacy. No legal jargon, no pressure either way.
