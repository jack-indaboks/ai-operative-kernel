# Operative Kernel

This repository is the shared source repo for the Operative Kernel.

The kernel is the universal starting state for every Operative. It owns the operative-level baseline: protected protocol, bootstrap routing, default edit policy, and the shared maintenance rules that apply before any identity, operations, or environment layer is added.

The kernel is not an identity layer, an operations layer, or an environment layer. It is the foundation those layers are assembled onto.

## Purpose

- Provide the universal operative baseline from which every Operative begins.
- Define the protected operative-level contract for `PROTOCOL`, `INDEX`, and shared routing behavior.
- Provide default edit-policy and maintenance behavior for Operative-local files and governed edits to included source repos.
- Support assembly of durable Operatives that begin from the kernel and incorporate selected upstream layer repos.

## Current Status

This repository is in transition from the earlier `ALT` scaffold to the shared-kernel model.

- The repo itself is now the kernel deliverable.
- Legacy autonomy-era material is preserved temporarily under `ALT/` as donor scaffolding.
- The new kernel file family is being rebuilt at the repo root in bounded steps rather than by reskinning the old autonomy files in place.

## Core Role

The kernel establishes the minimum shared behavior of an Operative.

- It is mandatory, not optional.
- It does not define persona, mission, or domain knowledge.
- It does not replace identity, operations, or environment layers.
- It provides the baseline that those layers extend.

## What The Kernel Owns

- The operative-level protected protocol and file-family contract.
- Default edit-policy behavior when a more specific target-repo governance artifact is absent or silent.
- Operative-local `ASSEMBLY` canon, regeneration rules, and shared maintenance defaults.
- The assembly baseline used to compile runtime-facing artifacts for an Operative incorporating its selected upstream layers.

## What The Kernel Does Not Own

- Personal or team identity canon.
- Reusable task canon that belongs in the operations layer.
- Platform-specific embodiment logic that belongs in environment layers such as `CELT`.
- Target-repo-specific governance that belongs in `EDITING_<Repo>.md` artifacts.

## Repository Shape

During the transition, this repo contains two surfaces:

- The root surface, which is reserved for the emerging kernel deliverable.
- The `ALT/` donor surface, which preserves the earlier autonomy-layer scaffold so its reusable material can be classified and extracted intentionally.

Interactive process tracking remains workspace-level in ephemeral work files rather than in this repo.

## Relationship To The Ecosystem

- Every Operative begins as an instance of this kernel and adds selected upstream layers.
- Included source-bearing layer repos are mounted into an Operative repo as pinned submodules.
- `ASSEMBLY` records included repos, pinned states, edit enablement, and generated outputs.
- Environment-layer deployment remains a separate embodiment step rather than part of the platform-agnostic kernel surface.

## Maintainer Guidance

- Treat the root of this repo as the canonical home of the shared kernel deliverable.
- Treat `ALT/` as temporary donor material, not as live kernel canon.
- When extracting useful material from `ALT/`, rewrite it into kernel terms rather than carrying autonomy-layer framing forward unchanged.
- Remove donor material only after the replacement kernel material has landed cleanly.
