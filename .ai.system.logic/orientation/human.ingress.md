# Ingress

Establish the request ID, operation, and applicable context before dependent work. Ask for missing facts. Invalid input or denied access stops the dependent operation.

The local exchange currently supports read-only lookup of this interface's documentation.

[Source JSON](../../ai.ingress.json)

Record identity · kind `ingress_contract` · version `1.0` · mode `reference_only`

## How to use this record

Validate the envelope before selecting or reading evidence.

For a documentation lookup, establish the request ID, operation, and query. An ambiguous repository is missing context when the envelope is otherwise valid. A malformed required field belongs to invalid input. If required access or authority is denied, stop the dependent operation. Accepted requests can reach launch. Unresolved or refused requests can return through egress.

The supported operation is locate_documentation for this interface. Accepted requests point to launch. Other outcomes point to local egress.

## Field guide

- `repository` — dastardlyrat/this-repository-machine-interface
- `landing_pad` — ai.landing.pad.json
- `landing_germ` — ai.landing.pad.low-mem.json
- `launch_pad` — ai.launch.pad.json
- `egress_contract` — ai.egress.json
- `request_envelope`
  - `required`
    - request_id
    - operation
    - query
  - `fields`
    - `request_id` — A nonempty correlation identifier.
    - `operation` — The requested operation. This interface supports locate_documentation.
    - `query` — The information sought in the interface documentation.
    - `target` — Repository and optional revision. Resolve a unique target from the request or established caller context.
    - `source_references` — Applicable source identities, paths, and revisions.
    - `context_references` — Context required to understand the query.
    - `authority_evidence` — Evidence of authority when required by the applicable access policy.
- `admission`
  - Validate required request fields and the supported operation.
  - Resolve the target and required references. Check authority before the dependent read.
  - If a required reference fails to resolve, stop the dependent step and report the condition.
- `outcomes`
  - `accepted`
    - `condition` — The target, required context, and applicable access are established.
    - `next` — ai.launch.pad.json
  - `missing_context`
    - `condition` — A well-formed request lacks a unique target or required context.
    - `next` — ai.egress.json
  - `invalid_input`
    - `condition` — A required field is malformed or absent, or the operation is unsupported.
    - `next` — ai.egress.json
  - `denied_access`
    - `condition` — Required access or authority is denied.
    - `next` — ai.egress.json

## Direct record references

- [ai.egress.json](../../ai.egress.json) · [Human companion](human.egress.md)
- [ai.landing.pad.json](../../ai.landing.pad.json) · [Human companion](human.landing.pad.md)
- [ai.landing.pad.low-mem.json](../../ai.landing.pad.low-mem.json) · [Human companion](human.landing.pad.low-mem.md)
- [ai.launch.pad.json](../../ai.launch.pad.json) · [Human companion](human.launch.pad.md)
