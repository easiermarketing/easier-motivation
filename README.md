# easier motivation

A single page for the moment you're not doing the thing you meant to do.

It doesn't need to know what the task is. It asks why you're stuck, which has six answers, and hands you a strategy that fits that answer and fits you.

## How it works

**Six causes.** Four from temporal motivation theory (Steel and König, 2006): the task is unclear, the task is boring, there's no near deadline, something else is pulling harder. Two emotional blockers that need different handling: dread before the event, and shame after being late.

**Tagged strategies.** Every card fixes one cause and pulls one of six levers: another person, task structure, place, reward, thinking, body.

**A profile.** Six weights, one per lever. The deck draws strategies weighted by how well each lever works for this person. Rating a card "worked" or "didn't help" adjusts its weight.

The profile is currently seeded for one person from a long conversation. A setup flow that builds it for a new user is the next step, not this version.

## Editing

Everything is in `index.html`.

- **Add a strategy:** add a line to the `STRATEGIES` array. Needs `id`, `cause`, `lever`, `title`, and optional `detail`.
- **Change a cause's explanation:** edit its `lede` in `CAUSES`.
- **Change default weights:** edit `DEFAULT_PROFILE`.

Every sentence should make sense to a stranger with no context. If it needs decoding, rewrite it.

## Storage

`localStorage`, per device. The `store` object at the top of the script is the only thing that touches it. To move to Cloudflare D1, replace `store.get` and `store.set` with calls to a Pages Function and keep the same shape.

## Deep links

`#start` `#boring` `#nodeadline` `#pulled` `#dread` `#late` `#tune`

## Deploy

Cloudflare Pages, connected to this repo. Push to `main` and it's live in about a minute. No build step.
