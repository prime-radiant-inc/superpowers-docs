---
name: documentation
description: Use when documentation work comes up in any form — updating docs after code changes, auditing docs against reality, writing user guides, tutorials, READMEs, product overviews or HTML brochures, defining or disputing terminology ("document this term"), revising one named doc ("validate and revise X"), deciding what docs a project needs, or bootstrapping docs for a project that has none.
---

# Documentation

## Overview

A doc is a set of **claims about reality**, written for a **named reader in
a named moment**. This skill is a project's documentation department in one
loop — study the project and its readers, decide the portfolio with the
human, write with the genre's craft, verify adversarially, maintain as the
code moves; maintenance is the same loop re-entered with a diff. The same
law binds every flow: classify first, auto-fix only the determinate, route
the ambiguous to the human, never rewrite a historical record, never let an
uncashed claim ship. **Violating the letter of these rules is violating the
spirit of them.** "I was bringing the docs up to date" is exactly how
design docs get their history erased.

## Dispatch — read the flow file before doing anything

Study first, scaled to the request (next section), then the row:

| Situation | You MUST read | Study |
| --- | --- | --- |
| No index / no docs / "set up docs" / "what docs does this project need?" | `references/portfolio.md`, then the genre flows | full |
| Full audit: "docs are out of date", pre-release, untrusted doc set | `references/audit.md` | full |
| Routine re-check of previously audited docs | `references/incremental.md` | micro |
| Just finished code work; update the docs that ride along | `references/write-path.md` | micro |
| "Document this term X"; create/extend the dictionary; term disputes; exceptions | `references/dictionary.md` | micro |
| "Validate and revise <doc>" — one named doc | `references/single-doc.md` | micro, escalates |
| Writing a brand-new engineering/contributor doc; "where does this doc go?" | `references/new-docs.md` | standard |
| User-facing docs: getting started, tutorial, how-to, user reference | `references/user-docs.md` | standard; set redesign: full |
| Adopter-facing: BROCHURE.md, the brochure site, README intro, positioning | `references/marketing.md` | full |

These are hard gates: do not start a flow from memory of this table. Flows
add process; the law below binds all of them and is never restated in flow
files.

**Precedence:** "validate and revise X" always *enters* through
single-doc.md, which reads X's Reader cell first; `user` and `adopter` docs
escalate to their genre flow and its study level — the cheap path never
skips a genre's craft law. **Universal gate:** no confirmed index → no
editing flow runs; bootstrap via portfolio.md / audit Phase 0 first.

## Scaled study

Study is proportional to the request — fixed-cost front-loading is the
ceremony this skill exists to avoid.

- **Micro** — read the index and dictionary; no human gate.
- **Standard** — micro, plus the portfolio rows the work touches; the
  born-doc confirm (the classification gate at standard depth) fires only
  if a new doc or row is born.
- **Full** — the complete portfolio pass (`references/portfolio.md`): real
  readers × real moments, existing docs mapped, gaps/excess/mis-addresses
  named, confirmed with the human as **one batch** — the genre's cast and
  voice confirms ride the same gate.

## STOP: classify before you edit (evergreen vs. point-in-time)

The single biggest failure is rewriting a dated design/plan/spec to "match
the code." A spec from three months ago describing how something *should*
work is **not wrong** when the code later diverged — editing it to match
destroys the record.

- **Evergreen** — README, ABOUT, CLAUDE.md, tutorials, living API/schema
  reference. Contract: *reflects current reality*. Drift is a defect → fix.
- **Point-in-time** — design specs, plans, brainstorm notes (often dated, or
  under `docs/specs|plans|…`). Contract: *true as of its date*. Drift vs.
  current code is **expected**. Never rewrite to match code; at most add a
  supersede banner or as-of date.
- **Mixed / unclear** — conflicting signals (a dated-folder `README`) → treat
  the whole doc as interview-only.

Classify the doc set **first**, at the **group level** (folder globs + named
exceptions), and **confirm with the human** before editing anything.
Precedence: a point-in-time signal (dated filename, point-in-time directory)
**beats** an evergreen name like `README`. Do **not** decide this per-doc by
gut as you go — surface it as one decision.

