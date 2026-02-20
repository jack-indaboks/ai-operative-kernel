# Autonomy Layer Template (ALT)

Use this repository as the starter Autonomy Layer. The Autonomy Layer is not an identity layer. It supplies governance for self-editing and long-running execution, and it is only included in a workspace when an agent is intended to modify identity files.

Identity layers assume their own files are immutable unless an Autonomy Layer is present in the workspace.

## Purpose

- Maintain ecosystem parity when identity files change.
- Define governed edit workflows (planning, edits, decision logging, and parity checks).
- Provide guardrails for TODO logging, decision capture, and workflow automation.
- Stay separate from identity layers so stable personas remain stable by default.

## Core Role

ALT is an integrity layer, not a lock.

- It does not attempt to prevent all out-of-band edits by humans or other tools.
- It defines the authorized maintenance workflow that keeps identity artifacts in sync.
- It ensures identity updates include required side effects (for example INDEX updates, CHANGELOG entries, and related cross-file alignment).

## What This Layer Is Not

- Not a replacement for PILT or TILT.
- Not a knowledge base for project content.
- Not a default dependency for identity layers.
- Not a personality or tone layer.

## Structure

| File | Role | Maintainer Notes |
|------|------|------------------|
| `00_CORE_autonomy.md` | Non-negotiable autonomy runtime kernel. | Template-maintained; avoid direct edits unless intentionally evolving ALT itself. |
| `01_INDEX_autonomy.md` | Agent routing map for autonomy files. | Keep in sync when file inventory changes. |
| `02_TASKS_autonomy.md` | Executable autonomy workflows. | Primary extension point for new automation workflows. |
| `03_GOVERNANCE_autonomy.md` | Ownership and permission model. | Maintainer-editable policy surface. |
| `04_STYLE_autonomy.md` | Style conventions for identity maintenance edits. | Maintainer-editable consistency surface. |
| `09_CHANGELOG_autonomy.md` | Append-only autonomy policy CHANGELOG. | Add new entries; avoid destructive edits. |

TODO tracking stays workspace-level (for example `TODO.md`) rather than in ALT.

## How It Fits Into Prompt Layering

- The prompt-layering TASK merges Autonomy CORE with one or more identity CORE files when self-editing is intended.
- If the Autonomy Layer is absent, identity files are generally treated as immutable.
- ALT can be used standalone or layered; governance behavior is the same in both cases.

## Guardrail Inheritance Rule

- In ALT workflows, identity edits inherit the target layer's guardrails from that layer's own files (at minimum CORE and INDEX).
- This inheritance model applies whether ALT runs standalone or blended with another identity layer.
- When target-layer guardrails and autonomy workflow steps conflict, operator direction is required before continuing.

## Out-of-Band Edit Policy

- Out-of-band edits are possible, but they are considered ad hoc.
- Ad hoc identity edits are expected to be reconciled through ALT workflows so parity is restored.
- Reconciliation captures missing side effects (for example CHANGELOG and INDEX alignment).

## Getting Started

1. Click **Use this template** on GitHub to create a new Autonomy Layer repository (for example `ALT_Nova`).
2. Define the autonomy CORE and INDEX files based on your environment and governance needs.
3. Include this repo alongside identity layers only when you want self-editing behavior.

## For Operators

- When you want a static assistant, exclude this repo from the workspace.
- When you want a self-editing assistant, include this repo and run the prompt-layering TASK.
- If edits occur outside ALT workflows, reconciliation restores the layer to a clean, parity-aligned state.
