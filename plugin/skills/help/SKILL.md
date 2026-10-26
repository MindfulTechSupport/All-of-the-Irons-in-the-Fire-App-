---
name: help
description: Help for "All of my Irons in the Fire!". Use when the user says "help", "how do I…", "what does this notification mean?", "Claude told me to update my memory settings", "what's the sensitive topics thing?", "my nudge didn't come", "it's not working", "how do I keep work and personal separate?", or seems confused about a Claude notice, installing, nudges, voice mode, or their data.
---

# Help

Answer the user's actual question in a few plain sentences, using the reference below. Don't read the whole thing out. In voice-friendly mode, keep it spoken and short, and put anything that needs a screen on the desk list.

If a notification came from Claude itself (not the plugin), say so, explain what it means, and make clear the choice is theirs. Never pressure the user to change a privacy setting; the plugin works either way.

If the reference doesn't cover it, help as best you can, then offer: "Want to send this to the developer as feedback?"

## Reference


Quick answers to the things people run into most. You can also just ask the plugin: "help," or "what does this notification mean?"

## Notifications from Claude

These come from Claude itself, not from the plugin. The plugin works either way.

### "Update your memory settings" or "Include sensitive topics in memory?"

**What it is:** Claude's own memory normally doesn't save sensitive topics, such as health (including things like ADHD), religion, politics, or gender identity. The first time you mention something like that and Claude decides not to save it, it shows a one-time notice asking whether you'd like it to.

**What to do:** it's your choice.
- **Leave it off** if you'd rather Claude not remember sensitive things. All of my Irons in the Fire! works fine without it.
- **Turn it on** if you want Claude to remember things like that too. Go to **Settings → Your Claude → Include sensitive topics in memory** (in older versions of the app, **Settings → Memory**). You'll see a small notice each time a sensitive memory is saved, so you can review it.

If the notice disappeared before you could read it, nothing is lost. You can change the setting anytime in the same place.

### "Claude saved a memory" notices

Claude remembers useful things from your chats. To see, edit, or delete them: **Settings → Your Claude → Manage** (next to "Your memory").

### A scheduled task asking for approval

When you set up a daily nudge, Claude may ask you to approve the scheduled task. Approve it to get nudges. You can turn it off anytime by saying "stop my daily nudge."

### A website or browser asking for permission

If the plugin helps you set something up in your browser (like creating a Claude Project), the browser may ask you to allow claude.ai. Allow it only if you asked for that help.

## Keeping work and personal separate

- **Separate accounts** are the strongest separation: one Claude account for work, one for personal, ideally in separate browser profiles.
- **Inside one account**, each Claude Project has its own memory. To keep a Project fully separate from your general memory, open the Project, find **Memory**, and turn off **Use account memory**.

## Installing and updating

- **You need a computer** to install. The Claude phone app can't install a plugin from a file.
- **Easiest:** in **Customize → Plugins**, add the marketplace `MindfulTechSupport/All-of-the-Irons-in-the-Fire-App-` and install from it.
- **Or:** download the latest `.plugin` file from [Releases](https://github.com/MindfulTechSupport/All-of-the-Irons-in-the-Fire-App-/releases/latest), then **Customize → Plugins → upload**. Remove the older version first.
- **Check it worked:** start a new chat and say "fire up."
- **Nothing happens after installing?** Start a brand-new chat. Existing chats may not pick up a new plugin.

## Your information

- **See what's saved:** "what do you know about me?"
- **Remove one thing:** "forget the hang gliding trip."
- **Remove everything:** "forget everything." You'll be offered an export file first.
- **Come back later:** "restore my irons" and share your export file.
- Nothing is sent to Mindful Tech Projects. See [PRIVACY.md](https://github.com/MindfulTechSupport/All-of-the-Irons-in-the-Fire-App-/blob/main/PRIVACY.md).

## Nudges

- **Not getting your daily nudge?** Check that the scheduled task is turned on and approved, and that notifications are allowed for the Claude app on your phone. Then say "check my daily nudge."
- **Change it:** "nudge me at 7 instead," "email my nudge," "stop the nudges."

## Voice and driving

- In the Claude app's voice mode, or after saying "I'm driving," the plugin talks in short sentences and never asks you to look at the screen.
- Anything that needs a screen goes on your desk list. Say "I'm at my desk" when you sit down.

## Still stuck?

Say "send feedback" and describe what happened, or [open a feedback form](https://github.com/MindfulTechSupport/All-of-the-Irons-in-the-Fire-App-/issues/new?template=feedback.yml).
