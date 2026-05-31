# jdclemons.dev

Static portfolio site for Josh Clemons. Exists primarily so subdomains (`*.jdclemons.dev`) have a registered domain to hang off of. The site itself is intentionally simple.

## Design rationale

The previous portfolio (see `~/Projects/old-portfolio`) was a Three.js scene with spinning photo-cubes and video-textured project meshes. Ambitious, fragile, and clearly a learning exercise. This is the corrective overcorrection.

Format is a software changelog. The choice is deliberate: it communicates background in a format a developer would actually read, the humor emerges from the structure rather than being bolted on, and it ages gracefully as entries are added.

Tone guide: terse SWE with dry self-deprecation. Think [grugbrain.dev](https://grugbrain.dev/) — complexity bad, ship thing, still learning somehow. No mission statements, no buzzwords, no "passionate about solving problems."

## Stack

None. Pure HTML and CSS. No framework, no build step, no node_modules. Drop `index.html` and `style.css` on any static host and it works. This is a feature, not an oversight.

## Changelog format

Each `.entry` block maps to a life stage. Version numbers approximate age. Changelog markers follow convention:

- `+` added — new capability, role, or identity acquired
- `-` removed — something deprecated or lost
- `~` changed — ongoing state or acknowledged reality

Keep entries short. One line each. The format enforces brevity.

## Adding projects

Projects live in `.projects ul` in `index.html`. Each entry should link to a subdomain:

```html
<li><a href="https://[name].jdclemons.dev">[name]</a> — one line description</li>
```

One line. No screenshots, no tech stack bullet points. If it needs more explanation than a line, it can explain itself on its own subdomain.

## What not to do

- No JavaScript unless something is genuinely impossible without it
- No animations, transitions, parallax, or anything that moves
- No frameworks (React, Vue, Svelte — none of it)
- No dark/light mode toggle (dark is fine, pick one)
- No cookie banners, analytics embeds, or tracking pixels
- Do not increase complexity to demonstrate skill — the skill is restraint

## Personal context

- Background: USMC (MOS 5711, nuclear, biological, chemical) → VetTec bootcamp → software engineer
- Has a kid; that's the "dad" entry
- GitHub/LinkedIn handles in `index.html` footer — verify before deploying

## Deployment

Static files. Serve from wherever. No CI pipeline required unless you want one.
