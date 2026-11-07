```text
IF reader = heuristic engine THEN read ai.landing.pad.json.
ELSE IF reader = AI THEN read ai.landing.pad.low-mem.json.
ELSE continue with the human README.
IF a required reference fails to resolve THEN stop the dependent step AND report the unresolved reference.
```

[Heuristic engine landing pad](ai.landing.pad.json) · [AI landing germ](ai.landing.pad.low-mem.json)

# This Repository Machine Interface

This standalone interface uses a full Lattice seed for heuristic engines and a compact germ for AIs. Both lead to [local ingress](ai.ingress.json), which describes the request context a caller needs to supply. The records provide orientation and request-admission rules for a receiving system.
