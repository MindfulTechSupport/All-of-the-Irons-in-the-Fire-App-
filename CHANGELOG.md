# Change summary — All of my Irons in the Fire!
*by Mindful Tech Projects*

Each version lists what changed and why, newest first.

---

## 0.9.0 — 2026-10-26

**Theme: take care of the brain.** Fast-thinking, busy brains can run for hours and forget water, food, the bathroom, or moving, or hit a wall when something feels too big. This version looks after the person, not just the project. Everything is offered as a question, never switched on by itself.

### New (`brain-care` skill)
- **Break check-in with "I'll hold that thought."** After a long stretch on one iron: "Want a quick break? Tell me what's on your mind first and I'll hold it." When you're back, it hands the thought right back.
- **Small things for the break**, from what you like: a few sips of water, a snack that keeps your energy steady (like a piece of fruit), stand up and stretch, rest your eyes, three slow breaths, fresh air, and yes, the bathroom you've been putting off. Never preachy; candy bars are still your call. Not medical advice.
- **Crunch-time mode:** if you need to push through, it just asks for a few sips and a ten-second stand.
- **Energy check:** "How's your energy today: low, medium, or high?" Tasks get sized to match, and a low-energy rest day counts as progress.
- **Tiny-step mode:** when something feels too big, one step of two minutes or less, then the next.
- **Body doubling:** "Stay with me while I work." It keeps you company and checks in lightly.
- **Done list:** everything you finish is recorded, by iron. "What did I get done?" shows it. It will feed the weekly recap later.
- **What's calling you today?** Pick by interest and energy, not guilt.

### Also new
- **The desk list comes first.** At a screen, the whole desk list shows right after the greeting until it's done or you say "not now."
- **Crossed off, not erased.** Finished desk-list items stay on the list with a line through them and a running count ("2 of 4 done"). Out loud, it says "two down, two to go."
- **People tasks** on the desk list: who to talk to, what to ask, and a draft message you can send yourself.
- **"Which of these sound like you?"** An optional setup question (founder, side hustler, ADHD brain, job and family, dreamer, creator, on the move, freelancer, small business owner, job hunting, caregiver, limited energy or burnout recovery, next chapter, volunteer, student). It decides which helpers to offer; it's never a label.
- **Talk it out:** adding a new iron starts with "Tell me everything about it, ramble away."
- **Quiet hours:** no nudges or check-ins during the times you protect.
- **Phone or computer?** It asks when it matters, and reminds you that chats carry over to the Claude app on your phone.

### Changed
- New principles: ask before doing; use neutral, inclusive language and the user's own words for the people in their life.
- Privacy note and disclosure now mention the done list and, only if you share them, how you describe yourself and your energy.
- Map fields added: `who-i-am`, `quiet-hours`, `brain-care`, `done-list`, and `done` on desk-list items.

---

## 0.8.1 — 2026-10-26

**Theme: help when you need it.** Prompted by a Claude notification Ed saw while driving and couldn't read before it disappeared.

### New
- **Help (new `help` skill and HELP.md).** Ask "help," "what does this notification mean?", or "Claude told me to update my memory settings" and get a short, plain answer.
- **Explains Claude's own notices**, starting with the "include sensitive topics in memory" prompt: what it is, that the choice is yours, where the setting lives, and that the plugin works either way.
- **Keeping work and personal separate:** separate accounts, or turning off "Use account memory" on a Claude Project.
- **"Check my daily nudge":** reports whether the nudge is on, when it runs next, and whether the last one worked.
- Help is linked from the README and the website.

---

## 0.8.0 — 2026-10-26

**Theme: always with you, and always yours.** The plugin keeps track of the things you can only do at a screen and walks you through them out loud. And you always know what it remembers, agree to it, and can erase it in one step.

