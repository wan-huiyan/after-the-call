---
name: rewind-that-call
description: Use when someone has just given a presentation, client call, demo, pitch or talk and wants to reflect on it, asks "how can I do better next time", "help me get oriented", "debrief the meeting", feels it went badly or "delivered it dry", or shares a meeting transcript, AI meeting summary, recording notes or slides after a call, even with no transcript at all. Also when they ask to turn the learnings into something cute or cheerful, or what Claude should do differently next time it builds a deck.
---

# Rewind that call 🌱

A kind, specific debrief after a presentation, then (if wanted) a cute page or slide deck of the learnings, and lessons for Claude from the session that built the deck. Pairs well with `sparkle-that-page` (cute effects) and `huashu-design` (design directions).

**Core principle:** the reader is often tired and down. Advice lands only if it is true, specific, and starts from what worked. True comes first: never invent praise, a quote or a minute.

## Check the input first

| What you have | What you do |
|---|---|
| A raw transcript with timestamps | The reply below, as written. |
| An AI meeting summary only (Gemini, Otter, Zoom, Teams notes) | Say so in one line. Never present the summary's wording as the audience's own words, and never invent a minute: mark points "(from the summary, no timestamp)". Skip the spoken-figures check unless the summary quotes a figure. |
| Notes or memory only | Ask one question each for "Where it stands" and "What went well" (what did they say at the end? what did they ask about most?), then give the reply without timestamps. |
| Timestamps that look offset (the recording started late, or times run past the call length) | Ask once for the offset before quoting minutes. |

Every timestamp you write must appear in the input. If you cannot point to it, leave the minute out.

## The reply, in this order

1. **Where it stands** (3 to 5 bullets). What the audience actually decided or asked for, quoted with timestamps. What any "pause" or "no" is literally about, marked as **stated** (they said why, quote it), **inferred** (your reading) or **unknown**. If a "no" is ambiguous, give both readings. The next meeting or send that is already booked.
2. **What went well** (2 or 3 items). Each one quotes the audience's own words with a timestamp. If nobody said anything positive, name something they did (stayed past time, asked a follow-up, booked the next step). If there is nothing at all, say plainly "there is little to quote this time" and move on. Never invent praise.
3. **Spoken figures vs the slides** (only if they differ). See the rule below.
4. **Presenting**: at most 5 changes. Each one: what to do, plus the timestamp where it would have helped ("At 9:30 they asked which one first; the options came at 24:00").
5. **Workflow**: at most 4 changes, split by who owns them. If an AI or a teammate built the deck, name what *they* should do differently (for example, adding features on call day, or twenty versions in one day). Do not put the whole load on the presenter.
6. **Time**: 1 or 2 changes, only from what the chat or transcript shows about prep (for example, if the deck was still changing in the last hour: keep the time before the next call for one timed run-through out loud, and food). No rule of thumb the evidence does not support.
7. **One next action**, doable today. Default: prepare for the next meeting already booked. After a clear "no", the next action is about recovery (a short thank-you, one question about what would change their mind, or closing it cleanly).
8. **Two one-line offers** (below): the cheer-up page, and lessons for Claude from the build session if Claude built the deck. Skip the cheer-up page after a clear "no" or if the person is not in the mood, unless they ask.

Acknowledge feelings in one plain sentence: "Feeling flat after that makes sense." No pep talk.

**Length:** the whole reply stays under 600 words. Cut the weakest change before cutting a timestamp.

**Data problems you spot** (a small group, counts that do not add up) are not presenting advice. Put at most two in one line, "Before the deck goes out:", after the next action.

**Owner unknown:** if nothing says who built the deck, write "you, or whoever builds the deck (an AI included)". Do not guess.

## When it really did go badly

A clear "no", a factual error the audience caught, or a tense exchange. Then:

- State the outcome first, in their words. Do not reframe it as a pause.
- "What went well" follows the fallback in step 2 (a behaviour, or "little to quote"). Do not stretch.
- Keep the changes to what would have changed the outcome, not polish.
- Plainer tone throughout. No cheer-up offer unless asked.

## Spoken figures: transcription first

Auto transcripts garble numbers ("seventeen" becomes "seventy", "fifteen" becomes "fifty"), names, and small words ("can" and "can't").

| Transcript vs slide | What you write |
|---|---|
| Sounds like the slide figure (17 vs "seventy") | A transcription error. Say so. Do not coach the speaker on it. |
| Partly garbled ("fifty fifty-five" for 15) | Do not conclude. Say it is probably transcription and ask the speaker to confirm in one clause. |
| The audience reacted to the spoken figure (asked about it, repeated it, corrected it) | They heard it, so it was probably said. Treat it as a real slip, kindly, and quote their reaction. |
| Unrelated to anything on the slide | Ask the speaker what they said. Do not assume a slip. |
| Any case | If the AI meeting summary repeats the wrong figure, give the slide figure for the follow-up email. |

