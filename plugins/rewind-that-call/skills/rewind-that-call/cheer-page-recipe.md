# Cheer-up page recipe

First built after a client call: three single-file HTML pages (garden, scrapbook, cozy quest),
each later turned into a slide deck. The person kept all three.

This is a method, not a script. The words on the page are yours, written for this person and this call.

## 1. Content first, one file

Write one content file (for example `content.md`) in a folder the person can find, named with the date and their first name. It holds the text every style shares. Cover, in your own words:

- A title and one line on what they delivered: warm and true to how the call went. After a clear "no", keep it plainer and skip the confetti.
- What the audience actually said: up to 4 short quotes, all from the debrief (fewer if fewer exist), words only, no timestamps on the page. First names only, no company names or figures, unless the person asks for them.
- What the pause or outcome really means (one short card).
- What went well (2 or 3).
- Presenting changes (at most 5).
- Workflow changes (at most 4), noting which are the AI's side.
- Time (one line, only if the debrief had a Time change; reuse it). If that change is about stopping prep, the behaviour is choosing a stop time and writing it down.
- What comes next: the next meeting as a checklist, and a suggested opening for it.
- A short, kind closing that fits them (rest, food, a break), not a stock sign-off.

The content file carries the same caps as the debrief (at most 5 presenting changes, 4 workflow changes) and nothing the debrief did not say. Every style uses this file verbatim, so the content cannot drift between versions. That consistency is the point of writing it first.

The page holds a client's words. Keep it on the person's machine. Before hosting it anywhere public or emailing it to others, ask.

## 2. Three styles, then build

Show three directions before building, and record the person's choice in a small file beside the content (for example `direction-approved.md`). A design-directions helper such as [huashu-design](https://github.com/alchaincyf/huashu-design) does this well if installed. The three that landed the first time, as a starting point, not a requirement:

| Style | Look | Moving parts |
|---|---|---|
| Garden | Sky, hills, a seedling mascot, a flower per win | Seedlings sprout, petals drift, sun bobs |
| Scrapbook | Paper, washi tape, polaroids, a small mascot, sticky notes | Polaroids pin in one by one, tap stars, tick boxes |
| Cozy quest | Pixel art, night sky, a pixel-face mascot, level-up banner, inventory slots | A slot fills per win, progress bars for things tried, a save screen |

If they love more than one, keep them all (separate files).

Each style has its own mascot or main motif (any you choose), and its own cute tab icon drawn from it. Put it inline as `<link rel="icon" href="data:image/svg+xml,...">`, so the file needs nothing beside it. Draw it for 16 px: thicker outlines, bigger eyes, no fine detail. [cutify-that-tab](https://github.com/wan-huiyan/cutify-this) does this well if installed. A page without one shows the browser's default icon in the tab, and that is the first thing the person sees.

Effects come from [sparkle-that-page](https://github.com/wan-huiyan/cutify-this) if installed, or hand-written CSS: confetti only on celebratory elements, floaters behind the content, and everything off under `prefers-reduced-motion`.

## 3. Slide version (if asked)

- One file per style, 1920x1080 stage scaled to fit.
- Arrow keys, swipe, and F for full screen. Number the slides.
- Reveal steps for lists, so one quote or win appears per arrow press.
- Ticks and progress saved in localStorage.
- Keep a portrait layout for phones.

## 4. Check before showing

- If you have no browser tool, say which of these checks you could not run and list them for the person; do not call the page checked.
- Screenshot every slide at 1920 and 390 px wide, plus one run with reduced motion. Make a contact sheet and look at it yourself.
- Step through every reveal step and screenshot the last step. A frame still empty in a still image may be a reveal that never fires.
- Every file has its own `rel="icon"`. Render each icon at 16 and 32 px on light and dark backgrounds, side by side, and look: each should read as its style's mascot or main motif.
- No errors in the browser console (and the design helper's own lint if installed; for huashu-design: `design_lint.py check`).
- Every style shows the same words as the content file.
- Open the files for the person if you can; otherwise give the full paths. Tell them in one line how to move through them.
