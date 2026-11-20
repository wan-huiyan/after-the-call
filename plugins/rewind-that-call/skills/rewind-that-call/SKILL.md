---
name: rewind-that-call
description: Use when someone has just given a presentation, client call, demo, pitch or talk and wants to reflect on it, asks "how can I do better next time", "help me get oriented", "debrief the meeting", feels it went badly or "delivered it dry", or shares a meeting transcript, AI meeting summary, recording notes or slides after a call, even with no transcript at all (it can find the meeting's notes through a Google Drive or Calendar connector). Also when they ask to turn the learnings into something cute or cheerful, or what their AI assistant (Claude, Codex, Cursor or another) should do differently next time it builds a deck.
---

# Rewind that call 🌱

A kind, specific debrief after a presentation, then (if wanted) a cute page or slide deck of the learnings, and lessons for the AI agent from the session that built the deck. Written for any agent; "you" means the agent reading this. Optional helpers if installed: `sparkle-that-page` (cute effects) and `huashu-design` (design directions).

**Core principle:** the reader is often tired and down. Advice lands only if it is true, specific, and starts from what worked. True comes first: never invent praise, a quote or a minute.

**These are principles, not a script.** Choose your own headings, titles and sentences for this person and this call. Nothing below is text to copy; where an example appears, it shows the idea only. Commands, file names and search syntax are exact; everything a person reads is yours to word.

## Check the input first

| What you have | What you do |
|---|---|
| Nothing handed over, and no Google Drive or Calendar tool available | Before anything else, ask (see "First run: get the transcript" below). |
| Nothing handed over, but a Google Drive or Calendar tool (connector or MCP server) is available | Find the meeting's notes yourself (below), then come back to this table. |
| A raw transcript with timestamps | The reply below, in full. |
| An AI meeting summary only (Gemini, Otter, Zoom, Teams notes) | Say so in one line. Never present the summary's wording as the audience's own words and never invent a minute; mark such points as coming from the summary, with no timestamp. Skip the spoken-figures check unless the summary quotes a figure. |
| Notes or memory only | Ask one short question each about where things stand and what went well (for example, what was said at the end, what they asked about most), then reply without timestamps. |
| Timestamps that look offset (recording started late, times run past the call length) | Ask once for the offset before quoting minutes. |

Every timestamp you write must appear in the input. If you cannot point to it, leave the minute out.

### First run: get the transcript

The debrief is only as good as its input, and a full transcript with timestamps is what makes it specific. When nothing was handed over and you have no Drive or Calendar tool, do not start from memory. Ask the person, in your own words and in one short message, which they would like:

- **Connect Google Calendar or Drive**, so this and future calls can be found automatically. Ask permission before guiding them. Gemini's meeting notes live in Drive (Calendar only links to them), so Drive is the one that matters. Guide them through your own agent's way of adding a connector or MCP server, step by step, without assuming a menu you have not seen; if you do not know how your agent does it, say so and point them to its documentation. Never ask them to paste passwords, tokens or keys into the chat. Once it is connected, carry on from "Finding the call's notes yourself".
- **Send the full transcript** now (from Google Meet's notes doc, Zoom, Teams, Otter or similar), ideally the timestamped one rather than a summary.
- **Go ahead without one**, from their notes or memory, knowing the debrief will have no timestamps (the notes-only row above).

Ask once. If they pick an option, follow it; if they decline to set anything up, do not ask again in this conversation. If your agent keeps notes or memory between sessions, offer to record their choice so a later debrief does not ask again, and record it only on a yes.

### Finding the call's notes yourself

Google Meet saves a "Notes by Gemini" doc to the organiser's Drive, linked from the Calendar event. Tested on a real call (2026-11-19) through a Drive connector; any Drive tool or MCP server should work the same way:

1. Search Drive for docs titled "Notes by Gemini" changed on the call's day, using whatever search form your Drive tool takes (plain keywords on some; with the Drive API query syntax, for example: `title contains 'Notes by Gemini' and modifiedTime > '<call date>T00:00:00'`). With a Calendar tool, the event's attachments should point to the same doc (this route is not tested yet); match on meeting title and start time.
2. Read the doc. It usually holds the summary and, under a Transcript heading, the full transcript with `hh:mm:ss` timestamps. Work from the transcript, not the summary. No transcript inside means the summary-only row applies.
3. Tell the person in one line which doc you used (title and date), so they can check it is the right call.
4. The notes may sit on a different account from the one connected (a work account). If nothing turns up, ask for the file rather than guess.

## The reply: order of content

Name each part in your own words. The order matters more than the labels: outcome first so they know where they stand, then what worked so the changes land.

1. **Where things stand** (3 to 5 points). What the audience actually decided or asked for, quoted with timestamps. What any pause or "no" is literally about, marked as **stated** (they said why; quote it), **inferred** (your reading) or **unknown**. If a "no" is ambiguous, give both readings. Any next meeting or send already booked.
2. **What went well** (2 or 3). Each quotes the audience's own words with a timestamp. If nobody said anything positive, name something they did (stayed past time, asked a follow-up, booked the next step). If there is nothing at all, say plainly that there is little to quote and move on. Never invent praise.
3. **Spoken figures vs the slides**, only if they differ. See the rule below.
4. **Presenting**: at most 5 changes. Each says what to do and where it would have helped: a timestamp if the input has them; otherwise the moment described in the person's own words, labelled as from their notes or the summary.
5. **Workflow**: at most 4 changes, split by who owns them. If an AI or a teammate built the deck, name what *they* should do differently (late features on call day, many versions in one day). Do not put the whole load on the presenter. Use what this conversation with the person shows, too (late changes, corrections), not only the transcript.
6. **Time**: 0 to 2 changes. Leave the section out if nothing in the transcript, the meeting chat or your conversation with the person shows how prep went. No rule of thumb the evidence does not support. (An idea, not wording: if the evidence shows the deck still changing late, the change might be to protect time before the next call for one timed run-through out loud.)
7. **One next action**, doable today. Default: prepare for the meeting already booked. After a clear "no", make it about recovery (a short thank-you, one question about what would change their mind, or closing cleanly).
8. **Two short offers**, one line each, in your own words: the cheer-up page, and lessons for the agent from the build session if an AI built the deck. Skip the cheer-up offer after a clear "no", or if the person has said they want only the debrief or seems upset in their own words, unless they ask; otherwise offer.

**Feelings:** acknowledge how they feel in one plain, honest sentence that fits what they told you. No pep talk, no stock comfort line.

**Length:** the whole reply stays under 600 words. Cut the weakest change before cutting a timestamp.

**Data problems you spot** (a small group, counts that do not add up) are not presenting advice. Put at most two in one line after the next action, framed as things to fix before the deck goes out again.

**Owner unknown:** if nothing says who built the deck, address the change to the presenter or whoever builds the deck, an AI included. Do not guess.

## When it really did go badly

A clear "no", a factual error the audience caught, or a tense exchange. Then:

- State the outcome first, in their words. Do not reframe it as a pause.
- What went well uses the fallback in step 2 (a behaviour, or little to quote). Do not stretch.
- Keep the changes to what would have changed the outcome, not polish.
- Plainer tone throughout. No cheer-up offer unless asked.

## Spoken figures: transcription first

Auto transcripts garble numbers ("seventeen" becomes "seventy", "fifteen" becomes "fifty"), names, and small words ("can" and "can't").

| Transcript vs slide | What to conclude |
|---|---|
| Sounds like the slide figure (17 vs "seventy") | A transcription error. Say so. Do not coach the speaker on it. |
| Partly garbled ("fifty fifty-five" for 15) | Do not conclude. Say it is probably transcription and ask the speaker to confirm in one clause. |
| The audience reacted to the spoken figure (asked about it, repeated it, corrected it) | They heard it, so it was probably said. Treat it as a real slip, kindly, and quote their reaction. |
| Unrelated to anything on the slide | Ask the speaker what they said. Do not assume a slip. |
| Any case | If the AI meeting summary repeats the wrong figure, give the slide figure for any follow-up message. |

Never tell the speaker to say numbers exactly as on the slide unless they confirm they misspoke or the audience reacted. If they correct you, accept it and update any notes.

## The cheer-up page (when asked)

Read `cheer-page-recipe.md` in this folder. In short: write one shared content file in your own words for this person; offer three styles; build the chosen ones (with design or effects helpers if installed, plain HTML and CSS otherwise); then look at every screen yourself. If you have no browser tool, say which checks you could not run and list them for the person; do not call the page checked.

## Lessons for the agent from the build session (when asked)

If an AI coding agent built or edited the deck, its session log shows what happened on the AI's side: how many versions, how late the last change came, what the person had to correct. Offer to look, in one line after the reply. Reading the logs is opt-in. The log script is for sessions you cannot see; if the build happened in this conversation, use what you can already see instead. This part sits outside the 600-word reply.

1. Run `scripts/session_evidence.sh <deck file name> <call start in UTC>` from this skill's folder (the one holding this file). It needs a bash shell and `jq`, plus `sqlite3` for Cursor. If you cannot run it (no shell, Windows, a missing tool), say the build-session lessons were skipped and why; do not report "no log found". It reads only Claude Code, Codex and Cursor logs; if another agent built the deck, say its log could not be read, rather than that it showed nothing, and write no items. Use the deck's real file name (ask if unsure); a wrong name finds nothing. It searches Claude Code logs (`~/.claude/projects/`, all worktrees), Codex logs (`~/.codex/sessions/`) and Cursor's chat database for anything from the last 7 days mentioning the deck (`DAYS=14` for longer), and prints only counts, edit and build times, and the person's own short messages. The Claude Code reader is tested; the Codex and Cursor readers are written from those tools' storage formats and have not been run on a real session, so label any evidence from them "(Codex/Cursor reader, untested)". It takes a minute or two. Never read a raw log: they are huge and tool output can hold secrets.
2. Look for: direct edits and build commands (a deck made by a script shows up as commands, not edits), how many came on call day and in the last hour before the call, features added late, the person correcting the same thing twice, deadlines the person stated.
   If the script finds no log, or no edits and no build commands, say so in one line and write no items.
3. Write at most 5 items, under a heading of your choosing. Each one:
   - cites its evidence with the log timestamp (for example, a count of edits on call day and the time of the last one);
   - is a rule ready to save: it states the rule, why it matters, and when to apply it, laid out in the format of the file it will be saved to;
   - addresses the person as "you", never "he" or "she";
   - records the pattern only, never client names, quotes, figures, file names or project folder names, which often name the client.
4. Ask before saving. On a yes, save each to whatever notes, memory or rules file the person's agent uses, in that file's existing format, one per file if that is the layout. Never overwrite an existing entry; add to it.

## Common mistakes

| Mistake | Fix |
|---|---|
| Ten tips in one wall | Caps above. Rank and cut the rest. |
| Advice with no evidence | Every change carries a timestamp, a quote, or (without either) the moment in the person's own words, labelled by source. |
| A timestamp that is not in the input | Leave the minute out. Summaries have none. |
| "They're not sold" accepted as fact | Check the transcript for what they said; a pause is not a rejection unless they said so. |
| "It's just a pause" when they said no | State the outcome first, in their words. |
| Praise made up to fill what went well | Quote, name a behaviour, or say there is little to quote. |
| Presenter blamed for team or AI choices | Split workflow changes by owner. |
| Generic tips ("know your audience") | Only changes this transcript supports. |
| Made-up rules of thumb ("25 minutes of content for a 45-minute slot") | Every number in the advice comes from the transcript, the slides, the meeting chat or your conversation with the person. |
| Copying example wording or headings as fixed text | Write for this person and this call. |
| Client quotes saved to notes or memory | Save the pattern, not the quote, and only on a yes. |

## Privacy

The transcript is usually a client's words. Work only from files the person gives you, or the meeting's own notes found through their connected Drive or Calendar. Do not paste quotes into anything shared or hosted (a public page, an email to others, a gist) without asking. The cheer-up page uses first names only by default.

## Afterwards

If notes, memory or persona files exist for this client, offer to update them with what the audience revealed (how they decide, what they asked first). Ask first, save the pattern rather than verbatim quotes or figures, date it, never overwrite.

## Changelog

- 1.4.0, 2026-11-20: first run, with no transcript and no Drive or Calendar tool, the agent asks once whether to guide the person through connecting Drive or Calendar, have them send the full transcript, or go ahead without one; it remembers the choice only on a yes.
- 1.3.0, 2026-11-20: principles, not a script. Removed every fixed phrase, title and heading the agent was told to say or display; each is now the principle behind it, and the agent writes its own words for the person and the call. Agent-neutral throughout (any agent, not only Claude); saving goes to whatever notes, memory or rules file the person's agent uses. The cheer-up recipe now lists what to cover, not what to write. Rule changes: Time is 0 to 2 changes and is left out without evidence; saved lessons follow the target file's format rather than fixed Why / How-to-apply lines; input without timestamps anchors changes to the person's own words; the agent uses the conversation it is in as evidence for Workflow and Time; a missing shell, browser or unsupported agent is reported as a skipped check, never as "nothing found"; cheer-page quotes are up to 4 and the Time line appears only when the debrief had one.
- 1.2.0, 2026-11-20: finds the call's notes through a Google Drive or Calendar connector when none is handed over (tested on a real call); the session-log script also reads Codex and Cursor (both readers untested).
- 1.1.0, 2026-11-20: renamed from after-the-call. New: an input check (summary-only and notes-only input never get invented timestamps), a branch for calls that really did go badly, a stricter spoken-figures table (partly garbled means ask; an audience reaction means a real slip; names and "can/can't" too), a Time rule that needs evidence, privacy rules, and lessons for Claude from the build session via `scripts/session_evidence.sh`.
- 1.0.2, 2026-11-20: every cheer-up style gets its own tab icon (the scrapbook demo had none).
- 1.0.1, 2026-11-20: examples are now invented.
- 1.0.0, 2026-11-19: written after a real client call and tested on a made-up call (3 runs without the skill, 3 with, 3 after tightening). Without it: 1 of 3 coached the speaker on a speech-to-text error, 0 of 3 had a "went well" section, 0 of 3 offered a cheer-up page, and replies ran to about 1,000 words. With it: none coached, all three had both, and the tightened version came in at 520 to 538 words.
