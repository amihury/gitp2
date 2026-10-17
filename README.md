# איקס עיגול · זירת הקרח

A Hebrew tic-tac-toe game in the browser. Play against an unbeatable computer, or pass the device for two players.

No install or build step. Open `index.html` in a browser.

## Features

- **נגד מחשב** — computer replies with minimax and never loses
- **שני שחקנים** — two people share the same board
- Scoreboard for circles, crosses, and draws
- Win line drawn through three in a row
- **מהלך אחורה** undoes the last move (and the computer’s reply in AI mode)
- **סיבוב חדש** clears the board and keeps the score
- Ice-arena theme, RTL Hebrew UI, works on phone and desktop

## Play

- You are **עיגול** (circle). The computer, or the second player, is **איקס** (cross).
- Circles always move first.
- Switching modes resets the score.

Wins, draws, and the current turn are shown above the board.

## Files

| File | Role |
| --- | --- |
| `index.html` | Page layout, board, scoreboard, controls |
| `styles.css` | Ice theme and layout |
| `game.js` | Turns, scores, undo, and minimax AI |

## How the AI works

In computer mode the opponent is **X**. After your move it searches every remaining line of play with minimax and picks a move that never loses: it wins if you slip, otherwise it forces a draw.
