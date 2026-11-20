# Cheer-up page recipe

First built after a client call: three single-file HTML pages (garden, scrapbook, cozy quest),
each later turned into a slide deck. The person kept all three.

## 1. Content first, one file

Write `content.md` in a Desktop folder named `<date> <Name> — call learnings/`. It holds the text every style shares:

- Title: "You did a hard thing today." plus one line on what they delivered. After a clear "no", use a plainer title ("Here is what we learned.") and skip the confetti.
- What the audience actually said (3 or 4 quotes, words only, no timestamps on the page). First names only, no company names or figures, unless the person asks for them.
- What the pause or outcome really means (one short card).
- What went well (2 or 3).
- Presenting: the changes (at most 5).
- Workflow: the changes (at most 4), with a note on which are the AI's side.
- Time (one line), plus "Pick a stop time and write it down."
- Tomorrow: the next meeting as a checklist, and the opening sentences to bring.
- Closing: "Now go and eat something." (adapt it to them).

Every style uses this text word for word, so the content cannot drift between versions.

The page holds a client's words. Keep it on the person's machine. Before hosting it anywhere public or emailing it to others, ask.

## 2. Three styles, then build

Show three directions before building, and record the person's choice in `direction-approved.md`. [huashu-design](https://github.com/alchaincyf/huashu-design) does this well if installed. The three that landed:

| Style | Look | Moving parts |
|---|---|---|
| Garden | Sky, hills, a seedling mascot, a flower per win, a noodle bowl at the end | Seedlings sprout, petals drift, sun bobs |
| Scrapbook | Paper, washi tape, polaroids, a rice-ball mascot, sticky notes | Polaroids pin in one by one, tap gold stars, tick boxes |
| Cozy quest | Pixel art, night sky, level-up banner, inventory slots | Trophy fills a slot per win, "I tried it" XP bars, campfire save screen |

If they love more than one, keep them all (separate files).

Every style gets its own cute tab icon, drawn from its mascot (the seedling, the rice ball, the pixel face). Put it inline as `<link rel="icon" href="data:image/svg+xml,...">`, so the file still needs nothing beside it. Draw it for 16 px: thicker outlines, bigger eyes, no fine detail. [cutify-that-tab](https://github.com/wan-huiyan/cutify-this) does this well if installed. A page without one shows the browser's grey globe in the tab, and that is the first thing the person sees.

Effects come from [sparkle-that-page](https://github.com/wan-huiyan/cutify-this) if installed, or hand-written CSS: confetti only on celebratory elements, floaters behind the content, and everything off under `prefers-reduced-motion`.

## 3. Slide version (if asked)

- One file per style, 1920x1080 stage scaled to fit.
- Arrow keys, swipe, and F for full screen. Number the slides.
- Reveal steps for lists, so one quote or win appears per arrow press.
- Ticks and XP saved in localStorage.
- Keep a portrait layout for phones.

## 4. Check before showing

- Screenshot every slide at 1920 and 390, plus one run with reduced motion. Make a contact sheet and look at it yourself.
- Step through every reveal step and screenshot the last step. A frame that is still empty in a still image may be a reveal that never fires.
- Every file has its own `rel="icon"`. Render each icon at 16 and 32 px on a light and a dark background, side by side, and look at them: each should read as its mascot.
- No page errors in the browser console (and `design_lint.py check` if huashu-design is installed).
- Open the files for the person with `open`, and tell them in one line how to move through them.
