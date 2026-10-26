# All of my Irons in the Fire! — Design Notes
*Mindful Tech Projects · started 2026-10-25 · owner: Ed Vita · version 0.9.1*

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
| Built-in clock and time-away awareness (added in 0.3.0) | Ed noticed it after sleeping and coming back: the plugin should know he'd been away for an hour, five hours, or overnight, and act like it's been helping all along. |
| Time-of-day greetings and opener questions (added in 0.3.0) | "Good afternoon, Ed. How are you doing?" feels like a friend; rotating openers like "What's on your mind?" get the juices flowing without feeling scripted. |
| Pick up where you left off (added in 0.3.0) | A one-line snapshot of the last session removes the hardest part of restarting: remembering where you were. |
| Nickname for Claude (added in 0.3.0) | Makes it feel personal. Ed's pick is ChatBro. It's a nickname only; Claude stays Claude. |
| Save at natural stopping points (added in 0.3.0) | People rarely say goodbye; they just walk away. Saving as you go keeps the pick-up accurate. |
| Daily nudge at a chosen time (added in 0.4.0) | The plugin only speaks when a chat is open; a scheduled task lets it reach out first. The user picks the time, approves it, and can stop it anytime. |
| Catch-up count (added in 0.4.0) | After time away, knowing "3 things are waiting" is calming; seeing all of them at once is not. Count first, two at a time. |
| Nickname check-in (added in 0.4.0) | Names that fit in October may not fit in March. A light monthly check keeps it the user's choice. |
| Quick summary offer, then continue or switch (added in 0.5.0) | Coming back is the hardest moment. Offering (not forcing) a short recap, then a clear "keep going or something else?", gets the user moving in two easy answers. |
| Irons glance with time since last touched (added in 0.5.0) | Ed's idea: an ADHD brain often notices something it hasn't thought about in a long time and suddenly has energy for it. Hours under a day, days after; neutral, no "overdue" labels; quick ways to pick it up, put it on hold, or drop a thought. |
| One question at a time (added in 0.5.0) | Stacked questions overwhelm, especially for ADHD brains. Ask, wait, then ask the next. |
| Review before publishing (process, 0.5.0) | Ed wants final approval and the chance to tweak each version before it goes public. Versions are prepared in a pull request and published only on his go-ahead. |
| Voice-friendly mode (added in 0.6.0) | Ed built most of this plugin by voice from the car. Spoken conversations need sentences, short turns, and words for numbers, not lists and symbols. |
| Hands-free while driving, with a later list (added in 0.6.0) | Safety first: never ask a driver to look or tap. Anything needing a screen is saved, not lost. |
| Update check and install guide (added in 0.6.0) | Ed's 0.3.0 to 0.5.0 installs never went through because installing from a phone isn't possible and the steps weren't clear. The plugin now explains it plainly and offers help when a new version is out. |
| No "sign out all devices" shortcut (decided in 0.6.0) | Considered and rejected: Claude can't install plugins into an account, signing out wouldn't help, and an app asking to take over your account looks like a scam. The real fix is the marketplace in 0.7.0. |
| Website on GitHub Pages (added in 0.7.0) | Free, lives in the same repository, and updates with every release. Feedback and Donate are highlighted, as Ed asked. |
| Marketplace (added in 0.7.0) | Install once, update from the repo. Fixes the "I can't install from my phone" problem for every version after the first. |
| Feedback the user submits themselves (added in 0.7.0) | The plugin runs in each user's Claude and can't write to Ed's database. The user reviews and posts it, so nothing private leaves without their yes. |
| One-time Patreon mention (added in 0.7.0) | Ed liked "mention it once." Anthropic's directory policy excludes software that works as advertising, so it's one line after setup, then only when asked. |
| Update check asks first (changed in 0.7.0) | Anthropic's directory policy: plugins shouldn't make Claude contact outside resources unless the user asks. |
| Desk list with 15-minute sessions (added in 0.8.0) | Ed's idea from the car: things that need a screen pile up across projects. One list, sized to 15 minutes, most important first, so sitting down feels doable. |
| Spoken check-offs (added in 0.8.0) | Ed's addition: "I just finished number one." "Okay, number two." One step at a time, no looking at the screen to know what's next. |
| Ask before remembering; forget everything (added in 0.8.0) | Ed's consent idea plus Anthropic's privacy rules: users should know what's saved, agree to it, and be able to erase it in one step. |
| Nudges by notification or email (added in 0.8.0) | Reach the user right away without building anything new: Claude's scheduled tasks already deliver both. Texting only via a service the user connects. |
| Built-in help, starting with Claude's own notices (added in 0.8.1) | Ed got a "memory settings" notice while driving and it vanished. Users need a plain answer: what it is, that it's their choice, and where the setting lives. |
| Brain care, always asked first (added in 0.9.0) | Ed: fast brains forget water, food, the bathroom, and moving; a break is easier to take when someone holds your thought. Wellness suggestions only, never medical advice or moralizing. |
| Desk list in front, crossed off not erased (added in 0.9.0) | Ed: small undone tasks are where great ideas stall; seeing line-throughs pile up keeps people going. Spoken mode gives the count instead of reading the whole list. |
| "Which of these sound like you?" (added in 0.9.0) | Ed: appeal to everyone; let people pick the groups that fit so the plugin offers the right helpers. Never a label. |
| Neutral, inclusive language rule (added in 0.9.0) | Ed asked for no gender bias anywhere; use the user's own words for the people in their life. |
| A privacy check for every version (added in 0.9.1) | Ed's rule after setting up the privacy-legal plugin: every release gets a short, plain-English privacy check before approval. Feedback stays public only, so Mindful never holds private user information. |
| Name and metaphor | "Irons in the fire" carries the whole idea: heat is attention, cooling is neglect, pulling an iron out is a choice. "Too many" was dropped because having many irons isn't the problem. |

## Limits to remember

- The clock works whenever a session is open, but the plugin doesn't run in the background between sessions.
- A plugin speaks up only when a session is opened. Reminders on a specific day need an optional scheduled task.
- A plugin can't create a Claude Project by itself; it uses the browser with the user's okay, or walks the user through it.

## Ideas for later

- Optional reminders for people who disappear for a week or more
- Testing with a few outside users before publishing more widely
- A landing page to promote the plugin
- Rethink where the irons map is stored before submitting to Anthropic's directory (policy 1G)
- Free and paid tiers (monthly subscription) — Ed's idea for later
