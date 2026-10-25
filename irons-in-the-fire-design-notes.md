# All of my Irons in the Fire! — Design Notes
*Mindful Tech Projects · started 2026-10-25 · owner: Ed Vita*

These notes record why the plugin works the way it does, so future versions keep the original intent.

## Origin

The idea started as a security question ("ask me which elementary school I graduated from") to keep a Claude session private if a laptop was left open. A Claude plugin can't lock anything: anyone at an unlocked computer can read the chat history and the plugin itself. Screen locks, short auto-lock timers, and separate accounts or browser profiles solve that.

The real need underneath was **keeping the different parts of life from bleeding together**. That became this plugin. It is explicitly not a security feature.

## The problem it solves

People, especially people with ADHD, juggle a day job, family, volunteer work, chores, and side projects like an app or a food truck. Buckets appear and disappear quickly. After a few days away there may be two new ones, and one that the person has run out of energy for.

## Key decisions and why

| Decision | Why |
|---|---|
| Opens with "Hello, [name]. What are we working on today?" | A friendly, low-effort start that gets to work fast. |
| Users define their own irons and questions | Makes it useful to everyone, not just one person's setup. |
| Learns keywords, but only with confirmation | So "food truck" or "permits" sorts automatically without the plugin guessing wrong. |
| Offers best guesses when unsure | Helps put things in the right place without making the user explain. |
| Detects new irons and asks | Life changes; the map has to keep up. |
| Catch-up after gaps, periodic review | Buckets change fast, especially for ADHD brains. |
| At most two nudges at a time, never guilt | Too many reminders cause shutdown, not action. |
| Snooze options (a day / a few days / a week) | The user picks when to be reminded. |
| Archive, never delete (unless asked) | Setting something down isn't giving up; it stays ready for its next chance at some heat. |
| Promote a bucket to a Claude Project ("give it a forge") | Siloed focus, its own documents, and collaborators. Done in the browser for the user by default, since most people don't want to stop for admin. |
| Remember each iron's "why" (added in 0.2.0) | An iron only stays hot with motivation. Leading a nudge with the why lands better than "you haven't touched this." |
| Spark catching (added in 0.2.0) | A tangent is often a good idea at an inconvenient time. Catch it, file it, offer to return. Never "get back on track." |
| Name and metaphor | "Irons in the fire" carries the whole idea: heat is attention, cooling is neglect, pulling an iron out is a choice. "Too many" was dropped because having many irons isn't the problem. |

## Limits to remember

- A plugin speaks up only when a session is opened. Reminders on a specific day need an optional scheduled task.
- A plugin can't create a Claude Project by itself; it uses the browser with the user's okay, or walks the user through it.

## Ideas for later

- Optional reminders for people who disappear for a week or more
- Testing with a few outside users before publishing more widely
- A landing page to promote the plugin
- Publishing through a public plugin marketplace once it's been tuned
