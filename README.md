# איקס עיגול · זירת הקרח

A browser Tic-Tac-Toe game with an ice-arena look. Play against the computer or another person on the same device.

## How to play

Open `index.html` in a browser. No build step or server is required.

- **נגד מחשב** — you play as ○; the computer plays as ✕ using minimax.
- **שני שחקנים** — take turns as ○ and ✕ on the same board.
- **מהלך אחורה** — undo the last move (in AI mode this also undoes the computer reply).
- **סיבוב חדש** — clear the board and keep the score. Changing mode resets the score.

Wins, losses, and draws are tracked on the scoreboard.

## Files

| File | Role |
| --- | --- |
| `index.html` | Page structure (Hebrew, RTL) |
| `styles.css` | Ice-arena layout and visuals |
| `game.js` | Turns, scoring, undo, and AI |
