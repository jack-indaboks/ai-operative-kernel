# TASKS

This file is the kernel-local task surface. Run the tasks defined here when their triggers match. If a kernel-owned task name is reserved but no workflow is defined here yet, stop and report the gap rather than inferring the missing procedure.

## curate-updates
- **Requirements:** file-read, file-write
- **Trigger Phrase / Intent:** "curate updates", "review upstream updates", "advance downstream canon"
- **Purpose:** Selectively advance downstream canon through upstream changes without clobbering downstream decisions.
- **When to Run:** When a downstream Operative, layer, or template needs to review upstream changelog entries before adopting them.
- **Workflow:**
  1. Review the relevant upstream `09_CHANGELOG_*` entries and any companion artifacts referenced there.
  2. Record a downstream disposition for each entry as `Included`, `Excluded`, or `Deferred`.
  3. Apply approved changes in a way that preserves downstream intent and provenance.
  4. Update downstream tracking and report any remaining follow-up.

## Reserved Kernel Tasks

- `assemble-operative`: reserved to the kernel; detailed workflow remains to be drafted in this file.