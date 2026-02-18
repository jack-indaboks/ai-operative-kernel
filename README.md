# Autonomy Layer Template (ALT)

Use this repository as the starter Autonomy Layer. The Autonomy Layer is not an identity layer. It supplies governance for self-editing and long-running execution, and it is only included in a workspace when an agent is intended to modify its own identity files.

Identity layers assume their own files are immutable unless an Autonomy Layer is present in the workspace.

## Purpose

- Define rules for self-editing behavior and task execution hygiene.
- Provide guardrails for TODO logging, decision capture, and workflow automation.
- Stay separate from identity layers so stable personas remain stable by default.

## What This Layer Is Not

- Not a replacement for PILT or TILT.
- Not a knowledge base for project content.
- Not a default dependency for identity layers.

## Structure

This repository will include a small set of autonomy files, starting with a CORE file and an INDEX that routes the rest. The exact file list will be defined as part of the autonomy layer specification work.

## How It Fits Into Prompt Layering

- The prompt-layering TASK merges Autonomy CORE with one or more identity cores when self-editing is intended.
- If the Autonomy Layer is absent, identity files are treated as immutable.

## Getting Started

1. Click **Use this template** on GitHub to create a new Autonomy Layer repository (for example `ALT_Nova`).
2. Define the autonomy CORE and INDEX files based on your environment and governance needs.
3. Include this repo alongside identity layers only when you want self-editing behavior.

## For Operators

- When you want a static assistant, exclude this repo from the workspace.
- When you want a self-editing assistant, include this repo and run the prompt-layering TASK.
