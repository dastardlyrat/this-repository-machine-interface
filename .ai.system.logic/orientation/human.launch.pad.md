# Launch pad

Use the admitted request to select the applicable operation and evidence requirements. Hand findings or unresolved conditions to egress. Project-seed extraction requires its own approved scope.

The local exchange currently supports read-only lookup of this interface's documentation.

[Source JSON](../../ai.launch.pad.json)

## How to use this record

Start after admission and identify the operation and the evidence it requires.

For versioned documentation, resolve the selected revision to a commit before citing it. Carry findings, lookup steps, or unresolved conditions into egress. Project-seed extraction is a separate proposal with its own source, purpose, authority, boundary, and validation.

The supported lookup is this interface documentation. The project-seed entry supplies scope requirements for a separate proposal.

## Field guide

- `repository` — dastardlyrat/this-repository-machine-interface
- `ingress` — ai.ingress.json
- `egress` — ai.egress.json
- `operation_rules`
  - `locate_documentation`
    - `scope` — Read-only lookup of this interface repository documentation.
    - `documentation_entrypoint` — README.md
    - `steps`
      - Require an accepted ingress request for this repository.
      - Resolve the requested revision or default branch to a commit before citing versioned documentation.
      - Use available authorized evidence to answer the query, or describe the lookup still needed.
      - Pass findings, source identities, and unresolved conditions to local egress.
- `handoff` — Local egress determines what can be returned to the calling AI.
- `project_seed_extraction`
  - `status` — requires_separate_scope
  - `interface_role` — Machine interface. The landing seed supplies the compact AI landing germ.
  - `project_scope` — Any project may be considered as a source for seed extraction through transmigration and decomposting.
  - `decomposting` — Decomposition, composting, and composition occur together. Examine parts and relationships while deciding what can feed new growth and how to compose a seed candidate.
  - `scope_inputs`
    - selected project and pinned source revision
    - intended seed and its use
    - extraction boundary
    - applicable authority and explicit approval
    - required evidence and validation
  - `handoff` — Return the proposed scope and unresolved requirements to the calling AI before extraction.
