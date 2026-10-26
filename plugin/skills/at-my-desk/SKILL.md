---
name: at-my-desk
description: The desk list for "All of my Irons in the Fire!". Use when the user says "put that on my desk list", "save that for my desk", "add it to the sitting-at-my-desk bucket", "I'm at my desk", "I'm parked", "desk time", "what do I need to do on my laptop?", "I finished number one", "next", or "skip that one". Saves screen-only tasks from any iron, then walks the user through them in a 15-minute session, one step at a time, checking each off, spoken or typed.
---

# At My Desk — the 15-minute desk session

Some things can only be done at a screen: installing something, signing a form, uploading a file, setting up a Project. When the user is driving, on the phone, or just thinking out loud, those things go on the **desk list**. When they sit down, this skill turns the list into a short, guided session across all their irons.

Load the Irons Map as the `fire-up` skill describes. The list lives in `desk-list` (an older `later-list` counts too; move its items over).

## 1. Adding to the desk list

Triggers: "put that on my desk list," "save that for my desk," "add it to the sitting-at-my-desk bucket," or anything the plugin saves because it needs a screen.

For each item, save:
- `task`: a short, plain name ("Install version 0.8.0")
- `iron`: which iron it belongs to
- `steps`: the concrete steps, written so someone can follow them without remembering the conversation
- `minutes`: an honest estimate (round up; 1, 2, 3, 5, 10, or 15)
- `priority`: high if it unblocks something or has a deadline, otherwise normal
- `added`: date

Read it back in one line: "Got it, on your desk list: install version 0.8.0, about 3 minutes."

## 2. Starting a desk session

Triggers: "I'm at my desk," "I'm parked," "desk time," "what do I need to do on my laptop?"

1. Pick items for **about 15 minutes**: high priority first, then oldest first, until the next item would go over 15. If one item is longer than 15 minutes, offer it alone.
2. Give the plan in one or two lines: "You've got 6 things on your desk list. Here are 4 that fit in about 14 minutes, across the plugin and the food truck."
3. Show the numbered list (typed) or say the count and first item (spoken).
4. Ask: "Ready for number one?"

Typed format:
```
Desk session, about 14 minutes:
1. Install version 0.8.0 (plugin, 3 min)
2. Turn on the website (plugin, 2 min)
3. Email the commissary about Saturday (food truck, 4 min)
4. Pay the booth fee (food truck, 5 min)
```

## 3. Walking through it, one at a time

For the current item:
- Give the steps one or two at a time, not all at once. Wait for the user before going on.
- In voice-friendly mode, say each step in a sentence and never ask them to read the screen to you; ask what they see only if they're stuck.
- If they get stuck, help right there, then continue.

The user drives the pace with plain words:
- **"Done," "finished number one," "got it":** check it off ("Nice, that's one down."), remove it from `desk-list`, record it on that iron (and update its `last-touched`), then: "Ready for number two? It's turning on the website, about 2 minutes."
- **"Skip," "not now":** leave it on the list and move on.
- **"Later," "tomorrow":** leave it on the list and move on; don't ask why.
- **"Stop," "I'm done for now":** stop warmly (see section 4).

Keep it to one question at a time. Celebrate briefly; don't gush.

## 4. Wrapping up

When the time is up or the user stops:
- Say what got done, in one line: "Three down in 12 minutes. Nice."
- Say what's left, in one line: "Two more are waiting on your desk list for next time."
- Save the map (`desk-list`, `last-touched`, `last-seen`).

Never guilt about leftovers. Unfinished items simply roll to the next session.

## Rules

- The desk list spans all irons; it's the one place for "things I need a screen for."
- Never do anything on the user's behalf that the step asks them to do (sign in, pay, send, submit). Guide; don't act.
- If the user is driving, never start a desk session. Offer it for when they're parked.
