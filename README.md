# sparring-scoreboard

A single-file dual score counter with an editable countdown timer, built for running scorekeeping at G-Elite martial arts tournaments. It is deliberately simple and works the same on a laptop, an iPad, or a phone (the phone is what we ended up using courtside).

## What it does

- Two independent score columns, each with `+1` / `-1` buttons. The `-1` button disables at zero so a score can't go negative.
- An editable countdown timer (minutes + seconds, capped at 10:00). Start and Pause control it; the display turns red in the final 20 seconds.
- A Reset button that zeroes both scores and returns the timer to its 2:00 default.
- Responsive layout that keeps both columns side by side and fills the viewport without scrolling, tuned for phone widths down to ~320px.

Everything is self-contained in `score.html`: no build step, no dependencies, no network calls, no stored state. Open the file in any browser and it runs.

## Source

The source committed here is the clean app. The copy served from the live host has two Cloudflare-injected snippets (a hidden anchor after `<body>` and the challenge-platform script before `</body>`); those are inserted at serve time and are not part of the source, so they were stripped before the first commit.

## Use

Open `score.html` in a browser, or host it as a static file. There is no deploy pipeline in this repo.
