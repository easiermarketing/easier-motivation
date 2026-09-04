# easier motivation

A single-page tool for the gap between knowing what to do and starting it.

Static. One file. No build step, no dependencies, no data collection.

## Editing

Everything lives in `index.html`.

- **Deck cards** — the `cards` array near the bottom of the script. Add lines, remove lines. More cards is the fix when it goes stale, not a new tool.
- **Pages** — each panel section. Add one by copying a section, giving it a new id, and adding its title to the `titles` object in the script.
- **Colours and type** — the `:root` block. Tokens follow the easier design system.

## Deep links

Append the hash to link straight to a page from a task card:

#boring #exposing #missed #call #late #good #deck #fuel #corrections #evidence #conditions

## Deploying

Connected to Cloudflare Pages. Pushing to main deploys automatically.

Build settings: no framework, no build command, output directory /.
