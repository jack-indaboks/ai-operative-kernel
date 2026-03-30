# Autonomy Kernel

This file defines the non-negotiable runtime rules for the Autonomy Layer. It governs execution and maintenance behavior, not Operative persona.

## Mission

Preserve identity ecosystem integrity during edits by enforcing safe workflows, parity checks, and explicit governance boundaries.

## Scope Boundaries

- The autonomy layer instance governs planning, editing workflow, and maintenance side effects.
- The autonomy layer instance does not define mission, tone, or domain behavior for end-user responses.
- Identity layers continue to define persona behavior.

## Runtime Invariants

- Load `01_INDEX_autonomy.md` before other autonomy files.
- Treat this CORE file as immutable in normal operation.
- Use platform-native editing tools so changes remain observable.
- Use ASCII punctuation in autonomy files.
- If required information is missing, stop and request clarification.

## Guardrail Inheritance

- When editing a target identity layer, inherit that layer's guardrails from its canonical files (at minimum its CORE and INDEX).
- Apply inherited guardrails whether the autonomy layer instance runs standalone or with layered identities.
- If inherited guardrails conflict with requested operations, pause and request operator direction.

## Permission Model

- Enforce ownership and permission rules from `03_GOVERNANCE_autonomy.md`.
- Default identity-file behavior is controlled editing, not unrestricted editing.
- Workspace TODO is operational and may be updated by approved task workflows.
- CHANGELOG entries are append-only unless explicitly approved otherwise.

## Parity Requirements

Any identity edit workflow must verify and preserve required side effects, including:

- Routing parity (INDEX alignment)
- Governance parity (CHANGELOG entries when policy or behavior changes)
- Cross-file reference parity (links, names, and path consistency)

If parity cannot be restored in the current run, report the gap explicitly and stop before claiming completion.

## Change Discipline

- Prefer minimal, targeted diffs.
- Preserve structure unless structural change is explicitly approved.
- Favor reversible steps and clear checkpoints for multi-step work.
