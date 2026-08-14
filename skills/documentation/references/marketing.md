# Marketing flow: BROCHURE.md → the brochure site, README hook

Law lives in the hub (claims-must-cash incl. the performer rule, honesty
floor, story law, voice law, regeneration rule, the gates). This flow adds
the genre's process. Craft companions: voice.md (speaker, slop tells,
exemplar test), brochure-design.md (the brochure site's visual standard),
and **elements-of-style.md — required reading before drafting any adopter
copy.** This genre defaults to the publication-writer voice (voice.md
preset 5): a less technical reader, sold the benefit, in plain English
with that preset's hard bans (no contrastive negation, no em dashes).

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
   gate** before any writing. **A broad instruction is not the batch
   confirm**: even when the human pre-authorized scope ("make the
   brochure"), the gate still asks its specific questions — voice, cast,
   section plan — because those weren't in the instruction.
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
   Every capability bullet carries its cash. A recorded session's output
   often depends on environment facts (the directory name feeding a
   scaffold, tool versions, an available local checkout): state every
   fact the shown output depends on, or the reader's replay diverges
   from the "real session" and the realness claim curdles. And a real
   transcript is carried whole — eliding an inconvenient line (a
   warning, an error) from output labeled real is fabrication, not
   tidying.
4. **Render the brochure site, `docs/index.html`**, per
   brochure-design.md — a single scrolling product page suitable for
   GitHub Pages, not a slide deck. Content is inherited: a capability
   appears on the page only if BROCHURE.md carries it verified. The
   section order is the story arc: **the problem in its own section,
   stated and left unresolved** (never introduce and resolve the problem
   in the same section); then what you get (user, benefit-first); using
   it (user; real commands); running it (the owner band, warm-accent
   shift); doors (one per cast member) plus the contributor pointer.
   One voice throughout; sections change audience, never speaker. First
   line is the sentinel (brochure-design.md); no index row for the
   rendered file — BROCHURE.md's row carries the claims, the sentinel
   keeps `scan` off the render.
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

## Strunk, required for this genre

Read `references/elements-of-style.md` (vendored, public domain) before
drafting — this is a hard step, not a suggestion, and the verifier checks
the result against it. Four rules are elevated to law here: Rule 12
(definite, specific, concrete) is the antidote to vapor; Rule 11
(positive form) the antidote both to over-hedged mush and to
selling-by-negation; Rule 13 (omit needless words); and Section V
"Interesting": never announce that the product is exciting — make it so.

## Revision

"Validate and revise BROCHURE.md" (or the brochure site) re-enters here
via single-doc.md's escalation — the genre's craft law applies to
revisions, not only births. Routine restamps by maintenance flows trigger
the regeneration rule (hub): the site's sentinel SHA vs. BROCHURE.md's
stamp SHA, re-render on mismatch.