Never write "say the numbers exactly as on the slide" unless the speaker confirms they misspoke or the audience reacted to it. If they correct you, accept it and update any notes.

## The cheer-up page (when asked)

Read `cheer-page-recipe.md` in this folder. In short: write one content file first. Show three styles (garden, scrapbook, cozy quest). Build the chosen ones with `huashu-design` for direction and `sparkle-that-page` for effects if installed; plain HTML and CSS work too. Then look at every screen yourself.

## Lessons for Claude from the build session (when asked)

If Claude Code built or edited the deck, its session log shows what happened on Claude's side: how many versions, how late the last change came, what the person had to correct. Offer it in one line after the reply: "Want me to look at the session that built the deck and write down what I should do differently next time?" Reading the logs is opt-in. This part sits outside the 600-word reply.

1. Run `scripts/session_evidence.sh <deck file name> <call start in UTC>` from this folder. Use the deck's real file name (ask if unsure); a wrong name finds nothing. It searches `~/.claude/projects/` (all worktrees) for logs from the last 7 days that mention the deck (`DAYS=14` for longer), and prints only counts, edit and build times, and the person's own short messages. It takes a minute or two. Never read a raw log: they are huge and tool output can hold secrets.
2. Look for: direct edits and build commands (a deck made by a script shows up as commands, not edits), how many came on call day and in the last hour before the call, features added late, the person correcting the same thing twice, deadlines the person stated.
   If the script finds no log, or no edits and no build commands, say so in one line ("no session log shows the deck being built, so there is nothing to learn from on my side") and write no items.
3. Write at most 5 items under **For Claude next time**. Each one:
   - cites the evidence with its log timestamp ("14 deck edits on call day, the last at 13:52 UTC, eight minutes before the call");
   - is written as a rule ready to save, with a **Why** and a **How to apply** line;
   - records the pattern only, never client names, quotes, figures, file names or project folder names, which often name the client ("freeze the deck the evening before a client call", not the client's numbers).
4. Ask before saving. On a yes, save each as a memory or lesson in the person's own format, one per file if that is their layout. Never overwrite an existing entry; add to it.

## Common mistakes

| Mistake | Fix |
|---|---|
| Ten tips in one wall | Caps above. Rank and cut the rest. |
| Advice with no evidence | Every change carries a timestamp or a quote. |
| A timestamp that is not in the input | Leave the minute out. Summaries have none. |
| "They're not sold" accepted as fact | Check the transcript for what they said; a pause is not a rejection unless they said it is. |
| "It's just a pause" when they said no | State the outcome first, in their words. |
| Praise made up to fill "What went well" | Quote, or name a behaviour, or say there is little to quote. |
| Presenter blamed for team or AI choices | Split workflow changes by owner. |
| Generic tips ("know your audience") | Only changes this transcript supports. |
| Made-up rules of thumb ("25 minutes of content for a 45-minute slot") | Every number in the advice comes from the transcript, the slides or the chat. |
| Client quotes saved to memory | Save the pattern, not the quote, and only on a yes. |

## Privacy

The transcript is usually a client's words. Work only from the files the person gives you. Do not paste quotes into anything shared or hosted (a public page, an email to others, a gist) without asking. The cheer-up page uses first names only by default.

## Afterwards

If memory or persona files exist for this client, offer to update them with what the audience revealed (how they decide, what they asked first). Ask first, save the pattern rather than verbatim quotes or figures, date it, never overwrite.

## Changelog

- 1.1.0, 2026-11-20: renamed from after-the-call. New: an input check (summary-only and notes-only input never get invented timestamps), a branch for calls that really did go badly, a stricter spoken-figures table (partly garbled means ask; an audience reaction means a real slip; names and "can/can't" too), a Time rule that needs evidence, privacy rules, and lessons for Claude from the build session via `scripts/session_evidence.sh`.
- 1.0.2, 2026-11-20: every cheer-up style gets its own tab icon (the scrapbook demo had none).
- 1.0.1, 2026-11-20: examples are now invented.
- 1.0.0, 2026-11-19: written after a real client call and tested on a made-up call (3 runs without the skill, 3 with, 3 after tightening). Without it: 1 of 3 coached the speaker on a speech-to-text error, 0 of 3 had a "went well" section, 0 of 3 offered a cheer-up page, and replies ran to about 1,000 words. With it: none coached, all three had both, and the tightened version came in at 520 to 538 words.
