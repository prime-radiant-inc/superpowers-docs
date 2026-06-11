Done, Jesse. The full audit is complete and everything is left **uncommitted on `eval/docs-plugin`** for your review. Here's the picture.

## What clipfan's docs now have

- **`docs/INDEX.md`** — the classification of record: 9 evergreen docs (Reader/Class/Owns globs), point-in-time rows for CHANGELOG/PLAN/`docs/superpowers/**`, the ABOUT.md foreign-owned exclusion, and your decided gaps (no CLAUDE.md, no brochure, no docs site, no standalone API ref) recorded so they don't get re-litigated.
- **`docs/DICTIONARY.md`** — 19 entries (clip vs history entry, clip-ID dedup vs echo suppression, menubar app vs menu bar, send vs push, etc.). `docmaint scan` is green across the repo. One structural lesson: `clipfan` had to live in Terms, not Names — docmaint's case-variant check has no exemption for the legitimate capitalized Swift module `Clipfan` and flagged 756 false positives until I restructured it.
- **Stamps** — all nine evergreen docs carry `last-reviewed: 2026-06-10 @ 5ed989c` with honest deferred counts (54 total — externals like macOS TCC behavior, GitHub secret-store state, and unconfirmable absence claims). `docmaint stale` now gives you a working maintenance loop.

## What verification found and fixed

~345 claims checked by 9 verification agents, then every applied edit re-checked by competing adversarial verifiers. Highlights of the ~40 fixes: ROADMAP rewritten as a post-1.0 living roadmap (five shipped items were still "Planned"); ARCHITECTURE's wrong default listen (`127.0.0.1:7853`), wrong `POST /v1/current` status, missing packages/routes, and the legacy-only signature documentation; TROUBLESHOOTING's wrong Settings pane, pre-loopback firewall advice, and a "flags older peers" feature that doesn't exist; README's pre-mesh topology/discovery story; the tmux emacs-binding overclaim in two docs; SECURITY's overstated recipient-binding and socket-permission claims; plus `chmod +x dist/install.sh` and the two point-in-time banners.

The adversarial passes earned their keep: they caught **my own fix** putting `auth_version=` in the wrong position in the HMAC canonical string (a client built from it couldn't authenticate), my safe-mode route list missing `/v1/peers`, and a README sentence promising self-healing the code only performs at app launch.

## Findings filed, not fixed (your call, each with a reader)

- **Coverage gaps:** `mesh-heal` (also absent from `clipfan help`'s usage text), `remove-host`, `local-fleet-reset`, and `storage-preflight` are operator-usable but undocumented; SECURITY never mentions the second credential class (sync SSH keys, the forced-command gateway, known_hosts pinning); TROUBLESHOOTING doesn't cover safe mode; README's config section omits `hostname` and the app-managed v2/SSH fields; `TMUX_TMPDIR`, `--no-restart`, `DEST` undocumented.
- **Duplication trims** (owners + replacement text in the corpus report): first-launch flow (README ⇄ building-from-source), tmux rationale, ROADMAP Done bullets restating ARCHITECTURE.
- **Code-side:** consider AAD-binding the envelope `recipient`; the tmux snippet's own header comment overclaims the emacs bindings (or bind y/Enter there); stale `apps/mac/build-app.sh` sibling; `UNIT_NAME` fossil in install.sh; stale `nohup` comment in DaemonClient.swift; CI fixture script gaps (`-F none`, process sweep, secret-byte scan, dead 17d3a refs).
- **Foreign-owned:** ABOUT.md still describes the removed peer-HTTP sync — fix routes through your maintaining-project-map skill.

`git diff` plus the two new files is the full review surface. Once you commit, the stamps' SHA cursor goes live and future sessions maintain this incrementally instead of re-auditing.