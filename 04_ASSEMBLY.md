# ASSEMBLY

This file is the canonical home for operative assembly. It records how an Operative is composed from the kernel and selected upstream sources and how that composition is projected into runtime-facing artifacts.

## Assembly Scope

- Included sources and their roles
- Pinned source states
- Precedence and routing rules
- Edit enablement for included repos
- Generated outputs and their destinations

## Required Assembly Record

Each included source should be recorded with enough information to assemble and maintain the Operative coherently.

- Source name and type
- Source path or mounted location
- Pinned revision or version reference
- Assembly role such as baseline identity, blended identity, persona-only input, operations layer, or environment layer
- Edit enablement for that source

## Assembly Defaults

- The kernel is required.
- Included source-bearing repos remain preserved as source-bearing repos rather than flattened into anonymous canon.
- Runtime-facing artifacts are generated from kernel and selected layer surfaces while preserving source provenance.
- Detailed assembly procedures belong in `02_TASKS.md`.

## Precedence Baseline

- `00_PROTOCOL.md` defines non-overrideable operative invariants.
- Operative files surfaced through the operative-level index define the active operative surface.
- Target-local edit governance applies per editable repo.
- Included source repos remain the canonical authoring surfaces for their own content.