### New
- **Desk list (new `at-my-desk` skill).** Anything that needs a screen, from any iron, goes on one list: "put that on my desk list." Each item gets plain steps and a time estimate.
- **15-minute desk sessions.** Say "I'm at my desk" or "I'm parked," and the plugin picks what fits in about 15 minutes (most important first) and walks you through it **one step at a time, spoken or typed**: "Ready for number one?" … "Done." … "Nice, that's one down. Ready for number two?" Say done, skip, later, or stop. Leftovers roll to next time, no guilt.
- **Nudge delivery choices.** The daily nudge can arrive as a phone notification, an email, or both. Texting works through a service you've connected yourself (for example Zapier).
- **Ask before remembering (new `my-data` skill).** At setup, the plugin explains in plain words what it will remember, where, and how to erase it, and asks permission before saving anything. Say no and it still helps you, without saving. Users upgrading from an older version see this once.
- **"What do you know about me?"** Shows everything saved, in plain words, with an option to export a copy.
- **"Forget everything."** Always offers an export file first, so you can keep your irons and come back later, then erases the whole irons map after one clear confirmation, and offers to stop the daily nudge too. "Forget [one thing]" removes just that.
- **"Restore my irons."** Share your export file and pick up right where you left off.
- **30-day check-in:** "Still okay with me remembering your irons between chats?"
- **Feedback in your own words.** Say "send feedback to the developer" and just talk. The plugin asks a few clarifying questions, boils it down to what you're really asking for, checks it with you, and drafts the note for you to submit.

### Changed
- `later-list` becomes `desk-list`, with steps, minutes, and priority per item. Older items move over automatically.
- PRIVACY.md now covers consent, what's saved, how long it's kept, and how to see or erase it.
- Map fields added: `consent`, `storage`, `nudge-delivery`, `desk-list`.

### For Anthropic's directory
- These consent and erase features answer the privacy rules (1D, 1E, 3A) and are a step toward 1G. Whether remembering between sessions is allowed in the directory is Anthropic's call; we'll ask them directly when we submit.

---

## 0.7.0 — 2026-10-26

**Theme: going public.** A home on the web, an easier way to install, a way for users to talk back, and a way to support the creator.

### New
- **Website.** A one-page site on GitHub Pages: what the plugin does, an example conversation, install steps, and highlighted **Download**, **Support on Patreon**, and **Send feedback** buttons. It's published from this repository's `docs/` folder.
- **Plugin marketplace.** This repository is now a Claude plugin marketplace (`.claude-plugin/marketplace.json`). Add it once in Customize, or in Claude Code run `/plugin install all-my-irons-in-the-fire --marketplace MindfulTechSupport/All-of-the-Irons-in-the-Fire-App-`, instead of downloading files for every version.
- **Send feedback.** Say "send feedback" and the plugin drafts a short note with you, shows it to you, and gives you the feedback form link. It never sends anything itself and never includes details from your irons.
- **Feedback form** on GitHub (Issues → Feedback), with a few simple questions.
- **Support the creator.** The plugin mentions Patreon (patreon.com/mindfultechsupport) **once**, right after setup, and never again unless you ask. The link is also on the website, the README, and the repository's **Sponsor** button.
- **Privacy note** (PRIVACY.md): the plugin sends nothing to Mindful Tech Projects.
- **"Try saying" examples** in the README.

### Changed
- **The update check now asks first.** Every couple of weeks (and during reviews) it offers to check for a new version and only looks online if you say yes, following Anthropic's directory policy that plugins shouldn't contact outside resources unless the user asks.
- Install guide covers the marketplace and file options.

### Before submitting to Anthropic's directory (not done yet)
- Anthropic's directory policy says software must not persistently store conversation content to build user profiles or read Claude's memory. The irons map is kept in the user's memory today, so the map's storage approach needs a rethink before directory submission.

---

## 0.6.0 — 2026-10-26

**Theme: talk to me, and keep me current.** Built from the car: the plugin should work out loud and hands-free, and nobody should get stuck on an old version because installing was confusing.

### New
- **Voice-friendly mode.** In Claude's voice mode, or when you say "I'm driving," "talk to me," or "talk me through it," the plugin speaks in short, plain sentences: no lists or symbols, numbers said the way people say them, one question at a time. It introduces itself by nickname ("Hey Ed, it's ChatBro. Good morning."), speaks the irons glance as a sentence, and reads back anything it saves. You can make it the default.
- **Hands-free while driving.** It never asks you to look, tap, or type. Anything that needs a screen is saved to a new **later list** and brought up next time you're typing: "You saved 2 things for when you're at a screen."
- **Update check.** About once a week (and during reviews), the plugin checks GitHub for a newer version and offers, in one line, to walk you through updating. It never installs anything itself or asks you to sign out of anything.
- **Install and update guide**, built into the plugin and in the README: step by step, including "this needs a computer; the phone app can't install plugins from a file."

