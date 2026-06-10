# User docs flow: set design + per-doc craft

Law lives in the hub. Birth mechanics are new-docs.md's (index row,
classification, verification, stamp) — this flow owns the set design and
the craft layered on top. Prose: elements-of-style where available, in the
resolved voice (voice.md; the teacher preset is this genre's natural fit).

## Set-level first (standard study; full for a set redesign)

1. Inventory the existing user-facing surface (the index's Reader column
   is the worklist; `user` rows plus gaps).
2. Name the reader journeys: evaluate → first success → routine use →
   troubleshoot/recover.
3. Propose a doc-set plan mapping docs to journey stages — one doc, one
   job. Doc types are Diátaxis-informed (tutorial = first success, how-to
   = task, reference = lookup, explanation = concepts) but serve the
   journeys, not the taxonomy: a project gets the docs its journeys need,
   never four-of-each.
4. **Confirm the plan with the human as one batch decision** — together
   with the resolved voice. A single new doc into an existing set
   confirms at the born-doc gate (the classification gate at standard
   depth). Only then write.

## Per-doc craft

- Lead with what the reader gets; the job statement shapes the first
  paragraph.
- **Name the primary reader in the doc's first lines, and order paths by
  that reader's journey.** When cast members share a doc, the named
  primary's path comes first; a "pick your path" table is fine, but the
  default path is the primary reader's. A getting-started whose first
  path is `git clone` + build-from-source is addressing a contributor —
  say so or re-address it (hub: the performer rule).
- Tutorials are measured by time-to-first-success; say up front what the
  reader will have at the end and roughly how long it takes.
- Real commands with really-produced output (hub: show real things).
- Prerequisites explicit, up front — including the ones the README
  forgot.
- Failure modes and recovery live next to the commands that fail.
- Project terms follow the dictionary but are defined for outsiders on
  first use; a user doc that must mention a deprecated term to orient
  outsiders ("formerly called X") uses the dictionary's `[manual]` /
  exception machinery rather than tripping scan.
- A user doc never points a user at internal material — "see the design
  doc" is a defect. Pointers go to other user docs or the operator docs.
- **Leave the work uncommitted** for human review, like every flow.

## Revision

User docs are evergreen index rows with Owns globs; write-path and
incremental maintain them. "Validate and revise <user doc>" enters via
single-doc.md and escalates here — craft standards apply to revisions.
This flow re-enters at set level only for redesigns ("our getting-started
guide sucks" reruns the journey pass).
