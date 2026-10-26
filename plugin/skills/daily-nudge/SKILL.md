---
name: daily-nudge
description: Sends the user's daily nudge for "All of my Irons in the Fire!". Use when a scheduled task says "Run the daily-nudge skill", or when the user asks "nudge me", "what should I look at today", or "give me my daily nudge". Writes one short, warm message about what's waiting across the user's irons in the fire.
---

# Daily Nudge — a short, warm reach-out

This usually runs from the user's scheduled task, with nobody in the chat yet. The message is what they'll see in their notification, so it has to stand on its own and read well on a phone.

## 1. Load the map and the clock

- Load the Irons Map as the `fire-up` skill describes (memory `/areas/irons-in-the-fire.md`, else `irons-in-the-fire.md`).
- Work out the current local time as in `fire-up` section 2, using the map's `timezone`.
- If there's no map, write one line: "Morning! Open Claude and say 'fire up' whenever you're ready to set up your irons in the fire." Then stop.

## 2. Decide what to say

Look at, in this order:
1. Snoozes whose `snooze-until` has arrived
2. `last-session`: where the user left off and the next step
3. Irons that have started cooling, leading with the iron's `why`
4. Saved sparks waiting on an iron

Pick **at most two** things. Fewer is better.

## 3. Write the nudge

Keep it to 2 to 4 short lines:
- A greeting for the time of day, using the user's name. Sign off with the nickname (`assistant-name`) if there is one.
- If it's been a day or more since `last-seen`, say how long, warmly ("It's been 3 days").
- The one or two things, each in a single line. Lead with the why for a cooling iron.
- One easy next step or question that invites them back.

Example:
> Good morning, Ed. Last time we left off picking the breakfast tacos for the farmers market. And the hang gliding trip's been cooling for 2 weeks, the one you've wanted for years. Want to put 15 minutes into either today?
> — ChatBro

If nothing is waiting:
> Good morning, Ed. Nothing's gone cold. Every iron is right where you left it. What's on your mind today?

## Rules

- Never guilt. No "you haven't," "you forgot," or "you should." Cooling irons are mentioned as options, not obligations.
- Don't change irons, keywords, or statuses from a nudge. Only save `last-nudged` (date and time) in the map.
- If `last-seen` is within the last 3 hours, the user is already active today: keep it to one line, or skip the nudge.
- Never include passwords, account details, or anything sensitive from the irons in the message.
- **Texted or emailed nudges travel through outside services** (Zapier and its texting provider, email providers). In those, never mention how the user describes themselves (`who-i-am`), health details, energy level, or private notes. If `nudge-generic: on`, don't name any irons: "Good morning, Ed. Two things are waiting in the fire whenever you're ready. — ChatBro"
