---
name: after-the-call
description: Use when someone has just given a presentation, client call, demo, pitch or talk and wants to reflect on it, asks "how can I do better next time", "help me get oriented", "debrief the meeting", feels it went badly or "delivered it dry", or shares a meeting transcript, recording notes or slides after a call. Also when they ask to turn the learnings into something cute or cheerful.
---

# After the call 🌱

A kind, specific debrief after a presentation, then (if wanted) a cute page or slide deck of the learnings. Pairs well with `sparkle-that-page` (cute effects) and `huashu-design` (design directions).

**Core principle:** the reader is often tired and down. Advice lands only if it is true, specific, and starts from what worked.

## The reply, in this order

1. **Where it stands** (3 to 5 bullets). What the audience actually decided or asked for, quoted with timestamps. What any "pause" or "no" is literally about. The next meeting or send that is already booked.
2. **What went well** (2 or 3 items). Each one quotes the audience's own words with a timestamp. Required, even when it went badly.
3. **Spoken figures vs the slides** (only if they differ). See the rule below.
4. **Presenting**: at most 5 changes. Each one: what to do, plus the timestamp where it would have helped ("At 9:30 they asked which one first; the options came at 24:00").
5. **Workflow**: at most 4 changes, split by who owns them. If an AI or a teammate built the deck, name what *they* should do differently (for example, adding features on call day, or twenty versions in one day). Do not put the whole load on the presenter.
6. **Time**: 1 or 2 changes (for example, the last 2 to 3 hours before a call are for one timed run-through out loud, and food).
7. **One next action**, doable today. Default: prepare for the next meeting already booked.
8. **Offer the cheer-up page** in one line (below). Skip it if the person is not in the mood.

Acknowledge feelings in one plain sentence: "Feeling flat after that makes sense." No pep talk.

**Length:** the whole reply stays under 600 words. Cut the weakest change before cutting a timestamp.

**Data problems you spot** (a small group, counts that do not add up) are not presenting advice. Put at most two in one line, "Before the deck goes out:", after the next action.

**Owner unknown:** if nothing says who built the deck, write "you, or whoever builds the deck (an AI included)". Do not guess.

## Spoken figures: transcription first

Auto transcripts garble numbers ("seventeen" becomes "seventy", "fifteen" becomes "fifty").

| Transcript figure vs slide | What you write |
|---|---|
| Sounds like the slide figure (17 vs "seventy") | A transcription error. Say so. Do not coach the speaker on it. |
| Partly garbled ("fifty fifty-five" for 15) | Treat it as transcription, and invite the speaker to correct you in one clause. |
| Unrelated to anything on the slide | Ask the speaker what they said. Do not assume a slip. |
| Either case | If the AI meeting summary repeats the wrong figure, give the slide figure for the follow-up email. |

Never write "say the numbers exactly as on the slide" unless the speaker confirms they misspoke. If they correct you, accept it and update any notes.

## The cheer-up page (when asked)

Read `cheer-page-recipe.md` in this folder. In short: write one content file first. Show three styles (garden, scrapbook, cozy quest). Build the chosen ones with `huashu-design` for direction and `sparkle-that-page` for effects if installed; plain HTML and CSS work too. Then look at every screen yourself.

## Common mistakes

| Mistake | Fix |
|---|---|
| Ten tips in one wall | Caps above. Rank and cut the rest. |
| Advice with no evidence | Every change carries a timestamp or a quote. |
| "They're not sold" accepted as fact | Check the transcript for what they said; a pause is not a rejection. |
| Presenter blamed for team or AI choices | Split workflow changes by owner. |
| Generic tips ("know your audience") | Only changes this transcript supports. |
| Made-up rules of thumb ("25 minutes of content for a 45-minute slot") | Every number in the advice comes from the transcript, the slides or the chat. |

## Afterwards

If memory or persona files exist for this client, offer to update them with what the audience revealed (how they decide, what they asked first). Quote, date, never overwrite.

## Changelog

- 1.0.1, 2026-11-20: examples are now invented.
- 1.0.2, 2026-11-20: every cheer-up style gets its own tab icon (the scrapbook demo had none).
- 1.0.0, 2026-11-19: written after a real client call and tested on a made-up call (3 runs without the skill, 3 with, 3 after tightening). Without it: 1 of 3 coached the speaker on a speech-to-text error, 0 of 3 had a "went well" section, 0 of 3 offered a cheer-up page, and replies ran to about 1,000 words. With it: none coached, all three had both, and the tightened version came in at 520 to 538 words.