**The classification confirmation is the one gate you never skip** — not
under time pressure, not under authority, not under "just be decisive, don't
kick it back to me." A one-line confirm costs seconds; skipping it is what
turns an audit into an erased design record. And when classification is
genuinely ambiguous (e.g. a reference-looking file inside a `specs/` folder
that also holds design docs), **resolve to the safe side — treat it as
point-in-time and confirm** — because a body rewrite is irreversible to the
record. Disclosing your assumption in a footnote *after* you've rewritten the
body is too late.

The confirmed classification **persists in the doc index** (`Class` column —
see Artifacts). Editing flows gate on it: no index → run audit Phase 0 first.
Never classify by gut mid-flow.

## Scope & exclusions

Default target: `README`, top-level `*.md`, `docs/**`, `CLAUDE.md`. **Always
exclude:** git-ignored paths, `.claude/`, `.private-journal/`, worktrees;
**generated / foreign-owned docs** (any "do not edit" / "generated by"
sentinel — editing them is futile, the next regeneration wipes it);
non-markdown. The dictionary (`docs/DICTIONARY.md`) is excluded from its own
terminology sweep.

## The rubric: what may be auto-fixed

Auto-fix a claim **only when ALL hold**:

1. the doc is **evergreen**;
2. the claim is **mechanical** — an identifier/path, CLI flag, config/env
   name+default, API route/field, or a token-level example fix;
3. a **single live (non-test) counterpart** exists in the code, so the right
   value is *determined, not guessed* (multiple hits / test-only / no hit →
   interview);
4. it's a **local token replacement** that leaves the surrounding sentence
   true;
5. a missing counterpart is **confirmed removed vs. renamed via git history**
   (`git log -S`, `--follow`, blame) before you conclude anything.

**Dictionary clause.** In evergreen prose only, a deprecated synonym may be
auto-fixed when ALL hold: the synonym maps to exactly one dictionary entry
(whose heading is the replacement); the match is whole-word; no exception
covers it; and the replacement leaves the surrounding sentence true. The
determinant is the dictionary instead of a code counterpart — conditions 1, 4
and 5 still apply. Code identifiers, UI strings: never auto-fixed — findings
only (rename / add entry / add exception). Commit messages: dictionary terms
in new ones; history is never flagged.

**Always interview — never auto-fix — regardless of category:**

- **Counts & inventories** ("14 workflows", "~40 files") — no canonical
  counting convention.
- **Bare line-number citations** (`file.go:120-130`) — they drift on every
  edit. Recommend rewriting to `file:symbol`; never silently renumber.
- **Absence / negative claims** ("there is no env-var fallback") — you can't
  grep-prove a negative.
- **Cross-reference repair** — detecting a broken link is fine; choosing its
  new target rarely is.
- **Structural changes to embedded examples** — rewriting an example's
  *shape* to a new schema.
- **Behavioral / semantic claims** ("does X when Y", sequencing, rationale).
- **Claims whose ground truth lives in another repo or an external binary.**

## Verify the claim, not just the symbol

Confirming that the *thing* a doc names exists is not confirming the *claim
about it*. A claim of the form "X is validated / X happens when Y / X is done
by Z / X is configured as W" is verified only by the **code path that enacts
it** — the validator that rejects, the handler that closes the stream, the
function that computes the value, the line that loads the asset — **not** by
X's mere existence. Check the verb, not just the noun.

- "the loader rejects an emit node that declares `runner`" → find the
  rejection in the validator, or the claim is false.
- "the stream closes when the run is terminal" → find the close on *every*
  terminal state, or name the one it misses.
- "diffs are computed in `internal/document`" → find the call there, not just
  the function's definition.
- "Tailwind is loaded from a CDN" → check the actual `<script src>`, not that
  Tailwind is used.

This is the most common false-`matches`: the noun checks out, so the verifier
waves the verb through. State the mechanism, and point the citation at the
code that *does* the thing claimed.

**The performer rule.** A surface cashes a claim *for a reader* only if
that reader is the one who performs it: operator plumbing cannot cash a
user-path claim. When the addressed reader's real surface lives in another
repo (a client, a plugin), cite that named external surface — and only if
it exists today; otherwise the claim is roadmap.

## Audience law (what ships to users and adopters)

- **Reader, moment, job.** Name the reader as a person-in-a-moment and
  what they can DO when the doc has done its job. A demographic is not a
  reader; a doc with no job is not written. This routes the dispatch and
  gates every genre flow.
