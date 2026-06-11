# RED/GREEN record — superpowers-docs v0.1.0 build day

Point-in-time record of the Iron-Law evidence behind the initial skill
text (2026-06-10). Workers were claude-session-driver sessions in
isolated worktrees; RED ran without the plugin, GREEN with
`--plugin-dir ~/git/superpowers-docs`. Standing caveat for all runs: the
predecessor skill (dotfiles `maintaining-documentation`, v1) is globally
deployed, so RED runs measure the failures that remain WITH v1 loaded —
exactly the delta this plugin must close, since it subsumes v1.

## RED 1 — brochure (worktree of a private infrastructure repo, the
family's standing eval target)

Prompt: create docs/brochure.html, "make it compelling."
Observed (commit bd87a70 in the worktree): a 14-slide deck with decent
engineer voice and a real problem beat (the stamped-docs environment
helps) — but **no generated-file sentinel** (file starts `<!doctype
html>`), **zero citation footers**, **no governed source doc** (claims
live only in the render), **no index row**, **no human gate**,
**auto-committed into the governed repo**, stacked imperative-fragment
headlines, and two self-flagged unresolved claims left in the artifact
(an uncashable absolute and an elided prerequisite).
Seeds → marketing.md process; hub red flags (render-without-source,
slide-without-citation, commit-unreviewed); rationalization rows
("the HTML is the artifact", "verified, so I'll commit it", "the language
has to lift").

## RED 2 — getting-started (same private repo's worktree)

Prompt: write docs/getting-started.md, "friendly and complete."
Observed (commit 80ae3a7): craft discipline largely HELD via v1
(claims verified against enacting code, adversarial re-verify caught 3
real issues, scan clean, index row, stamp with 1 honestly-deferred
claim). Remaining failures: **auto-committed again**, **no named primary
reader** (clone-and-run local path leads; deployed-service user path
second), **no journey/set-level thinking**, **no born-doc gate**.
Seeds → user-docs.md (name the primary reader, order by their journey,
set-level first, uncommitted); hub ("getting started obviously means:
clone the repo").

## RED 3 — study ("get the docs into shape", clipfan worktree)

Prompt: "what docs does this project need? make the improvements."
Observed: v1 auto-fired its full audit — classification gate held
(stopped for confirmation), interviews fired on semantic rewrites
(ROADMAP reshape). But **zero reader enumeration, zero portfolio
thinking** — "what docs does it need" was answered entirely as
claim-verification plus structural hygiene — and the worker **offered to
write an unsolicited CLAUDE.md mid-flow** (scope-creep instinct; it did
ask). Run still in progress at log time; conclusions above were stable by
Phase 0–1.
Seeds → portfolio.md (the readers × moments pass v1 cannot supply); hub
("docs are in shape — every claim verifies"; "while I'm in here").

## RED 4 — ride-along: substituted

v1's write-path text is ported with mechanical deltas and was itself
born from v1's own TDD record; with v1 globally deployed a clean
no-skill RED is unobtainable. Substituted with: v1's existing evidence +
the GREEN-side port-equivalence expectation (no regression vs. v1
behavior). "Stamps without verifiers" was removed from RED expectations
(unobservable without the stamp concept) and lives in GREEN.

## GREEN 1 — "Document this term: <term>" (host-repo worktree)

Routed by the dispatch table (quoted the row: dictionary.md, micro
study). Stayed bounded; verified the existing entry against the enacting
code paths (verify-the-verb) and the docmaint matcher's
multi-word-synonym behavior; made no edits; routed the one judgment call
(a spelling inconsistency) to the human with a correctly-scoped
resolution incl. `[permanent]` exceptions for historical records. The
plugin fired, not v1, despite the overlap. **Pass.**

## GREEN 2 — "Validate and revise <one doc>" (same worktree)

single-doc.md flow: bounded 2-line diff, **left uncommitted** (the law
both RED authoring runs broke), one determinate token fix applied with a
code citation, restamp with 3 honestly-deferred claims (two with ground
truth outside the repo + one behavioral). The mandated adversarial
verifier caught a real pre-existing bug in the host project's admin
tooling that the first pass missed — routed to the project owner as a
behavioral finding, not auto-fixed (details live with that private
project, not here). Legacy 4-column index handled cleanly (no Reader
cell → no user/adopter escalation). **Pass.**

## GREEN 3/4 — born-doc gate + portfolio routing: PASS (clipfan live eval)

Full-study bootstrap on `/tmp/eval-clipfan` (branch `eval/docs-plugin`,
~3h13m, all uncommitted for review). The whole loop fired as designed:

- **The batched gate**: one multi-tab confirm (classification / births /
  audit scope; later a second batch for corrections / restructures /
  judgment calls / dictionary entries). ABOUT.md correctly excluded as
  foreign-owned (maintaining-project-map's). The human declined CLAUDE.md
  at the births tab → recorded in the index's **decided-gaps comment with
  dates and reasons** ("no brochure — internal proprietary tool, adopters
  are teammates served by README + ABOUT.md" — the cast law applied with
  judgment, not by rote).
- **Artifacts born conformant**: 5-column INDEX.md (Reader cells incl.
  `user+adopter` sectioned values; tight Owns globs), DICTIONARY.md (19
  entries) via the entry-batch approval. Independently re-verified after
  the run with the plugin's own docmaint: `scan` 0 violations, `stale`
  yields a working deferred-claims worklist, 9 evergreen docs stamped
  `2026-06-10 @ 5ed989c` with honest deferred counts (54 total,
  externals).
- **Verification at depth**: ~345 claims, 9 verification agents, ~40
  applied fixes incl. two restructures; the competing adversarial pass
  caught the worker's OWN bad fix (auth_version misplaced in the HMAC
  canonical string — would have broken client auth) before stamping.
- **Doc-or-code fork routed to the human**: `chmod +x dist/install.sh`
  fixed in the repo so the documented command works, by explicit human
  choice at the judgment tab.

## Baseline-vs-plugin, same repo (the subsumption delta, observed)

RED 3 (v1-only, ~2h, /tmp/red-study-clipfan) vs GREEN 3/4 (plugin):
v1 produced reader-named gap findings only at the END, as a byproduct of
truth repair; no up-front reader model, no portfolio gate, no decided-gaps
persistence, no Reader column, dictionary only *recommended* (finding #6).
The plugin led with all five and then ran the same truth-repair machinery.
Convergent judgments across both runs (ROADMAP reframe, PIT banners,
install.sh exec bit) confirm the ported v1 core is intact.

## GREEN 5 — marketing flow, end to end (clipfan brochure): PASS with one finding

Same-day follow-up at the human's request — reopening the recorded
"no brochure" decided gap (its rationale had gone stale; the repo is
public). The flow produced governed `docs/BROCHURE.md` (template section
shape; every capability cited; limitations tagged by bearer; stamped with
11 honest external-truth deferrals) and an 18 KB self-contained
`docs/brochure.html`: 11 slides, three acts + close, Act III warm-accent
shift, per-slide citation footers, correct sentinel pinning the source
stamp SHA (`scan` skips it; the regeneration cursor is armed). README got
hook-plus-pointer only. The verifier pair (claims attacker + voice/story/
design auditor) found zero fabrications — one rebuilt the binary and
byte-checked the `--help` output — and 12 real craft defects (footer
mis-citations, two deck details the source doc didn't carry, an X-not-Y
over budget, an unmarked elision), all fixed and re-confirmed by a third
agent before stamping. Render-verified in Chrome (hook + Act III).
Decided-gaps record updated to show the human reopening, with the other
gaps preserved.

**Finding:** the worker skipped the batched cast/voice confirm, treating
the human's launch instruction (which pre-authorized scope and audience)
as the gate. Scope was indeed pre-answered; voice and cast were not — it
self-resolved to the engineer default and flagged that for veto in its
report. Candidate flow tightening (Iron Law applies before any edit): "a
broad instruction is not the batch confirm; the gate asks its specific
questions even when scope arrives pre-authorized."

## RED 6 — human review of GREEN 5's artifact (2026-06-11)

The project owner reviewed the clipfan deck and rejected four things the
flow-as-written permitted — this is the failing test for the next round
of flow edits:

1. **Problem and promise mixed in one beat**: slide 2 is titled "What you
   get" but its body is the problem statement (isolated clipboards,
   OSC 52 half-works, images have no path). The story law said "problem
   beat first" but never said "in its own beat, unresolved."
2. **Wrong default voice for the genre**: engineer/mechanism register for
   an adopter audience that should be read as less technical and sold
   the benefit.
3. **AI prose tells survived the auditor**: 18 em dashes; contrastive
   negation as a selling device ("keeps outsiders out, not a bad
   insider") — the slop list's one-per-artifact X-not-Y budget is too
   loose for this genre, and em dashes weren't banned at all.
4. **Wrong artifact class**: a keynote deck, when the reader's real
   moment is "landing on a product page" — a brochure site suitable for
   GitHub Pages.

Owner's directives: default the brochure to a benefit-selling voice for
a less technical reader; render a brochure website, not a deck; REQUIRE
writing-clearly-and-concisely (vendor it into the plugin); plain English
that reads like an experienced published writer; zero contrastive
negation; zero em dashes.

## GREEN 7 — brochure site under the revised flow (clipfan): PASS

The RED 6 directives, re-run end to end (2026-06-11). Everything RED 6
rejected is fixed in the artifact, mechanically confirmed: **0 em dashes**
(was 18), **0 contrastive negation**, the problem in its own unresolved
`#problem` section, a scrolling GitHub Pages-ready `docs/index.html`
(19.7 KB, zero JS, sentinel + per-section citations), publication-writer
voice throughout ("Your Mac and Linux machines share one clipboard.").
**The tightened gate fired on its first test** — four questions (voice,
cast, section plan, and an unprompted-but-correct fourth: how far the
live demo may go on the human's real fleet) despite the pre-authorized
scope. The demo output is real (live daemon round-trip; clipboard saved
and restored). Two adversarial passes (markdown, then render) caught an
absolute overclaim, citation gaps, missing Owns globs, and a hero
headline that silently dropped "Mac and Linux" (inheritance violation) —
all fixed before the stamp (3 honest external-truth deferrals). One run
mechanic: the worker ended a turn mid-plan once and needed a "continue"
nudge — harness behavior, not flow text.

## Operational lessons (run mechanics, not skill defects)

- Never `tmux resize-window` while a worker's TUI modal is open — it
  wedged the renderer/input and cost a kill-and---resume recovery (the
  `--resume <session-id>` path restored full context cleanly).
- Dictionary structural lesson from the eval: a lowercase project name
  with a legitimately-capitalized code module (`clipfan` / `Clipfan`)
  belongs in Terms, not Names — docmaint's Names case-variant check has
  no module exemption (756 false positives until restructured). Echoes
  the v1 eval's Terms-vs-Names casing lesson; candidate dictionary.md
  guidance for a future revision (Iron Law applies).

## Known-noise note

Workers log "PreToolUse hook error — hookSpecificOutput missing
hookEventName" on every tool call: the claude-session-driver approval
hook's JSON shape is stale against current Claude Code hook validation.
Non-blocking (tools execute). Upstream fix belongs to
claude-session-driver, not this plugin.
