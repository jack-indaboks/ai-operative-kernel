# TASKS

Task macros keyed to short triggers. When a trigger is invoked, run the associated workflow exactly as written.

## Reconcile Identity Edits
- **Requirements:** file-read, file-write
- **Trigger Phrase / Intent:** "reconcile identity edits", "restore parity", "sync identity governance"
- **Purpose:** Restore parity after ad hoc or out-of-band identity edits.
- **When to Run:** After identity files changed outside standard autonomy workflows.
- **Workflow:**
  1. Identify modified identity files and summarize what changed.
  2. Confirm required side effects (INDEX routing, cross-file references, and identity DECISIONS entries where applicable).
  3. Apply missing parity updates with minimal diffs.
  4. Report the reconciliation summary and remaining risks.

