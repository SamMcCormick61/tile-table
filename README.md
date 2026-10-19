# Tile Table

A crossword tile game for 2 to 4 players, each on their own device. Standard 15×15 board, 100 tiles, official scoring, and the TWL06 tournament word list.

**Play:** https://sammccormick61.github.io/tile-table/

## How it works

- The host taps **Start a new table** and shares the four-letter code (or the invite link).
- Friends open the page, type their name and the code, and join. No accounts needed.
- The host's browser runs the game. Every player connects out to a public relay ([HiveMQ's public MQTT broker](https://www.hivemq.com/mqtt/public-mqtt-broker/)) over a secure WebSocket, which works on mobile data and strict Wi-Fi. The host keeps the page open until the game ends; if anyone reloads, they rejoin where they left off.

## Files

- `index.html` - the whole game (rules, scoring, board, networking)
- `words.txt` - word list (TWL06 plus QI, ZA, OK, EW, ZEN)
- `mqtt.min.js` - MQTT.js 5.10.1 (MIT license), bundled so the page has no build step
