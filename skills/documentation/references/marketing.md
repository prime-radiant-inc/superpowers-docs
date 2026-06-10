# Marketing flow: BROCHURE.md → brochure.html, README hook

Law lives in the hub (claims-must-cash incl. the performer rule, honesty
floor, story law, voice law, regeneration rule, the gates). This flow adds
the genre's process. Craft companions: voice.md (speaker, slop tells,
exemplar test), brochure-design.md (the rendered deck's visual standard).

## The cast

The "deciding whether to adopt" reader is a **cast**, not a person: the
**user** (hands on keyboard; receives the capability) and the
**owner/operator** (deploys it; carries the cost and risk). When they're
the same human they are different moments, which the reader law already
treats as different readers. The **contributor** is not this artifact's
audience — at most a one-line pointer to the engineering docs. Each cast
member gets their own proof type (user: the experience, real commands,
demos; owner: mechanisms and invariants) and their own exit (CTA).
Strategic order is user-first: the user acts create a champion; the owner
act is the trust brief that champion hands their platform owner. For a
server-side component whose end-user surface lives in a client repo, the
user act cites that external surface or is labeled roadmap (hub: the
performer rule decides).

## Process

1. **Full study** (portfolio.md): confirm the index, the cast for this
   project, and the resolved voice (voice.md) — **one batched human
   gate** before any writing.
2. **Write the thesis first** (story law): one sentence; every section
   and slide must advance it.
3. **`docs/BROCHURE.md`** — the canonical positioning document, governed
   end to end. Birth goes through new-docs.md (index row — Reader
   `adopter` — classification, verification, stamp); this flow adds the
   section shape (templates/BROCHURE-template.md): one-sentence
   what-it-is; what you get (user; problem beat first); using it (user;
   first-success on an existing deployment); running it (owner); fit by
   role incl. who it's NOT for; limitations each tagged by who bears
   them; getting started, one path per cast member. **Owns rule:** the
   enacting surfaces of the capabilities it names — not the whole tree.
   Every capability bullet carries its cash.
4. **Render `docs/brochure.html`** per brochure-design.md. Content is
   inherited: a capability appears in the deck only if BROCHURE.md
   carries it verified. The arc is three acts plus a close — Act I what
   you get (user; problem beat, then transformation; the user is the
   subject of every verb; zero architecture), Act II using it (user;
   real commands), Act III running it (owner; engineering register; the
   warm-accent shift), close: one door per cast member plus the
   contributor pointer. One voice throughout; acts change audience,
   never speaker. First line is the sentinel (brochure-design.md); no
   index row for the rendered file — BROCHURE.md's row carries the
   claims, the sentinel keeps `scan` off the render.
5. **README intro — hook plus link, never a restatement.** The README
   carries BROCHURE.md's one-sentence what-it-is verbatim (BROCHURE.md
   owns it) and a pointer. A restated capability list is the duplication
   the corpus pass exists to kill.
6. **Verify before stamping** (hub precondition): the independent
   verifier checks claims (cash + performer), voice (banned list +
   exemplar test), story (thesis, problem beat, beat-turns), and the
   citation footers. Then stamp BROCHURE.md; the render carries
   BROCHURE.md's stamp SHA in its sentinel.
7. **Leave it uncommitted** for human review, like every audit edit.

## Strunk, elevated for this genre

Rule 12 (definite, specific, concrete) is the antidote to vapor; Rule 11
(positive form) the antidote to over-hedged mush; Rule 13 (omit needless
words); and Section V "Interesting": never announce that the product is
exciting — make it so.

## Revision

"Validate and revise BROCHURE.md" (or the brochure) re-enters here via
single-doc.md's escalation — the genre's craft law applies to revisions,
not only births. Routine restamps by maintenance flows trigger the
regeneration rule (hub): sentinel SHA vs. stamp SHA, re-render on
mismatch.
