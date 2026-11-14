# Poo Party

A silly collect-the-poos game for Farah, Mia and Gemma. Each poo has its own mini-game; playing earns party points that hatch new poos.

- `index.html` is the whole game (no build step). Open it in a browser or host it on Netlify / GitHub Pages.
- Progress is saved per player in the browser's localStorage, so it stays on the device it was played on.

## Poos so far

| Poo | Game | Party points to hatch |
| --- | --- | --- |
| Sir Plops-a-Lot | Poo Catcher | start |
| Flappy McPlop | Flappy Poo | 30 |
| Peeky Poo | Whack-a-Poo | 50 |
| Skater Poo | Poo Runner | 70 |
| Fancy Poo | Match the Poo (plus Free Dress-Up) | 90 |
| Sporty Poo | Poo Hop | 110 |

Poos hatch in order, and one game can hatch at most one poo (the hatch meter resets each time). Once all six are hatched, the Poo Disco opens.

Each scored game has three titles (Little Stinker, Super Pooper, Poo Master); the score levels are in `TITLES`.

To add a poo: add an entry to `POOS`, write a game object with `tap`, `pointer`, `update(dt)` and `draw(ctx)`, and add it to `GAMES`.
