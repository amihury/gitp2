# איקס עיגול · זירת הקרח

A Hebrew, RTL tic-tac-toe game with an icy arena theme. Open it in any modern browser — no install or build step.

Play against an unbeatable computer (minimax), or pass the device for two players. Scores, undo, and a win-line animation are built in.

## Features

- **נגד מחשב** — AI replies with minimax and never loses (best play leads to a draw)
- **שני שחקנים** — local pass-and-play on one board
- **Scoreboard** — tracks wins for ○ / ✕ and draws across rounds
- **מהלך אחורה** — undoes the last move (and the computer’s reply in AI mode)
- **סיבוב חדש** — clears the board and keeps the score
- **Win line** — SVG stroke drawn through three in a row
- **Hebrew UI** — full RTL layout (`lang="he"`, `dir="rtl"`)

## Run

Open `index.html` in a browser. That is all.

Optional: serve the folder with any static server if you prefer (`npx serve`, Live Server, etc.).

## Play

| Rule | Detail |
|------|--------|
| You | **עיגול** (○) |
| Opponent | **איקס** (✕) — computer or second player |
| First move | Circles always start |
| Mode switch | Resets the board **and** the score |
| New round | Clears the board; score stays |

Status text above the board shows whose turn it is, wins, or a draw (“תיקו על הקרח”).

## Project structure

```
gitp2/
├── index.html   # Page shell, board grid, controls
├── styles.css   # Ice theme, layout, animations
├── game.js      # Rules, AI (minimax), undo, scores
└── README.md
```

## Tech notes

- Plain HTML, CSS, and vanilla JavaScript — no framework or bundler
- Fonts: [Assistant](https://fonts.google.com/specimen/Assistant) + [Secular One](https://fonts.google.com/specimen/Secular+One) via Google Fonts
- Board state is a 9-cell array; win checks use the eight classic lines
- AI uses recursive minimax over empty cells (`x` maximizes, `o` minimizes)
- Undo pops from a move history; in AI mode it removes both the AI move and your previous move
- Responsive: board fits `min(520px, 100vw − 32px)`; works on phone and desktop

## Controls

| Control | Action |
|---------|--------|
| Board cell | Place ○ or ✕ on an empty square |
| נגד מחשב / שני שחקנים | Switch mode (resets score) |
| מהלך אחורה | Undo last move(s) |
| סיבוב חדש | New round, keep score |
