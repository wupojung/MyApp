# Decision Log

Use this file to preserve important product, architecture, workflow, and scope decisions so that future contributors and AI agents can recover project context without relying on chat history.

## Decision template

### DEC-XXX — Title

- Date: YYYY-MM-DD
- Status: Proposed / Accepted / Superseded
- Context:
- Decision:
- Rationale:
- Consequences:
- Related requirements:

---

## Decisions

### DEC-001 — Requirements before implementation

- Date: 2026-09-29
- Status: Accepted
- Context: The project is being initialized before the app requirements are fully defined.
- Decision: Do not begin application implementation yet. First discuss and document the requirements, MVP scope, and major product decisions.
- Rationale: This reduces premature implementation and gives later AI-assisted coding a stable specification.
- Consequences: The repository begins with planning documentation only.

### DEC-002 — Unity as final implementation platform

- Date: 2026-09-29
- Status: Accepted
- Context: The intended final application will be implemented with Unity.
- Decision: Product and technical planning should remain compatible with a later Unity implementation.
- Rationale: Unity is the selected application platform.
- Consequences: Implementation-specific decisions will be deferred until requirements are clearer.

### DEC-003 — Design documents live under doc/

- Date: 2026-09-29
- Status: Accepted
- Context: The repository will store both project discussions/results and later source code.
- Decision: Store product and design documentation under `doc/`.
- Rationale: Keeps design context version-controlled and separated from later application source code.
- Consequences: Future requirement and architecture documents should be added under `doc/` unless there is a strong reason otherwise.
