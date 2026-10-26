# All of my Irons in the Fire!
*A Claude plugin by Mindful Tech Projects*

**Current version: 0.8.0** · [Website](https://mindfultechsupport.github.io/All-of-the-Irons-in-the-Fire-App-/) · [Change summary](CHANGELOG.md) · [All releases](releases/)

**[💬 Send feedback](../../issues/new?template=feedback.yml)** · **[❤️ Support on Patreon](https://www.patreon.com/mindfultechsupport)**

## What it does

All of my Irons in the Fire! helps people keep every iron in the fire glowing: the job, the family, the side hustle, the dream. It learns the user's life, remembers why each iron matters, and helps them decide which ones to heat up, which to let rest, and which to pull from the fire. It never throws an iron away. It keeps each one safe and ready for the next chance to put some heat to it.

## How it feels to use

- **It keeps time with you.** It knows what time it is and how long you've been away, so you get "Good morning, Ed. Hope you got some rest," not a cold start.
- **It picks up where you left off.** "Last time we were on the food truck. Want a quick summary of what we were talking about?" Then: "Keep going on the food truck, or work on something else?"
- **It asks a question to get you going.** "How are you doing this afternoon, Ed?" or "What's on your mind?"
- **It keeps a desk list.** Anything that needs a screen goes on one list across all your irons. Say "I'm at my desk" and it walks you through about 15 minutes of it, one step at a time, out loud if you like: "Ready for number one?" "Done." "Nice, number two…"
- **It asks before it remembers.** It tells you exactly what it saves, and "what do you know about me" or "forget everything" work anytime.
- **It talks like a person when you're talking out loud.** In Claude's voice mode, or when you say "I'm driving," it speaks in short, plain sentences, one question at a time, hands-free. Anything that needs a screen is saved for later.
- **It helps you stay up to date.** Every couple of weeks it offers to check for a new version (only looking online if you say yes) and walks you through updating.
- **It makes feedback easy.** Say "send feedback" and it drafts a note to the creator with you.
- **It shows all your irons at a glance**, with how long since each one was touched: "Food Truck: 3 hrs, Hang Gliding Trip: 18 days." Spot one you've missed, and jump in or put it on hold.
- **It tells you what's waiting.** Back after a few days? "It's been 4 days, Ed. There are 3 things to catch up on."
- **It can nudge you at a time you pick**, like 8:30 on weekday mornings, even when you haven't opened Claude.
- **You can give Claude a nickname.** ChatBro, anyone? It checks in now and then to make sure the name still fits.
- **It sorts it into the right iron.** Say "food truck" and it knows that's your side project. If it isn't sure, it offers a few guesses.
- **It learns your world.** Each time you confirm or correct, it remembers the words that belong to each iron.
- **It remembers your why.** Tell it why an iron matters and it brings that back when the iron starts cooling.
- **It catches sparks.** Wander off to another iron mid-task and it helps you get the idea down, files it in the right place, and lets you choose to stay with it or come back.
- **It spots new irons**, like that hang gliding trip you just started talking about.
- **It checks on cooling irons gently**, at most two at a time: put some heat to it, ask again later, let it rest, or pull it out of the fire.
- **It runs a periodic review** every two weeks, monthly, or never, as you choose.
- **It gives a hot iron its own forge.** A big iron can become its own Claude Project, set up in your browser if you like.

## Core design principles

- Warm, brief, never guilt-inducing. Check on at most two irons in the fire at a time.
- Learn the user's life: every iron in the fire, what belongs to each, and which are hot enough to become Projects. Ask before promoting one.
- Keep tabs on all the irons in the fire, so nothing the user cares about quietly goes cold.
- Remember why each iron in the fire matters. An iron only stays hot with motivation, so capture the user's "why" and bring it back when an iron is cooling.
- When the user strays to another iron in the fire, treat it as a spark worth catching, not a mistake. Help get the idea out, suggest which iron it belongs to, and offer to return to it. Never say "get back on track."
- The user decides which irons stay in the fire. Pull them out (archive) instead of throwing them away (delete).
- Learn new keywords only with the user's confirmation.
- Keep time with the user: know what time it is, how long they've been away, and where they left off, so every return feels like picking up a conversation, not starting over.
- Ask direction questions, not secrets; this is not a security feature.

## Install

**You'll need a computer for this.** Plugins are added in Claude on the web (claude.ai), the Claude desktop app, or Claude Code; the Claude phone app can't install a plugin from a file. Once installed, it's on your Claude account.

### Option 1: add the marketplace (recommended)

This repository is a plugin marketplace. Add it once, and new versions can come from here.

- **Claude desktop app or claude.ai:** go to **Customize → Plugins**, add a marketplace, and enter `MindfulTechSupport/All-of-the-Irons-in-the-Fire-App-`. Then install **all-my-irons-in-the-fire**.
- **Claude Code:**
  ```
  /plugin install all-my-irons-in-the-fire --marketplace MindfulTechSupport/All-of-the-Irons-in-the-Fire-App-
  ```

### Option 2: install from a file

1. Open [the latest release](../../releases/latest) and download the file ending in `.plugin` (currently `all-my-irons-in-the-fire-v0.8.0.plugin`).
2. In the Claude desktop app or claude.ai, go to **Customize → Plugins**.
3. Remove an older version if it's listed, then upload the file.

Then start a new chat and say **"fire up."** The greeting should match the time of day.

### Updating

Ask "is there a new version?" anytime, or let the plugin offer during a review. It walks you through the update on a computer. Your irons map is kept separately, so nothing is lost.

## Try saying

- **"Fire up."** Greets you for the time of day and picks up where you left off.
- **"What's in the fire?"** Shows every iron and how long since you touched it.
- **"I'm driving, talk me through it."** Switches to hands-free, spoken style.
- **"Put the hang gliding trip on hold. Waiting on gear."** Rests an iron with a note.
- **"Review my irons."** A quick look at everything: keep, rest, or pull out of the fire.
- **"Put that on my desk list."** Saves a screen-only task for later.
- **"I'm at my desk."** A guided 15-minute session through your desk list.
- **"What do you know about me?"** Shows everything saved; "forget everything" erases it.
- **"Send feedback."** Drafts a note to the creator with you.

## Feedback and support

All of my Irons in the Fire! is free and made by one person at Mindful Tech Projects.

- **Ideas, problems, or love notes:** [send feedback](../../issues/new?template=feedback.yml). You can also just say "send feedback" to the plugin, and it'll help you write it.
- **If it helps you:** [support the creator on Patreon](https://www.patreon.com/mindfultechsupport). The plugin mentions this once after setup and never nags.
- **Privacy:** the plugin sends nothing to Mindful Tech Projects. See [PRIVACY.md](PRIVACY.md).

## Skills

| Skill | What it's for |
|---|---|
| `fire-up` | Clock and time-of-day greeting, quick summary and continue-or-switch, sorting, learning, whys, spark catching, new and cooling irons, catch-up count, nickname check-in, first-time setup and daily-nudge setup, voice-friendly mode, update check, feedback |
| `daily-nudge` | The optional daily nudge at a time you choose: what's waiting, in a few warm lines |
| `at-my-desk` | The desk list across all irons, and guided 15-minute desk sessions with spoken check-offs |
| `my-data` | What's saved and permission to save it; see, export, or forget everything |
| `irons-review` | Look at everything; add, rename, merge, rest, archive, revive; update whys |
| `give-it-a-forge` | Turn a hot iron into its own Claude Project |

## Repository layout

```
README.md        This page, always describing the current version
CHANGELOG.md     What changed in every version, newest first
LICENSE          Usage terms
PRIVACY.md       What the plugin does (and doesn't do) with your information
.claude-plugin/  Marketplace catalog, so Claude can install the plugin from this repo
docs/            The website (GitHub Pages)
plugin/          The plugin's source files (current version)
releases/        Frozen copies of every version, version number in each file name
  v0.1.0/
  v0.2.0/
  v0.3.0/
  v0.4.0/
  v0.5.0/
  v0.6.0/
  v0.7.0/
  v0.8.0/
```

## Versioning

Versions follow [Semantic Versioning](https://semver.org): `MAJOR.MINOR.PATCH`. Each release gets a git tag (`v0.2.0`), a GitHub Release with notes and the downloadable plugin, an entry in CHANGELOG.md, and a folder in `releases/` with versioned copies of the plugin, README, and design notes.

Every version goes through review before it's published:

1. **Prepare** on a `release/vX.Y.Z` branch: update `plugin/` and its version number, add the version's section to CHANGELOG.md, and add a `releases/vX.Y.Z/` folder with the versioned files.
2. **Review** in a pull request. The owner reviews the changes and can request or make tweaks; nothing is public yet.
3. **Publish** only after the owner approves: the pull request is merged into `main`, and the [Publish releases](.github/workflows/release.yml) workflow creates the tag and Release page automatically.

## Where your map lives

Your Irons Map is a short, readable note kept in Claude's memory (if memory is on) or in a file called `irons-in-the-fire.md` in your working folder. You can open and edit it anytime.

## License

Copyright © 2026 Mindful Tech Projects. All rights reserved. See [LICENSE](LICENSE). This project is in early development and is not yet open for reuse or redistribution.
