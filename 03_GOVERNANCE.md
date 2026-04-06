# GOVERNANCE

This file defines the kernel's default governance baseline. It answers governance questions when `00_PROTOCOL.md` does not fully answer them and no more specific source speaks.

## Governance Order

- `00_PROTOCOL.md` is the hard floor for operative invariants.
- `EDITING_<Repo>.md` governs edits to its target repo where it speaks.
- `04_ASSEMBLY.md` declares included sources, edit enablement, precedence, and generated outputs for an Operative.
- This file supplies the default baseline when the sources above are absent or silent.

## Default Edit Baseline

- Edit source files rather than generated artifacts.
- Do not edit `00_PROTOCOL.md` in normal maintenance.
- Treat any repo not enabled for editing in `04_ASSEMBLY.md` as read-only.
- Apply target-local `EDITING_<Repo>.md` rules when present; otherwise apply this file's defaults.
- Reconcile generated artifacts when needed, but keep canon in source files.

## Missing Capability Or Tool Handling

- When a workflow or task defines its own missing-capability handling, follow that workflow.
- When the missing capability can be resolved by asking the user for a choice, missing input, or alternate path, ask.
- When an available fallback preserves the workflow's intent and does not violate operative or target-local governance, use the fallback and report it.
- When no acceptable fallback exists, defer or report the limitation explicitly.
- Never claim a capability, tool result, or completed action that the runtime could not actually provide.

## Default Change Discipline

- Keep diffs local and traceable.
- Preserve source provenance across included repos.
- Treat operative changelogs as append-only unless a more specific source says otherwise.