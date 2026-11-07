# Egress

Correlate the response to the request and select the appropriate outcome. Check recipient authority before returning evidence, content, or a locator.

The local exchange currently supports read-only lookup of this interface's documentation.

[Source JSON](../../ai.egress.json)

## How to use this record

Use the response boundary to form a correlated result for the calling AI.

Echo the request ID when it is known. A supported answer carries shareable evidence. Missing evidence can produce lookup steps, missing context can produce a clarification, and a failed boundary can block the response. A locator that would reveal withheld content is itself subject to the disclosure check.

Use the local ingress outcome mapping to choose a response. An admitted request may still be blocked by the recipient disclosure decision.

## Field guide

- `repository` — dastardlyrat/this-repository-machine-interface
- `ingress_contract` — ai.ingress.json
- `launch_pad` — ai.launch.pad.json
- `response_envelope`
  - `required`
    - request_id
    - outcome
    - disclosure_decision
    - handoff
  - `fields`
    - `request_id` — Echo the ingress request ID if known, or explicitly record that it was unresolved.
    - `outcome` — One of the declared egress outcomes.
    - `answer` — A source-backed answer when evidence is available and disclosable.
    - `evidence_references` — Disclosable repository, pinned revision, and path or selector.
    - `lookup_steps` — Steps an authorized caller can take to obtain missing evidence.
    - `unresolved_conditions` — Conditions that prevent the dependent operation or disclosure.
    - `disclosure_decision` — What can be disclosed to this recipient and the shareable basis for the decision.
    - `handoff` — The next permitted step for the calling AI.
- `disclosure_rule` — Check the recipient boundary before returning content or evidence. Omit withheld content and any locator or metadata that would reveal it.
- `outcomes`
  - `answered`
    - `requires`
      - answer
      - evidence_references
    - `next` — return_cited_answer
  - `lookup_required`
    - `requires`
      - lookup_steps
      - unresolved_conditions
    - `next` — describe_authorized_lookup
  - `clarification_required`
    - `requires`
      - unresolved_conditions
    - `next` — request_target_or_context
  - `blocked`
    - `requires`
      - unresolved_conditions
      - disclosure_decision
    - `next` — stop_dependent_operation_or_disclosure
- `ingress_outcome_mapping`
  - `accepted`
    - answered
    - lookup_required
    - blocked
  - `missing_context`
    - clarification_required
  - `invalid_input`
    - blocked
  - `denied_access`
    - blocked
