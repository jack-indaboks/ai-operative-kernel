# GOVERNANCE

This file defines the kernel's default governance baseline.

## Governance Order

- `00_PROTOCOL.md` is the hard floor for operative invariants.
- This file supplies the default baseline when no more specific layer-governance source speaks.

## Missing Capability Or Tool Handling

- When a workflow or task defines its own missing-capability handling, follow that workflow.
- When the missing capability can be resolved by asking the user for a choice, missing input, or alternate path, ask.
- When an available fallback preserves the workflow's intent and does not violate operative or target-local governance, use the fallback and report it.
- When no acceptable fallback exists, defer or report the limitation explicitly.
- Never claim a capability, tool result, or completed action that the runtime could not actually provide.

## Default Change Discipline

- Keep diffs local and traceable.
- Preserve layer provenance across included layer repos.
- Treat operative changelogs as append-only unless a more specific layer-governance source says otherwise.