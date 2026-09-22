# Lyrics Trainer

A single-file memorization trainer for short texts. Shows one line at a time with a counter and a Next button. Built for [`lyrics.txt`](./lyrics.txt) (Sonnet 18) but the embedded text is easy to swap.

## Run

No build, no install, no server. Open `index.html` directly in any browser:

```
open index.html        # macOS
start index.html       # Windows
```

## Tools Used
- **Harness** - Claude Code CLI
- **Model** -  minimax/minimax-m3

## Chosen Change
- My chosen change was the restart button; I want this because it allows the user to immediately go back to the beginning of the card deck from their current position.

## Usage Evidence
- I used  $0.28 to complete this lab, according to my OpenRouter activity page

## Help Needed
- Originally, I was getting an 401 / authentication failure and decided to manually input my open router api key into my zshrc file, which solved the issue

## In the Code

A `keydown` listener at the bottom of the script maps `ArrowRight` to `advance()`, so Next works from anywhere on the page. Native `<button>` elements only fire Enter/Space while focused — without this listener, the user would have to Tab to the button before pressing →.


