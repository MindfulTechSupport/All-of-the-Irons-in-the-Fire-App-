# Irons Map format

One Markdown file holds the user's whole map. Keep it human-readable — the user may edit it by hand. Preserve anything the user wrote, even if it doesn't match this format.

```markdown
# All of my Irons in the Fire!

name: Ed
review-every: monthly          # every two weeks | monthly | never
last-check-in: 2026-10-25
last-review: 2026-10-01
away-reminder: scheduled task   # scheduled task | next session only

## Active irons

### Food Truck
- type: side project
- why: my ticket to retiring rich
- keywords: food truck, menu, permits, commissary, catering
- last-touched: 2026-10-24
- cooling-after: 14 days
- snooze-until:
- forge: (none)                # or: Claude Project "Food Truck"
- sparks:
  - 2026-10-20: breakfast tacos for the Saturday farmers market
- notes:

### Day Job
- type: work
- keywords: reports, Sam, quarterly review
- last-touched: 2026-10-25
- cooling-after: 30 days

### Home & Car
- type: personal
- keywords: oil change, tires, honey-do list, county letter
- last-touched: 2026-10-10
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
- `why` is the user's own words for why the iron matters. Use it when an iron is cooling. Leave it blank if they skip it.
- `sparks` are ideas the user had while working on a different iron. Bring them up next time this iron is worked on, then clear the ones the user has dealt with.
- `type` is free text the user picks (work, side project, personal, family, volunteer, travel…).
- `cooling-after` defaults to 14 days. Users can change it per iron ("don't bug me about the car for a month").
- `snooze-until` is set by the nudge choices: a day = +1, a few days = +3, a week = +7.
- `forge` records the Claude Project name once an iron is promoted.
- Dates are YYYY-MM-DD.
