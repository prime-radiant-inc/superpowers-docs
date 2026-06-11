Done, Jesse. The brochure is written, verified, stamped, and rendered — all four files left uncommitted on `docs/brochure` for your review.

**What's in the tree:**

| File | State | What it is |
|---|---|---|
| `docs/BROCHURE.md` | new | The governed positioning doc: what-it-is sentence, problem beat, six cashed capability bullets, a real CLI demo, the owner's trust brief, fit, seven limitations tagged by bearer, three doors. Stamped `2026-06-11 · 9b9970e · 3 deferred`. |
| `docs/index.html` | new | The brochure site, rendered from BROCHURE.md: single scrolling page, 19.7 KB, inline CSS, zero JS, zero external requests, sentinel carrying the stamp SHA, citation line on every section. |
| `README.md` | modified | Old intro paragraph replaced by BROCHURE.md's one-sentence verbatim plus a pointer. Everything the old paragraph said survives elsewhere in the README, except "per-SSH session state," which now lives only in ARCHITECTURE § Goals. |
| `docs/INDEX.md` | modified | New `adopter`/`evergreen` row for BROCHURE.md; decided-gaps comment now records the reopening — dated 2026-06-11, attributed to you, with the stale "internal proprietary tool" rationale quoted in full and the other 06-10 decisions untouched. |

**The demo is real.** The daemon on this Mac is live, so the console block in "Using it" was actually executed: copy, paste round-trip, and the health check. I saved your clipboard first and restored it byte-for-byte after (cost: two transient entries in your fleet's history).

**Verification was two independent adversarial passes.** The first (on the markdown) caught a real overclaim — I'd stated the loopback bind absolutely when SECURITY/ARCHITECTURE both qualify it ("out of the box" now), plus two citation gaps, a thesis echo, and two Owns globs the row was missing (`internal/cli/**`, `dist/tmux.conf.snippet`). The second (on the render) caught my hero headline silently dropping "Mac and Linux" — an inheritance violation — and an owner-band citation line that had shed half its cashing sections. All findings fixed; both verifiers landed on "ship-ready after fixes." The 3 deferred claims in the stamp are the ones with ground truth outside the repo: the demo provenance, the GitHub releases page, and repo visibility.

One thing to know for review: the page and README link to `blob/main/...` URLs, so those links 404 on live GitHub until this branch merges to main. And if you enable Pages ("deploy from branch, /docs folder"), the site serves at the project root as-is.