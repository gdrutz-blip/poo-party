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
| Pirate Poo | Poo Pairs (memory cards) | 190 |
| Ninja Poo | Poo Slice (swipe) | 210 |
| Racer Poo | Poo Race (lane dodging) | 230 |
| Justin Poober | Poo Beat (rhythm) | 250 |
| Michael Jacksonpoo | Poo Spotlight (keep the poo in the light) | 270 |
| Poozer | Poo Bricks (breakout) | 290 |
| Plumber Poo | Poo Pipes (rotate-the-pipes puzzle) | 310 |
| Musketeer Poo | Poo Duel (sword timing) | 330 |
| Fairy Poo | Poo Path (steer down a winding path) | 350 |
| Clown Poo | Poo Juggle (keep balls in the air) | 370 |
| Unicorn Poo | Rainbow Blast (shoot the grumpy clouds) | 390 |
| Chef Poo-la-la | Poo Kitchen (tap ingredients in ticket order) | 410 |
| Poo-peroni | Pizza Spin (throw pepperoni at a spinning pizza) | 430 |

Party points fill an egg. When it is full she taps it to hatch (7 taps) and the meter resets, so only one poo hatches at a time. Hatched poos sometimes ask for a wipe, a snack or a nap; ignoring them has no penalty and helping earns 4 party points. Once all twenty-two are hatched, the Poo Disco opens.

Each scored game has three titles (Little Stinker, Super Pooper, Poo Master); the score levels are in `TITLES`.

To add a poo: add an entry to `POOS`, write a game object with `tap`, `pointer`, `update(dt)` and `draw(ctx)`, and add it to `GAMES`.

## Extras

- **Hat shop:** spend party points on hats for any hatched poo. Rare hats (Golden Crown, Rainbow Afro, Angel Halo, Flame Hair) only come from golden eggs.
- **Golden eggs:** earned the first time a game reaches its top title (Poo Master). Tap to hatch (9 taps) for a rare hat, or 25 bonus stars once all four are owned.
- **Sticker book:** every poo hatched, every title, and 10 special stickers.
- **Rename:** each player can give any hatched poo their own name (14 letters max).
- **Play vs. a friend:** two players take turns on the same game; the winner gets 5 bonus stars.

- **Mystery eggs:** every player hatches the poos in their own random order (the first is always Sir Plops-a-Lot). Costs go up by hatch number, and unhatched poos are hidden.
- **Egg price cap:** eggs get a bit pricier for the first few poos, then stay at 150 party points each so the collection never turns into a grind.
