# Overhouse

A cellular-automaton toy in the spirit of Conway's Game of Life, but with houses.

## State

Prototype in the browser, client only. Merges to `main` are deployed to
https://overhouse.tobias.world.

## How it works

- A house is a pentagon: an **underside**, two **walls** and two **roof** sides. Houses
  connect edge to edge, and only matching sides connect (underside to underside, wall to
  wall, roof to roof). The shape is adjustable, which changes which tilings are possible.
- Each tick, every house counts its connected sides (0–5) and looks up in a rule table
  whether to **die**, **stay** or **grow** a new house on a random free side. New houses
  may not overlap existing ones unless overlap is allowed.
- Presets (Slow bloom, Crystal, Lace, Coral, Wildfire) show what the default shape can
  do; Random rolls a new rule table, and every rule can be changed while it runs.
- Clicking a house sends a ripple or echo through the connections, shows its lineage,
  or seeds, removes or freezes it.
- Houses are colored by connected sides. The link holds the rules, shape and random
  seed, so it reproduces a world.

## Development

Commands, project structure and conventions are in [`AGENTS.md`](AGENTS.md).
