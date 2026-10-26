# Irons Map format

One Markdown file holds the user's whole map. Keep it human-readable — the user may edit it by hand. Preserve anything the user wrote, even if it doesn't match this format.

```markdown
# All of my Irons in the Fire!

name: Ed
assistant-name: ChatBro          # what the user calls Claude; blank = Claude
timezone: America/Chicago
last-seen: 2026-10-26 09:23      # local time, updated at natural stopping points
last-session:
  iron: Food Truck
  left-off: deciding the breakfast taco lineup for the farmers market
  next: pick two tacos and price them
  summary:
    - Farmers market is Saturdays, 7 AM to noon; booth fee is paid
    - Leaning toward chorizo-and-egg plus a veggie option
    - Still open: pricing, and whether to offer coffee
last-opener: "What's on your mind?"
nickname-checked: 2026-10-26     # last time we asked if the nickname still fits (every ~30 days)
nudge-time: "08:30"              # daily nudge time, or none
nudge-days: weekdays             # every day | weekdays | custom list
nudge-task: "Irons in the Fire: daily nudge"
last-nudged: 2026-10-26 08:30
voice-style: off               # on = always talk in voice-friendly style
update-checked: 2026-10-26      # last time we checked GitHub for a newer version
later-list:                     # saved while driving or on a phone, for when there's a screen
  - Set up the hang gliding Project
review-every: monthly          # every two weeks | monthly | never
last-review: 2026-10-01
away-reminder: scheduled task   # scheduled task | next session only

## Active irons

### Food Truck
- type: side project
- why: my ticket to retiring rich
- keywords: food truck, menu, permits, commissary, catering
- last-touched: 2026-10-26 06:15
- cooling-after: 14 days
- snooze-until:
- forge: (none)                # or: Claude Project "Food Truck"
- sparks:
  - 2026-10-20: breakfast tacos for the Saturday farmers market
- notes:

### Day Job
- type: work
- keywords: reports, Sam, quarterly review
- last-touched: 2026-10-25 17:40
- cooling-after: 30 days

### Home & Car
- type: personal
- keywords: oil change, tires, honey-do list, county letter
- last-touched: 2026-10-10 20:05
- cooling-after: 21 days
- snooze-until: 2026-10-28

## Resting irons
(paused on purpose — not nagged about until snooze-until or the user brings them up)

### Hang Gliding Trip
- keywords: hang gliding, trip, gear
- resting-since: 2026-10-20

## Out of the fire (archived)
(kept for history; only revived if the user asks)

### Littlecoin
- archived: 2026-09-15
```

Field notes:
- `last-seen` replaces the 0.1.0/0.2.0 `last-check-in` (date only). If a map has `last-check-in` and no `last-seen`, read it as that date at noon and write `last-seen` from then on.
- `last-touched` is a date and time (local), so the irons glance can show hours for anything under a day. An older date-only value is read as noon that day.
- `timezone` is an IANA name (America/Chicago). Update it if the user says they've moved or are traveling.
- `last-session` is one short snapshot, overwritten each time. It's for picking up, not a history. `summary` is 2 to 4 lines, written in plain words the user would recognize.
- `why` is the user's own words for why the iron matters. Use it when an iron is cooling. Leave it blank if they skip it.
- `sparks` are ideas the user had while working on a different iron. Bring them up next time this iron is worked on, then clear the ones the user has dealt with.
- `type` is free text the user picks (work, side project, personal, family, volunteer, travel…).
- `cooling-after` defaults to 14 days. Users can change it per iron ("don't bug me about the car for a month").
- `snooze-until` is set by the nudge choices: a day = +1, a few days = +3, a week = +7.
- `forge` records the Claude Project name once an iron is promoted.
- Dates are YYYY-MM-DD.
