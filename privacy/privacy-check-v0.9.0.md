RESEARCH NOTES — NOT LEGAL ADVICE — REVIEW WITH A LICENSED ATTORNEY BEFORE ACTING

> **⚠️ Reviewer note**
> - **Sources:** no legal research database connected; legal references are from model knowledge `[model knowledge — verify]`.
> - **Read:** PRIVACY.md, the plugin's skills (fire-up, my-data, daily-nudge, brain-care, at-my-desk, help), the website (docs/index.html), and the GitHub feedback form.
> - **Flagged for your judgment:** 3 items marked `[review]`.
> - **Currency:** not searched for recent developments; verify the cited rules before relying.
> - **Before relying:** fix items 1–4 below (all small); have an attorney skim this before the Anthropic directory submission.

# Privacy check — All of my Irons in the Fire! v0.9.0

*Mindful Tech Projects · 2026-10-26 · prepared with the privacy-legal plugin (first check; becomes the template for future versions)*

## Bottom line

**Low risk, with four small fixes.** The plugin's design keeps users' information in their own Claude account and sends nothing to Mindful Tech Projects, which avoids most privacy obligations. The fixes are about saying things more precisely and about two outside services (texting and the website's fonts).

**Classification:** PIA REQUIRED by house rule (every version gets a check); no mandatory GDPR impact assessment, because Mindful doesn't process the plugin data itself `[review]`. No conflict with the privacy note that would stop the release.

## 1. What this version changes

Version 0.9.0 adds brain care (breaks, energy check, tiny steps, body doubling, done list), keeps the desk list in front, and asks optional setup questions: "which of these sound like you?" (which can include ADHD, burnout recovery, caregiver, limited energy) and quiet hours.

## 2. What's saved and where

| What | Where | Who decides |
|---|---|---|
| Irons, whys, notes, desk list, done list, settings, timestamps | User's Claude account memory, or a file in the user's folder | The user |
| Optional self-description (e.g., ADHD, burnout) and energy level | Same | The user |
| Feedback | Public GitHub issues, posted by the user | Mindful (how it's used); GitHub hosts |
| Patreon supporter info | Patreon, shared with Mindful as creator | Mindful (controller) |

Nothing goes to Mindful's own systems. There are none.

## 3. Who else could see it (third parties)

- **Anthropic** hosts the user's Claude account, memory, and scheduled tasks, under Anthropic's privacy policy.
- **Zapier and its texting provider** (SMS by Zapier uses Twilio) carry the text of any texted nudge, if the user turns texting on.
- **Email providers** carry the text of emailed nudges.
- **GitHub** hosts feedback posts and the website, and logs website visitors' basic connection data.
- **Google Fonts**: the website loads its fonts from Google, which receives each visitor's IP address.
- **Patreon** processes donations.

## 4. Findings and fixes

**1. "Only you and your Claude can see it" is too absolute.** Anthropic stores the user's Claude account data. **Fix:** say "stored in your own Claude account, which Anthropic hosts under its privacy policy; Mindful Tech Projects never receives it," with a link to Anthropic's privacy policy.

**2. Texted and emailed nudges travel through outside services.** A nudge might mention an iron by name, such as "the job search" or something personal. **Fix:** (a) add to PRIVACY.md that texted or emailed nudges pass through Zapier, its texting provider, or email providers, under their policies; (b) in the daily-nudge skill, never put self-description, health, or energy details in a texted or emailed nudge; offer a "keep my texts generic" setting.

**3. Privacy questions go to a public place.** PRIVACY.md says "Questions: open an issue," which would make someone's privacy request public. **Fix:** add a private contact for privacy requests, such as an email address you're comfortable publishing. `[review]` Your choice of address.

**4. The website loads Google Fonts from Google's servers.** European courts have found that loading Google Fonts this way, without consent, shares visitors' IP addresses in violation of GDPR (for example, LG München I, 20 January 2022, 3 O 17493/20) `[model knowledge — verify]`. **Fix:** host the two fonts in the repository instead, or use the system fonts. This is a one-time change, and the site looks the same.

**5. Optional self-description can be health information.** Choices like "ADHD brain" or "burnout recovery" are sensitive. They stay in the user's own account, and the disclosure already mentions them, so this is fine. **Keep:** say "optional, skip anytime" when asking, and never repeat them in nudges (see finding 2).

**6. Children.** The plugin isn't designed for children. **Fix:** add one line to PRIVACY.md, "intended for adults; not directed to children under 13" (US COPPA) `[model knowledge — verify]`. Consider "under 16" for Europe `[review]`.

**7. Patreon supporter info.** Mindful receives supporter names and emails from Patreon. **Fix:** add one line to PRIVACY.md saying Mindful uses supporter info only to thank and update supporters, and never sells or shares it.

**8. PRIVACY.md header says version 0.8.0.** **Fix:** update it with each release.

**9. Anthropic directory rule 1G (memory and profiles).** The consent, see-it, and erase-it design addresses privacy best practice. Whether between-session memory is allowed in the directory is Anthropic's call. **Next step:** ask in the submission (the Mindful Rule proposal).

## 5. What applies, briefly `[model knowledge — verify]`

- **US state privacy laws** (California CCPA/CPRA, Texas TDPSA, others) apply to businesses above revenue or data-volume thresholds, or (in Texas) to non-small businesses. A free, one-person plugin that collects no user data is very likely outside them.
- **EU/UK GDPR** reaches non-EU businesses that offer services to people in the EU and process their personal data. Mindful processes very little (public feedback, Patreon supporter info), so obligations are light: a clear privacy notice, a way to make requests, and respect for deletion requests.
- **Texting (TCPA):** texts go only to the user's own verified number, at their request, so this is low risk.

## 6. Fix list

| # | Fix | When | Effort |
|---|---|---|---|
| 1 | Precise "Anthropic hosts it" wording + link | Next release | 5 min |
| 2 | Nudge privacy: PRIVACY.md line + generic-text rule | Next release | 15 min |
| 3 | Private contact for privacy requests | Next release (Ed picks address) | 5 min |
| 4 | Self-host website fonts | Next release | 15 min |
| 5–8 | "Optional" wording, children line, Patreon line, header version | Next release | 10 min |
| 9 | Ask Anthropic about rule 1G | At directory submission | — |

## 7. Sign-off

Prepared: 2026-10-26 · Reviewed by Ed Vita: ☐ · Attorney review (when available): ☐