- **Claims must cash.** A capability claim enters citing the surface that
  enacts it (verify the verb). An outcome claim needs a real measurement,
  or is rewritten as the capability it gestures at. Rhetoric may amplify
  verified claims, never substitute for them. Future work is cut or
  labeled roadmap.
- **Show real things.** Every command, output, number, and demo in an
  audience doc was produced from the project as it is — run, not
  imagined. Fabricated example output is the signature failure of the
  genre.
- **Honesty floor.** Superlatives need measurements; comparisons dated
  and fair; limitations stated; who it's NOT for stated; costs stated to
  whoever bears them — never sell one reader's burden as another
  reader's benefit. "It's just marketing" is the rationalization this
  skill exists to kill.
- **Story law** (adopter artifacts): the problem beat is load-bearing,
  must cash like any claim, and **stands in its own beat — stated and
  left unresolved there**, never introduced and answered in the same
  breath; one controlling idea, written down before composing; every
  beat turns — a section that leaves the reader where it found them is
  cut. Structure from the storytellers' canon, facts from the repo
  (`references/marketing.md`).
- **Prose law.** The writing step uses
  elements-of-style:writing-clearly-and-concisely where available — and
  for adopter-facing artifacts the vendored copy at
  `references/elements-of-style.md` is **required reading before
  drafting**, no availability escape. Writing happens in the resolved
  project voice (`references/voice.md`: the project's `## Voice`
  dictionary section, else a preset — the publication writer for
  adopter artifacts, the engineer everywhere else). The independent
  verifier checks voice exactly as it checks claims.

## Artifacts: dictionary and index

The skill maintains exactly **two** artifacts per project, plus inline
stamps. Never a third metadata file.

