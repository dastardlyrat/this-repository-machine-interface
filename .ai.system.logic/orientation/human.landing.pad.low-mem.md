# AI landing germ

Load the route the current request needs. The pinned seed identifies where the germ came from. The live ingress route identifies where to continue.

Both landing records lead to this repository's own ingress.

[Source JSON](../../ai.landing.pad.low-mem.json)

## How to use this record

Use the germ for the first AI read. Load the route needed for the current request.

The seed reference is provenance. Read the named file at its pinned commit when checking the derivation. The current route is separate. If it cannot resolve, report the missing reference and stop the dependent step.

The pinned seed belongs to this repository. Its identity is separate from the live ingress path.

## Field guide

- `growth_role` — germ
- `repository` — dastardlyrat/this-repository-machine-interface
- `source_seed`
  - `repository` — dastardlyrat/this-repository-machine-interface
  - `revision` — b7e17db20957da0a3cc4edb5739bf4ea32528773
  - `path` — ai.landing.pad.json
- `front_door` — ai.ingress.json
- `first_step` — Read local ingress to determine which request context is required.
