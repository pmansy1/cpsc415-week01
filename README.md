# Lyrics Trainer

A single-file memorization trainer for short texts. Shows one line at a time with a counter and a Next button. Built for [`lyrics.txt`](./lyrics.txt) (Sonnet 18) but the embedded text is easy to swap.

## Run

No build, no install, no server. Open `index.html` directly in any browser:

```
open index.html        # macOS
xdg-open index.html    # Linux
start index.html       # Windows
```

Or double-click the file in Finder/Explorer. The poem is embedded in the HTML, so the app works from `file://` with no network access.

## Controls

- **Next** — advance to the next line. After the last line, wraps to the first.
- **Restart** — jump back to line 1 from anywhere.
- **Tab** — move focus to a button.
- **Enter / Space** — activate the focused button.
- **→ (Arrow Right)** — anywhere on the page, advances like Next.

## Files

- `index.html` — the whole app (HTML + CSS + JS in one file).
- `lyrics.txt` — the source poem. Not loaded at runtime; the same lines are embedded inside `index.html`.

## Customize

To train a different text, edit the `rawText` template literal inside the `<script>` block in `index.html`. Use one line of text per line in the template, then update the line count expectation if you want to be precise. Blank lines are filtered out automatically.

## Tech

Plain HTML, CSS, and vanilla JavaScript. No frameworks, packages, build step, or API calls.