- **`docs/DICTIONARY.md`** — normative terminology for docs, code
  identifiers, commit messages, and UI strings; divergences live in its
  Exceptions section, scoped by path globs only. An optional `## Voice`
  section (inert to docmaint's parser) carries the project voice —
  `references/voice.md`. Template: `templates/DICTIONARY-template.md`;
  grammar and lifecycle: `references/dictionary.md`. Evergreen, stamped,
  and the canonical owner of terminology.
- **The doc index** — a sentinel-fenced table (`<!-- doc-index:begin/end -->`)
  in `docs/README.md`, or standalone `docs/INDEX.md` where no README exists.
  Columns: Doc | What | Reader | Class | Owns. `Reader` is the addressed
  reader (`user`, `operator`, `contributor`, `adopter`, `+`-joined for
  sectioned docs, `—` for point-in-time rows) — agent judgment, no
  tooling: the cell records the *addressed* reader; whether the doc's
  surfaces are ones that reader performs is checked by agents (the
  performer rule). `Class` is the persisted classify-and-confirm output;
  `Owns` is machine-readable path globs (what `docmaint stale` diffs). A
  `Decided gaps` HTML comment below the fence records confirmed
  won't-write decisions so future studies don't re-litigate them.
  Template: `templates/INDEX-template.md`. (Legacy 4-column indexes from
  the predecessor skill parse fine — docmaint reads column positions from
  the header — and gain Reader at their next full study.)
- **`docmaint`** (`scan | stamp | stale`, `--help` for usage) does the
  mechanical work. It never edits docs; agents do, under the rubric. It
  ships in this skill's `scripts/` directory — invoke it as
  `${CLAUDE_SKILL_DIR}/scripts/docmaint` (the documented skill-content
  substitution; for plugin skills it resolves to the skill's subdirectory
  within the plugin), and pass `--root <target-repo>` unless your cwd is
  already the target repo root (`--root` defaults to cwd). Flow files
  write bare `docmaint <subcommand>`; this resolution rule applies
  everywhere.

## Stamp contract

Evergreen docs carry one idempotent block at EOF (`docmaint stamp` maintains
it; sentinel `<!-- doc-audit:last-reviewed -->`):

```
---
<!-- doc-audit:last-reviewed -->
_Last reviewed: 2026-06-09 · commit `abc1234` · verified against code (2 claims deferred to review)._
```

The SHA is provenance **and** the incremental cursor — a deliberate change
from the predecessor skill. Incremental re-audits are **triage, not
soundness**: deferred claims keep a doc on the worklist regardless of SHA;
claims with ground truth outside the repo are cleared only by full audits;
terminology never depends on stamps (`docmaint scan` full-sweeps every run).
**Stamping precondition (all flows):** no stamp without independent
verification of the applied edits — full audits use two or more competing
verifiers (Phase 3); diff- or worklist-bounded flows use at least one
independent verifier. Don't stamp point-in-time docs. Stamp only what you
verified — and any evergreen claim you could *not* verify this pass,
including claims whose ground truth lives outside the repo, counts toward
`--deferred N`. Never let an unverified claim ride under a clean stamp.

**Regeneration rule.** The brochure site (`docs/index.html`) is rendered
from `docs/BROCHURE.md` and carries a first-line sentinel naming
BROCHURE.md's stamp SHA. **Any flow that restamps BROCHURE.md** —
write-path, incremental, and audit included — compares the site's
sentinel SHA to the new stamp SHA and re-renders on mismatch
(`references/marketing.md`, `references/brochure-design.md`). One skill
owns both artifacts; a restamp without the re-render check is a defect,
not an accepted cost.

## Pragmatism law

- Docs exist for readers. Before creating any doc, entry, or artifact, name
  the reader. No reader → don't write it.
- Adopt existing structures before imposing new ones.
- Two artifacts per project (dictionary, index) plus stamps. Never a third.
- A coverage gap is a finding to file, not a mandate to generate a doc.
- The dictionary stays readable in one sitting: load-bearing terms only.
- Write-path stays bounded by the diff. If maintenance isn't cheap, it won't
  happen.
- The portfolio is sized to the project: a 300-line utility earns a
  README, not a doc suite.
- Every flow leaves its edits **uncommitted** for human review. Verified
  is not reviewed.

## Red flags — STOP

- "I'll bring the docs up to date" across a whole spec/plan set **without
  classifying first**. → Classify and confirm first.
- About to **renumber** a `file:line` citation. → Convert to `file:symbol`
  via interview.
- About to **rewrite an example's structure** to the new schema. →
  Interview, not auto-fix.
- Pressured to "be decisive / don't confirm", about to classify docs
  yourself and **rewrite their bodies**. → The classification confirm is the
  one gate you never skip. Surface it; a one-line yes costs seconds.
- Concluding a feature was "removed" / deleting its docs **from a grep
  miss**. → Check git history first.
- "Close enough, I'll just fix the count." → Counts go to the human.
- Editing a file that says "generated" / "do not edit". → Skip it.
- Marking a claim "matches" **without a citation**. → Cite it or don't claim
  it.
- About to **finish without a second adversarial pass over your own edits**.
  → In a full audit, run the competing verify pass (audit Phase 3) first; in
  bounded flows, the one-verifier stamping precondition applies. Fix what it
  finds.
- Marking a claim "matches" because the **symbol exists**, without checking
  the code *does* what's claimed about it. → Verify the verb, not the noun.
- Audited each doc, never looked at the **set** (duplication, gaps,
  contradictions, index). → Per-doc passes are blind to set-level defects;
  run the corpus review (audit Phase 4 — applies to the full-audit flow).
- About to remove a `[permanent]` exception, or a `[temporary]` one on scan
  evidence alone. → Permanent: never. Temporary: confirm via git history
  first (a grep miss is not resolution).
- About to stamp a doc whose edits nobody independently verified. → The
  stamping precondition applies in every flow, not just full audits.
- About to write a doc, or a dictionary entry, no one asked to read. → Name
  the reader (pragmatism law).
- About to add a third per-project metadata file. → Two artifacts. Never a
  third.
- About to write an exception scope in prose ("code touching X"). → Path
  globs only.
- Editing docs in a project with no confirmed index `Class` column. → Run
  audit Phase 0 first.
- About to render the brochure site with no governed `BROCHURE.md`
  behind it. → The render inherits; it never originates (marketing.md).
- A brochure-site section without a citation line. → Every section cites
  the doc that verifies it.
- About to **commit** doc work nobody reviewed. → Verified ≠ reviewed;
  every flow leaves edits uncommitted.
- "While I'm in here" — about to write a CLAUDE.md, an extra doc, or fill
  a gap nobody asked about, mid-flow. → Gaps are findings; new docs get
  the born-doc gate.
- A "get started" whose first path is clone-and-build for a deployed
  product. → That's the contributor's journey; name the primary reader
  (the performer rule).
- "Get the docs into shape" handled as claim-verification only. → Run the
  portfolio pass; per-doc truth says nothing about who reads, what's
  missing, or what's mis-addressed.
- An enacting surface attributed to a reader who never performs it. → The
  performer rule; re-address the doc or re-route the claim.
- An outcome claim with no measurement; an absolute ("no third party
  ever…"); example output never run. → Cash it, soften it, or cut it.

## Rationalizations

| Excuse | Reality |
|--------|---------|
| "The spec says X but the code says Y, so the spec is wrong." | Only if the spec is **evergreen**. A point-in-time design doc is allowed to differ — classify first. |
| "It's obviously a reference doc, I'll just fix it." | Per-doc gut calls are how design docs get their history rewritten. Confirm the classification with the human. |
| "They said be decisive and not to kick decisions back — so I'll classify and rewrite myself." | The classification confirm is the one gate you never skip; it's the difference between fixing a doc and erasing a design record. A one-line confirm costs seconds. |
| "Nothing in it reads as a dated design narrative, so it's evergreen." | Absence of obvious design language isn't proof of evergreen, especially in a mixed folder like `specs/`. Ambiguous + destructive edit → treat as point-in-time and confirm. |
| "I disclosed my assumption at the end." | A footnote after you've rewritten the body is too late — the record is already changed. Confirm *before* editing, not after. |
| "The line number moved, I'll update it." | Line numbers drift on every edit; re-pinning re-breaks it. Convert to `file:symbol`. |
| "I'll bring the example up to the new schema." | Structural example rewrites change meaning → interview, don't auto-fix. |
| "The grep found nothing, the feature's gone." | A grep miss is not proof of removal. Check git history; it may be renamed. |
| "37 vs. ~40 is close, I'll just write the real number." | Counts have no canonical convention — hand it to the human. |
| "The symbol/route/field exists, so the claim checks out." | Existence ≠ the claim. Verify the code path that *enacts* it (the validator/handler/call site), not just that the noun exists. |
| "Every doc verified clean, so the docs are good." | Per-doc accuracy ≠ a healthy set. Duplication, missing docs, and cross-doc contradictions only surface at the corpus level (audit Phase 4). |
| "Scan found zero hits, the exception is resolved." | A grep miss is not resolution — confirm via `git log -S` first; `[permanent]` exceptions are never removed on scan evidence. |
| "It's a tiny doc edit, stamping without a verifier is fine." | The stamp *means* independently verified. No verifier, no stamp. |
| "The docs feel incomplete, I'll add a doc for each gap." | Gaps are findings. A doc with no reader is debt, not coverage. |
| "It's a brochure — the HTML is the artifact, I'll write it directly." | The render inherits from governed BROCHURE.md; claims live where stamps reach. No source doc, no render. |
| "The work is verified, so I'll commit it." | Verified ≠ reviewed. Every flow leaves the tree uncommitted for the human. |
| "While I'm in here, I'll also write the CLAUDE.md / fill the gaps." | Gaps are findings; a doc no one asked to read is debt. New docs get the born-doc gate. |
| "Getting started obviously means: clone the repo." | That's the contributor's first success. Name the primary reader; order paths by *their* journey. |
| "The docs are in shape — every claim verifies." | Per-doc truth ≠ the right portfolio. Study asks who reads, what's missing, what's mis-addressed. |
| "The page needs to be compelling, so the language has to lift." | A concrete benefit carries its own excitement (voice law). Uncashed lift is the slop this skill bans. |

## Common mistakes

- Editing before classifying.
- Spawning one subagent per point-in-time doc — batch them; they aren't
  claim-verified.
- An unbounded first-run interview backlog — prioritize, defer the tail to a
  report.
- Auto-committing any flow's output — leave it uncommitted for human
  review (both authoring baselines committed unbidden; the counter is
  law, not preference).
- Declaring done without adversarially verifying your own edits — your fixes
  are a prime hiding spot for confident-but-wrong claims (audit Phase 3).
- Treating per-doc verification as the whole job — duplication, gaps,
  cross-doc contradictions, and a missing index are set-level defects
  invisible to a per-doc pass (audit Phase 4).
- Verifying the noun, not the verb — confirming a symbol exists instead of
  confirming the code does what the doc claims about it.
- Treating `stale` output as proof of cleanliness — it is triage; soundness
  comes from full audits.
