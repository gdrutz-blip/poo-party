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
| DJ Poo | Poo Says (memory tunes) | 130 |
| Builder Poo | Poo Tower (stacking) | 150 |
| Astro Poo | Poo Bounce (jumper) | 170 |

Party points fill an egg. When it is full she taps it to hatch (7 taps) and the meter resets, so only one poo hatches at a time. Hatched poos sometimes ask for a wipe, a snack or a nap; ignoring them has no penalty and helping earns 4 party points. Once all nine are hatched, the Poo Disco opens.

Each scored game has three titles (Little Stinker, Super Pooper, Poo Master); the score levels are in `TITLES`.

To add a poo: add an entry to `POOS`, write a game object with `tap`, `pointer`, `update(dt)` and `draw(ctx)`, and add it to `GAMES`.
