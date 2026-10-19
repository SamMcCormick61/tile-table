# Tile Table

A crossword tile game for 2 to 4 players, each on their own device. Standard 15×15 board, 100 tiles, official scoring, and the TWL06 tournament word list.

**Play:** https://sammccormick61.github.io/tile-table/

## How it works

- The host taps **Start a new table** and shares the four-letter code (or the invite link).
- Friends open the page, type their name and the code, and join. No accounts needed.
- The host's browser runs the game and the players connect to it directly (WebRTC via [PeerJS](https://peerjs.com)), so the host keeps the page open until the game ends. If anyone reloads, they rejoin where they left off.

## Files

- `index.html` - the whole game (rules, scoring, board, networking)
- `words.txt` - word list (TWL06 plus QI, ZA, OK, EW, ZEN)
- `peerjs.min.js` - PeerJS 1.5.4 (MIT license), bundled so the page has no build step
