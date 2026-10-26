---
name: irons-review
description: Periodic review of everything in "All of my Irons in the Fire!". Use when the user says "review my irons", "what's in the fire", "show my irons", "clean up my buckets", "what does my organization look like", or when the review period set in the Irons Map has passed. Also handles adding, renaming, merging, resting, archiving, and reviving irons.
---

# Irons Review — keep the fire organized

Load the Irons Map the same way the `fire-up` skill does (memory `/areas/irons-in-the-fire.md`, else `irons-in-the-fire.md` in the working folder). Format: `../fire-up/references/irons-map-format.md`.

## When to run

- The user asks.
- During `fire-up`, if `last-review` is older than `review-every`, offer once: "It's been about a month since we looked at all your irons. Quick review now, or later?" Respect "later" and don't ask again this session.

## The review (keep it short — aim for under two minutes of the user's time)

1. Show a compact snapshot, hottest first:
   - **Glowing** (touched recently)
   - **Cooling** (past their cooling threshold)
   - **Resting**
   - Count of archived irons (don't list unless asked)
2. Ask one question at a time, starting with cooling irons. Lead with the iron's why when one is recorded: "The hang gliding trip's been cooling. You said it's the trip you've wanted for years. Put some heat to it, let it rest, or pull it out of the fire for now?"
3. For any glowing iron whose why is blank or may be out of date, ask lightly once: "Still the same why behind this one?" Skip if the user seems busy.
4. Mention any uncaught sparks waiting on an iron, if there are any.
5. Then: "Any new irons in the fire that aren't on here?" Add new irons the user names, and ask for their why.
6. Then: "Anything here you're done with or out of energy for?" Pull out of the fire (archive) what they choose. Being out of energy is a fine reason; remind them it stays safe and ready for its next chance at some heat.
7. If the user gave Claude a nickname and hasn't been asked in 30+ days, ask: "Still happy calling me [nickname]?" Also check the daily nudge: "Still want your nudge at [time], or change it?" Update the map (and the scheduled task, with a yes).
8. Offer to promote any iron that is running hot (lots of activity, documents, collaborators) using `give-it-a-forge`.
9. Update `last-review` and summarize the changes in one or two lines.

## Edits the user can ask for anytime

- **Add** an iron: name, type, a few keywords.
- **Rename** or **merge** two irons (combine keywords; keep the user's notes from both).
- **Move** a keyword between irons.
- **Change cooling time** for an iron.
- **Add or update an iron's why.**
- **Rest** an iron (paused, not nagged) or **revive** a resting/archived one.
- **Archive** (out of the fire). **Delete** only if the user explicitly says delete, and confirm once first.

## Tone

Encouraging, never guilt-inducing. Having many irons is normal; the goal is that the ones the user cares about stay glowing and the rest are set down on purpose.
