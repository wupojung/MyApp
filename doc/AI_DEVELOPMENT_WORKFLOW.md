# AI-Assisted Development Workflow

> Status: Draft

This project may use ChatGPT, Gemini, Codex, Antigravity, or other AI tools. The repository documentation is the persistent source of truth; chat history alone is not.

## 1. Roles

### Product / design discussion

AI may help:

- clarify requirements
- compare product options
- identify risks and missing cases
- draft user flows and acceptance criteria
- review consistency across documents

### Implementation

Implementation starts only after explicit approval of the relevant requirements.

AI may later help:

- create implementation plans
- write Unity/C# code
- create tests
- review pull requests
- diagnose CI/build failures

## 2. Required context for AI agents

Before implementing a task, an AI agent should read at minimum:

1. `README.md`
2. `doc/README.md`
3. `doc/PROJECT_BRIEF.md`
4. `doc/REQUIREMENTS.md`
5. `doc/DECISIONS.md`
6. Any task-specific design document

## 3. Working principle

```text
DISCUSS
→ DOCUMENT
→ REVIEW
→ FREEZE TASK SCOPE
→ IMPLEMENT
→ TEST
→ REVIEW
→ MERGE
```

Do not allow implementation to silently redefine requirements. If implementation reveals a product decision, update the relevant document and decision log.

## 4. Git workflow

Recommended later workflow:

- `main` remains the stable project baseline.
- Each meaningful change uses a dedicated branch.
- Changes are proposed through a pull request.
- PR descriptions should state the requirement/design documents they implement.
- AI-generated changes must be reviewable and testable like human-generated changes.

## 5. Current restriction

The project is currently in **Phase 0 — Requirements Discovery**.

Until that phase is explicitly closed:

- Do not create Unity application code.
- Do not choose architecture prematurely.
- Do not add dependencies merely because an AI agent prefers them.
- Focus on product goals, user scenarios, scope, constraints, and acceptance criteria.

## 6. Context handoff

At the end of a meaningful discussion round:

- update the relevant document under `doc/`
- record major decisions in `doc/DECISIONS.md`
- keep unresolved questions explicit

This makes it possible for a different AI model or future conversation to continue from the repository rather than reconstructing decisions from memory.
