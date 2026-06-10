# Single doc: "validate and revise <doc>"

Law lives in the hub. This flow is bounded by one named doc, by design —
if it stops being cheap, it stops being used.

## Preconditions

A confirmed index (hub: universal gate; none → portfolio.md / audit
Phase 0 first). The doc has an index row; if not, it's either born now
(new-docs.md, born-doc gate) or it's untracked debris — interview.

## Process

1. **Read the doc's index row first.** Class and Reader decide
   everything:
   - **Point-in-time** → meta-checks only (superseded-but-unmarked,
     missing date, linked-as-live, broken refs). Never rewrite the body.
   - **Evergreen + Reader `contributor`** → continue here.
   - **Evergreen + Reader `user` or `adopter`** → **escalate**: this
     entry point hands off to user-docs.md / marketing.md and the study
     level rises to that genre's — a revision gets the genre's craft law
     (voice, story, cast), not just claim-rechecking. The cheap path
     never silently strips a genre's law.
2. Re-verify the doc's claims under the hub rubric — verify the verb, the
   performer, the citations. Auto-fix the determinate; collect the rest
   and interview.
3. `docmaint scan` — fix terminology violations this doc carries (the
   dictionary clause applies).
4. Stamping precondition: one independent verifier re-checks the applied
   edits with citations. Then `docmaint stamp --set <doc> [--deferred N]`.
5. Leave the edits uncommitted for human review.
