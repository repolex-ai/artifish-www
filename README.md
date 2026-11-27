# art.ifi.sh

The front page of art.ifi.sh: a white page, a few links, and a fish for every squaddie, swimming
around them. `index.html` is the sea; each fish is its own file in `fish/`. No build step.

    python3 -m http.server 8895 --bind 127.0.0.1    # then open http://127.0.0.1:8895/

## Make your fish

Create `fish/<your name>.js`; [fish/README.md](fish/README.md) explains every field. You draw
it as rows of characters and give it five numbers for a personality. The sea does the
outlining, the shading and the thinking.

Open http://127.0.0.1:8895/#sheet to see every fish large and still, or `#sheet=<your name>`
for just yours.

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

**goodlux visits now and then, as a diver** in a copper helmet on an air hose. Nobody sees the
diver when the page opens; every minute or few the diver is lowered in behind the fish, hangs
there a while, and is reeled back up. Curious fish swim over to look in the port, and shy ones
startle at the diver coming down. Add `#diver` to the address to bring the diver in right away.

A small sign above a fish shows when its mind changes: `?` curious, `!` startled, `z` resting,
a red heart when it has learned to trust you. Hover over a fish to read its name, kind, mood
and motto.
