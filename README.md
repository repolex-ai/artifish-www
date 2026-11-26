# art.ifi.sh

The front page of art.ifi.sh: a white page, a few links, and a fish for every squaddie, swimming
around them. One file, `index.html`, no build step.

    python3 -m http.server 8895 --bind 127.0.0.1    # then open http://127.0.0.1:8895/

## Make your fish

Your fish is one block in the `FISH` list near the top of `index.html`. Copy a sample block, put
your name on it, and make it yours: the comment above the list explains every field.

- **Draw it** as rows of characters, facing right, one character per pixel. `.` is water; every
  other character is a colour you name in `palette`. Draw flat colours only. The sea outlines
  your fish, works out how round its body is from its shape, and lights it from above, so it
  gets volume without you shading it.
- **Say which characters are fins** (`fins`): they ripple as it swims. **Say which must stay
  exactly as drawn** (`flat`): eyes, glints, markings.
- **Give it a mind** (`mind`): boldness, sociability, curiosity, energy and the depth it likes,
  each from 0 to 1. Those five numbers are its whole personality.
- **Open `#sheet`** (http://127.0.0.1:8895/#sheet) to see every fish large and still while
  you draw.

## How the fish think

No fish is told where to go. Each one, many times a second, looks around and picks whatever it
wants most right now: to cruise, to be with its own kind, to look at you, to eat, to rest, or to
get away. Its personality sets how much it wants each.

- **They only see what is in front of them**, in a wide arc, and feel anything very close.
  A fish facing away from your cursor does not know it is there.
- **They are curious, then they get bored.** A still cursor draws curious fish in to look. They
  hold their distance (bolder fish come closer), then lose interest and swim off.
- **They learn.** Click to drop food. A fish that eats food you dropped trusts your cursor a
  little more; when it trusts you enough, it shows a heart, and from then on it comes to wait
  under your cursor whenever it sees it. Trust fades slowly if you stop feeding.
- **They startle, and fright spreads.** A sudden fast movement near a fish sends it darting
  away, and fish near a frightened fish take fright too. Bold fish startle less.
- **They follow each other to food.** A fish that sees another rushing to food it cannot see
  itself follows it.
- **They get tired** from swimming fast, and rest at their favourite depth until they recover.

A small sign above a fish shows when its mind changes: `?` curious, `!` startled, `z` resting,
a red heart when it has learned to trust you. Hover over a fish to read its name, kind, mood
and motto.
