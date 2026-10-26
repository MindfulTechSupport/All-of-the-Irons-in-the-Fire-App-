# All of my Irons in the Fire!
*by Mindful Tech Projects*

## What it does

All of my Irons in the Fire! helps people keep every iron in the fire glowing: the job, the family, the side hustle, the dream. It learns the user's life, remembers why each iron matters, and helps them decide which ones to heat up, which to let rest, and which to pull from the fire. It never throws an iron away. It keeps each one safe and ready for the next chance to put some heat to it.

## How it feels to use

- **It greets you and asks what you're working on.** "Hello, Ed. What are we working on today?"
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
- Ask direction questions, not secrets; this is not a security feature.

## Skills

| Skill | What it's for |
|---|---|
| `fire-up` | Greeting, sorting, learning, whys, spark catching, new and cooling irons, first-time setup |
| `irons-review` | Look at everything; add, rename, merge, rest, archive, revive; update whys |
| `give-it-a-forge` | Turn a hot iron into its own Claude Project |

## Where your map lives

Your Irons Map is a short, readable note kept in Claude's memory (if memory is on) or in a file called `irons-in-the-fire.md` in your working folder. You can open and edit it anytime.

## Version

0.2.0. See CHANGELOG.md for what changed in each version.
