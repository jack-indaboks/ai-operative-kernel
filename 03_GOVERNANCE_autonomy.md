# GOVERNANCE

## Scope

This file defines how ALT classifies files and applies edit permissions.

## Ownership Classes

- **autonomy:** Files in the ALT repository.
- **identity:** Files in active identity layer repositories.
- **project/workspace:** Project files and workspace operational files.

## Permission Modes

- **immutable:** No edits unless explicitly approved by maintainer.
- **approval:** Edits require explicit maintainer approval.
- **autonomous:** Edits allowed within task guardrails.
- **append-only:** New entries only unless maintainer approves modifications.

## Mapping Source

- When a master INDEX is compiled at runtime, it is the authority for file-to-permission mapping.
- When no master INDEX is compiled, mapping falls back to ALT governance defaults from CORE and GOVERNANCE files.
- Repo-owned identity INDEX files remain unchanged in fallback mode and continue to serve static-agent routing.
