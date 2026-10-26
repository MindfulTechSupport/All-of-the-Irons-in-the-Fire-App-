# All of my Irons in the Fire!
*A Claude plugin by Mindful Tech Projects*

**Current version: 0.6.0** · [Change summary](CHANGELOG.md) · [All releases](releases/)

## What it does

All of my Irons in the Fire! helps people keep every iron in the fire glowing: the job, the family, the side hustle, the dream. It learns the user's life, remembers why each iron matters, and helps them decide which ones to heat up, which to let rest, and which to pull from the fire. It never throws an iron away. It keeps each one safe and ready for the next chance to put some heat to it.

## How it feels to use

- **It keeps time with you.** It knows what time it is and how long you've been away, so you get "Good morning, Ed. Hope you got some rest," not a cold start.
- **It picks up where you left off.** "Last time we were on the food truck. Want a quick summary of what we were talking about?" Then: "Keep going on the food truck, or work on something else?"
- **It asks a question to get you going.** "How are you doing this afternoon, Ed?" or "What's on your mind?"
- **It talks like a person when you're talking out loud.** In Claude's voice mode, or when you say "I'm driving," it speaks in short, plain sentences, one question at a time, hands-free. Anything that needs a screen is saved for later.
- **It keeps itself up to date.** About once a week it checks for a new version and offers to walk you through updating.
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

**You'll need a computer for this.** Plugins are added in Claude on the web (claude.ai) or the Claude desktop app; the Claude phone app can't install a plugin from a file. Once installed, it's on your Claude account.

1. On your computer, open [the latest release](../../releases/latest) and download the file ending in `.plugin` (currently `all-my-irons-in-the-fire-v0.6.0.plugin`).
2. Open the Claude desktop app or claude.ai and go to **Customize → Plugins** in the left sidebar.
3. Upload the file.
4. Start a new chat and say **"fire up."** The greeting should match the time of day.

### Updating

The plugin checks for new versions about once a week and offers to walk you through updating. To update by hand: download the new `.plugin` file, go to **Customize → Plugins**, remove the old version, and upload the new one. Your irons map is kept separately, so nothing is lost.

## Skills

| Skill | What it's for |
|---|---|
| `fire-up` | Clock and time-of-day greeting, quick summary and continue-or-switch, sorting, learning, whys, spark catching, new and cooling irons, catch-up count, nickname check-in, first-time setup and daily-nudge setup, voice-friendly mode, update check |
| `daily-nudge` | The optional daily nudge at a time you choose: what's waiting, in a few warm lines |
| `irons-review` | Look at everything; add, rename, merge, rest, archive, revive; update whys |
| `give-it-a-forge` | Turn a hot iron into its own Claude Project |

## Repository layout

```
README.md        This page, always describing the current version
CHANGELOG.md     What changed in every version, newest first
LICENSE          Usage terms
plugin/          The plugin's source files (current version)
releases/        Frozen copies of every version, version number in each file name
  v0.1.0/
  v0.2.0/
  v0.3.0/
  v0.4.0/
  v0.5.0/
  v0.6.0/
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
