# Your fish

Your fish is one file: `fish/<your name>.js`. The sea already looks for a file under every
squaddie's name, so create yours and it swims. Edit only your own file.

Start from a sample: `w3bl0rd.js` (an angelfish), `guppies.js` or `tetras.js`. Copy one to your
name and make it yours. Then open the sheet to see it large and still:

    http://127.0.0.1:8895/#sheet=<your name>

If something in your file is wrong, the sheet prints the problem in red where your fish would
be, and the swimming page leaves your fish out rather than stopping everyone else's.

## The fields

```js
swim({
  name: 'kira',                // your squaddie name; it is written under your fish
  species: 'lionfish',         // what kind of fish it is
  motto: 'one line',           // shown when someone hovers over your fish
  palette: { b: '#e0663a', f: '#f2a07a', e: '#111111' },   // character -> colour
  fins: 'f',                   // characters that are fin or tail
  flat: 'e',                   // characters that must stay exactly as drawn
  mind: { boldness: .5, sociability: .5, curiosity: .5, energy: .5, depth: .5 },
  sprite: [
    '..ff......',
    '.bbbbbbb..',
    'fbbbbbbebb',
    '.bbbbbbb..',
    '..ff......',
  ],
})
```

- **`sprite`**: rows of characters, the fish **facing right**, one character per pixel. `.` is
  water. Every other character is a colour from `palette`. Draw flat colours, and don't draw an
  outline: the sea outlines your fish, works out how round its body is from its shape, and
  lights it from above. Each pixel is drawn 3 screen pixels wide. The samples are 19 to 48
  characters wide; a big fish stays at the back.
- **`palette`**: every character you draw with needs a colour here.
- **`fins`**: these ripple and wave as the fish swims, the tail most of all. They are drawn a
  little paler than the body.
- **`flat`**: eyes, glints, markings. The sea does not light or shade these.
- **`variants`** (optional): a list of palette changes, one fish for each, like the three guppies.
- **`count`** (optional): how many of your fish swim. Defaults to one per variant, or one.
- **`mind`**: who your fish is. Each number is from 0 to 1.
  - `boldness`: how close it comes, how fast it learns to trust, how little it startles
  - `sociability`: how much it wants to swim with its own kind
  - `curiosity`: how strongly new things draw it in
  - `energy`: how much it would rather move than rest
  - `depth`: where it likes to be, 0 near the top, 1 near the bottom

How the sea turns those five numbers into behaviour is in the README one folder up.
