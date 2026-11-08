```text
IF reader = heuristic engine THEN read ai.landing.pad.json.
ELSE IF reader = AI THEN read ai.landing.pad.low-mem.json.
ELSE continue with the human README.
IF a required reference fails to resolve THEN stop the dependent step AND report the unresolved reference.
```

[Heuristic engine landing pad](ai.landing.pad.json) · [AI landing germ](ai.landing.pad.low-mem.json)

# This Repository Machine Interface

This standalone interface uses a full Lattice seed for heuristic engines and a compact germ for AIs. Both lead to [local ingress](ai.ingress.json), which describes the request context a caller needs to supply. The records provide orientation and request-admission rules for a receiving system.

A request enters through [ingress](ai.ingress.json), proceeds to the [launch pad](ai.launch.pad.json) when admitted, and returns through [egress](ai.egress.json). The first supported operation is a read-only lookup of this interface documentation.

## Project seed extraction

This repository is a machine interface. Its landing seed supplies the compact AI landing germ. Any project may be considered as the source of a separate project seed through **transmigration and decomposting**.

**Decomposting** is decomposition, composting, and composition happening together. Examine the project's parts and relationships while deciding what can feed new growth and how to compose that material into a seed. The emerging candidate can change which boundaries and relationships need further examination.

Before extraction, identify the selected project and pinned revision, the intended seed, the extraction boundary, and the authority and evidence required. The [launch pad](ai.launch.pad.json) records those requirements for a separately approved scope.

See [Decomposting Theory](.ai.system.logic/human.DECOMPOSTING_THEORY.md) for recovery and recomposition, recursive transmigration, and the quadrangle of proper construction.

Our developing technology is documented in [xOSG Prototype](https://github.com/alia-june/xOSG-prototype).

## Human-readable JSON records

Use the [project JSON map](.ai.system.logic/human.PROJECT_JSON_MAP.md) to follow the records by function, find their companions, and locate direct dependencies.

- [Egress](.ai.system.logic/orientation/human.egress.md)
- [Ingress](.ai.system.logic/orientation/human.ingress.md)
- [Heuristic landing pad](.ai.system.logic/orientation/human.landing.pad.md)
- [AI landing germ](.ai.system.logic/orientation/human.landing.pad.low-mem.md)
- [Launch pad](.ai.system.logic/orientation/human.launch.pad.md)
