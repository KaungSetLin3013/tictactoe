# ⚔️ The Reckoning

A gothic-themed twist on tic-tac-toe, in a single self-contained HTML file. No build step, no dependencies to install — open it in a browser and play.

The twist: marks don't last forever. Each player may only have **3 marks on the board at once** — place a 4th, and your oldest mark vanishes. It turns the familiar 3×3 grid into a constantly shifting puzzle where you have to think a move or two ahead of your own disappearing pieces, not just your opponent's.

## ✨ Features

- **Two game modes**
  - **Solo — Challenge the Oracle**: play against an AI opponent
  - **Duel — Two Players**: pass-and-play on the same device
- **Vanishing marks mechanic** — only the 3 most recent marks per player stay on the board; placing a 4th makes the oldest fade away. The mark about to vanish pulses as a warning before your next move.
- **Vanish-aware AI** — the Oracle uses a depth-limited minimax search that simulates the vanishing rule itself, so it plays correctly around its own and the player's disappearing marks rather than just optimizing for a static board.
- **Score tracking** — running win/draw/loss tallies for both solo and duel modes, with a reset option.
- **Animated win line** and a full-screen victory/draw overlay with a "Play Again" / "Return to Menu" choice.
- **Gothic visual theme** — candle-flicker accents, Cinzel/IM Fell English typography, parchment-and-ink color palette, ornamental card borders.

## 🎮 How to play

Standard tic-tac-toe rules apply — get three of your marks in a row, column, or diagonal — with one addition:

> Once you have 3 marks on the board, placing a new one removes your **oldest** mark first. Watch for the pulsing cell — that's the mark about to disappear on your next turn.

1. Open `index.html` in a browser (works on desktop and mobile).
2. Choose **Solo** to play against the Oracle, or **Duel** for two players on one device.
3. Tap/click an empty cell to place your mark.
4. Win, lose, or draw — then play again or return to the menu. Scores persist until you hit Reset.

## 🛠 Tech stack

- Vanilla HTML/CSS/JS — single file, no frameworks, no build tools
- Google Fonts: [Cinzel](https://fonts.google.com/specimen/Cinzel) and [IM Fell English](https://fonts.google.com/specimen/IM+Fell+English) (loaded via CDN, so an internet connection is needed for the fonts to render as intended — the game still works offline with fallback serif fonts)
- All game logic — board state, the vanish mechanic, minimax AI, win detection, and animations — runs client-side with no external services

## 🚀 Running it

No setup required:

- **Locally**: just open `index.html` in any modern browser.
- **Hosted**: drop it on GitHub Pages, Netlify, Vercel, or any static host — it's a single file with no server-side dependencies.

## ⚙️ Customization ideas

- Change `MAX_MARKS` in the script to make the board more or less forgiving (e.g. `4` for a slower-paced game, `2` for a faster, more chaotic one).
- Adjust the minimax `depth` cutoff (currently capped at 7) to tune how far ahead the Oracle plans — higher is stronger but slower.
- Swap the `--gold` / `--p1` / `--p2` CSS variables to retheme the color palette away from the gothic look.

