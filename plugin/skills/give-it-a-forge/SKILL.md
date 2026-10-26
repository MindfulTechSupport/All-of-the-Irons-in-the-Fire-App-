---
name: give-it-a-forge
description: Promotes an iron in "All of my Irons in the Fire!" into its own Claude Project so it can be siloed for focus, hold its own documents, and be shared with collaborators. Use when the user says "make this a project", "give it a forge", "turn this bucket into a project", "this needs its own space", or accepts the offer to promote an iron.
---

# Give It a Forge — promote an iron to a Claude Project

Load the Irons Map as described in the `fire-up` skill.

## 1. Prepare the Project

From the iron's entry and the conversation, draft:
- **Project name**: the iron's name, unless the user wants another.
- **Description**: one sentence on what this iron is.
- **Project instructions**: a short block telling Claude what this Project is for, the iron's why (in the user's words), the key people, goals, keywords, and any sparks captured so far, and to keep other irons out of it. When other irons come up inside the Project, Claude should catch the spark and suggest where it belongs rather than refusing.
- **Files to add**: list any documents the user has mentioned for this iron.

Show the draft briefly and ask: "Look right? Want me to set it up in your browser, or would you rather do the clicks yourself?" Default offer: do it for them.

## 2a. Set it up in the browser (default)

Only with the user's yes, and only if a browser tool is available (Claude in Chrome or the built-in browser). Load that browser's skill first if one is listed.

1. Open claude.ai in the user's browser (they must already be signed in; never enter passwords).
2. Go to Projects and create a new Project.
3. Enter the name and description.
4. Paste the Project instructions.
5. Do not upload files on your own. Tell the user which files to drop in, unless they've asked you to upload specific files they supplied.
6. Tell the user it's done and where to find it.

If the browser can't be reached or something on the page doesn't match, stop and fall back to 2b.

## 2b. Walk the user through it

Give short numbered steps: open claude.ai → Projects → create a Project → paste the name, description, and the instructions (provide them in a copyable block) → add the listed files.

## 3. Update the map

Set the iron's `forge` field to the Project name. Tell the user: "From now on, open the [name] Project when you're working on this. I'll still keep it on your map so check-ins and reviews include it."

## Rules

- Never create a Project, upload files, or share a Project with anyone without the user's explicit yes in chat.
- Never enter passwords or sign the user in.
- A plugin can't create a Project by itself; it's done through the browser or by the user.