### Changed
- Release pages now carry full computer-based install steps.
- Reviews include the update check.
- Map fields added: `voice-style`, `update-checked`, `later-list`.

### Honest limits
- Claude's voice mode is started by the user; the plugin can't speak first, and the daily nudge is still a written notification.
- Anthropic's documentation doesn't say whether plugins are active in voice mode. Version 0.6.0 is ready for it; the first real test is opening voice mode on a phone and saying "fire up."

### Coming in 0.7.0
- The GitHub repository becomes a plugin marketplace, so updates can come straight from the repo after a one-time setup.

---

## 0.5.0 — 2026-10-26

**Theme: an easy way back in.** Coming back to a conversation is easier when someone offers to remind you where you were, then lets you choose where to go next.

### New
- **Quick summary offer.** When you come back after an hour or more: "Last time we were on the food truck. Want a quick summary of what we were talking about?" If yes, you get 2 to 4 short lines: what was decided, where you stopped, and the next step.
- **Continue or switch.** Right after: "Want to keep going on the food truck, or work on something else?" Choosing something else offers your one or two hottest irons by name, the catch-up rundown if things are waiting, or something new.
- **Irons glance.** When you're choosing what to pick up, you see a short list of every active iron and how long since you last worked on it: hours if it's under a day, days after that ("Food Truck: 3 hrs," "Hang Gliding Trip: 18 days"). Sometimes spotting something you haven't touched in weeks is exactly what gives you the energy to jump in. No warnings or "overdue" labels; on-hold irons are marked as such.
- **Quick actions from the glance.** Pick any iron, keep going, say "put the trip on hold" (with an optional note like "waiting on the permit"), or drop a quick thought on any iron without switching.
- **Richer session snapshot.** The plugin now saves a short `summary` (key points, decisions, open questions) at natural stopping points, so the recap is accurate.

### Changed
- **One question at a time.** The greeting asks a single question and waits; the catch-up count and nickname check-in come after you've picked what to work on.
- The catch-up count is now stated in the greeting, with the rundown offered as one of the "what next" choices.
- `last-touched` now records the time as well as the date, so the glance can show hours. Older date-only values still work.
- Reviews open with the irons glance.

### Process
- Versions are now prepared on a `release/vX.Y.Z` branch with a pull request for review, and published only after Ed approves.

---

## 0.4.0 — 2026-10-26

**Theme: reaching out, and catching up.** The plugin can now come to you at a time you choose, tells you what's waiting when you've been away, and checks in on the little things like its nickname.

### New
- **Daily nudge at a time you pick.** Setup asks whether you want a nudge at a certain time of day (for example 8:30 AM on weekdays). If yes, it sets up a scheduled task, with your approval, that sends a short, warm message about what's waiting, even on days you don't open Claude. Change it or stop it anytime ("nudge me at 7 instead," "stop the nudges").
- **New `daily-nudge` skill.** Writes the nudge: a time-of-day greeting, where you left off, at most two things waiting, and one easy next step. Signed with your nickname for Claude. Never guilt.
- **Catch-up count.** After a day or more away, the greeting says how long it's been and how much is waiting: "It's been 4 days, Ed. There are 3 things to catch up on." It offers a quick rundown, two items at a time, instead of dumping everything.
- **Nickname check-in.** About once a month, it asks lightly whether the nickname still fits: "Still happy calling me ChatBro?"
- **Reviews include the nickname and nudge.** The periodic review checks both.
- **Upgrading users get offered the nudge once**, at a calm moment, and aren't asked again if they decline.

### Map format
- Added `nickname-checked`, `nudge-time`, `nudge-days`, `nudge-task`, and `last-nudged`. Older maps keep working.

### Setup questions (in order)
1. Your name  2. A nickname for Claude  3. Your irons in the fire  4. Their whys (optional)  5. How often to review  6. A daily nudge time (optional)

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
