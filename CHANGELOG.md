# Change summary — All of my Irons in the Fire!
*by Mindful Tech Projects*

Each version lists what changed and why, newest first.

---

## 0.3.0 — 2026-10-26

**Theme: keeping time with you.** You sleep, you work, you come back. The plugin should know you've been away and pick up the conversation like a friend would, not start over.

### New
- **Built-in clock.** Each session starts by checking the current time and your timezone, then working out how long you've been away: under an hour, a few hours, overnight, or days.
- **Greetings for the time of day.** "Good morning, Ed." "Good afternoon, Ed." "Good evening, Ed." Late at night: "Hey Ed, you're up late."
- **Greetings that fit the gap.** "Welcome back" after a short break, "Hope you got some rest" after a night's sleep, "Good to see you, it's been 4 days" after a longer stretch, never as a scolding.
- **Picks up where you left off.** The plugin saves a one-line snapshot (which iron, where you stopped, the next step) and offers it when you come back: "Last time we were on the food truck menu. Want to pick that back up?"
- **Opener questions to get the juices flowing**, rotated so they don't repeat: "How are you doing this afternoon, Ed?", "What's on your mind?", "Where do you want to put some heat today?", and more.
- **Give Claude a nickname.** Setup asks what you'd like to call Claude; Ed's pick is ChatBro. Change it anytime ("call yourself ChatBro").
- **Saves as you go.** The clock and snapshot update at natural stopping points, not just at the end, since people often just walk away. Saying goodnight gets a goodnight back.

### Changed
- New core principle: keep time with the user, so every return feels like picking up a conversation.
- Map fields: `last-check-in` (date only) is replaced by `last-seen` (date and time). Added `timezone`, `assistant-name`, `last-session`, and `last-opener`. Maps from 0.1.0 and 0.2.0 keep working and upgrade themselves.

### Honest limits
- Claude knows the time whenever a session is open, but it doesn't run in the background between sessions. Reminders while you're away still use the optional scheduled task.

---

## Repository housekeeping — 2026-10-26

No change to the plugin itself.

- Organized the repository: `plugin/` holds the readable source, `releases/` holds frozen, version-named copies of every release.
- `README.md` restored to its standard name so GitHub shows it on the front page; it now states the current version, install steps, layout, and versioning rules.
- Versioned snapshots: `README-v0.1.0.md`, `README-v0.2.0.md`, `design-notes-v0.2.0.md`, and `all-my-irons-in-the-fire-vX.Y.Z.plugin`.
- Added `LICENSE` (all rights reserved while in early development) and `.gitignore`.
- Added the **Publish releases** automation: whenever a new `releases/vX.Y.Z/` folder lands on `main`, GitHub creates the `vX.Y.Z` tag and a Release page with notes from this file and the versioned files attached. Its first run publishes `v0.1.0` and `v0.2.0`.

---

## 0.2.0 — 2026-10-25

**Theme: motivation and sparks.** An iron only stays hot with a reason behind it, and a wandering mind is often bringing a good idea at an inconvenient time.

### New
- **Remembers each iron's "why."** Setup and new-iron creation ask, lightly and optionally, why each iron matters (for example "my ticket to retiring rich"). The why is saved on the Irons Map.
- **Cooling nudges lead with the why.** Instead of "you haven't touched this," it says "the food truck's been cooling, and you said this one's your ticket to retiring rich."
- **Spark catching.** When you stray to another iron mid-task, the plugin treats it as a spark worth catching: it helps get the idea out, suggests which iron it belongs to, saves it there, and offers to stay with it or come back later. It never says "get back on track."
- **Sparks come back.** Saved sparks are brought up the next time that iron is worked on, and in reviews.
- **Reviews check the why.** The periodic review asks whether an iron's why still holds, and edits can add or update a why anytime.
- **Forged Projects carry the why.** When an iron becomes its own Claude Project, its instructions include the why and any captured sparks.

### Changed
- Added the official "What it does" statement and the core design principles to the plugin, so Claude follows them in every interaction.
- Language now uses "irons in the fire" throughout: put heat to it, cooling, let it rest, pull it out of the fire, running hot.
- Archiving is described as "pulling it out of the fire for now; it stays safe and ready for its next chance at some heat."

### Map format
- Added `why` and `sparks` fields to each iron. Existing 0.1.0 maps keep working; the new fields fill in over time.

---

## 0.1.0 — 2026-10-25

First release.

- **Fire Up:** greeting by name, "What are we working on today?", sorting into irons, learning keywords with confirmation, spotting new irons, cooling-iron nudges (at most two) with snooze, catch-up after gaps, first-time setup.
- **Irons Review:** periodic review; add, rename, merge, move keywords, rest, archive, revive.
- **Give It a Forge:** promote an iron to a Claude Project, set up in the browser with the user's okay or walked through step by step.
- Archive instead of delete; nothing changes without the user's yes; not a security feature.
