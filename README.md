# Poo Party

A silly collect-the-poos game for Farah, Mia and Gemma. Each poo has its own mini-game; playing earns party points that hatch new poos.

- `index.html` is the whole game (no build step). Open it in a browser or host it on Netlify / GitHub Pages.
- Progress is saved per player in the browser's localStorage, so it stays on the device it was played on.

## Poos so far

| Poo | Game | Hatches at |
| --- | --- | --- |
| Sir Plops-a-Lot | Poo Catcher | start |
| Flappy McPlop | Flappy Poo | 25 party points |
| Peeky Poo | Whack-a-Poo | 60 party points |
| Skater Poo | Poo Runner | 110 party points |

To add a poo: add an entry to `POOS`, write a game object with `tap`, `pointer`, `update(dt)` and `draw(ctx)`, and add it to `GAMES`.
