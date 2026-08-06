# superpowers-docs

> A documentation department in a box: a Claude Code plugin that plans, writes, and maintains a project's docs with verified claims.

**Family:** superpowers · **Type:** tool · **Lifecycle:** experimental · **Owner:** obra

## What it does
A single `documentation` skill acting as hub and dispatch: it studies a project and its readers, agrees a doc portfolio with the user, then routes to flow references for contributor docs, user docs, marketing/brochure sites, single-doc work, incremental updates, and audits. Craft references (voice, Strunk, brochure design, dictionary) set the writing law; a Python `docmaint` script with a header-aware index parser handles doc maintenance mechanics. Developed RED/GREEN against clipfan baselines, with the evidence record kept in `docs/superpowers/evals/`.

## How it fits
- Depends on: —
- Used by: — (installable as a Claude Code plugin, v0.1.0)
- External: none at runtime

## Runtime & data
- Runs: local Claude Code plugin (skill + stdlib Python script)
- Data in: the target project's code, docs, and reader context
- Data out: doc portfolios and written/maintained documentation in the target project

<!-- Maintained by the maintaining-project-map skill. Do not hand-edit; regenerated. -->
