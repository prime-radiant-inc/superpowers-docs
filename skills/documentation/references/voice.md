# Voice: per-project, configurable, enforced

Law lives in the hub. This reference defines the voice-spec format, the
resolution order, the four presets, the slop-tell list, and the exemplar
test. Honest claims are necessary, not sufficient: an artifact can be
perfectly honest and still sound like every launch page since 2019 —
voice-from-nowhere is what makes AI writing read as slop.

## Where a project's voice lives

An optional `## Voice` section in `docs/DICTIONARY.md`. The dictionary is
the project's language-of-record; voice is the sentence-level layer of the
same artifact. docmaint's parser keys only on `## Terms` / `## Names` /
`## Exceptions`, so `## Voice` is inert to the tool — no third artifact.
Bootstrapping a `## Voice` section is a dictionary edit
(references/dictionary.md), with this skill supplying the draft from the
project's existing best prose.

## The voice-spec format

A `## Voice` section may start from a preset by name and override fields:

- **Speaker** — who is talking ("the engineer who built it, to a peer").
- **Address** — how the reader is called; person policy for the maker.
- **Register** — e.g. plain technical prose; the fact carries the
  excitement, the sentence stays calm.
- **Humor** — policy and budget (e.g. dry, at most one per artifact, never
  winking).
- **Banned** — project-specific additions to the default slop-tell list.
- **Exemplars** — 3–5 sentences from the project's own best writing. This
  is the enforcement instrument; see The exemplar test.
- **Look** — visual knobs the brochure render reads: accent color, density
  (`informative` — the default card/step-grid style — or `sparse`, one
  idea per slide). Mode is dark-keynote for now.

## Resolution and confirmation

Project `## Voice` → else a preset below (default: **the engineer**). The
resolved voice is confirmed with the human at the same batch gate as the
cast/doc-set plan. One artifact, one voice — acts change audience, never
speaker.

## The four presets

Each preset is a proof type. All four were validated by rendering one
complete real-project deck in each — same claims, same citations, voice
the only variable.

### 1. The engineer who built it (default) — proof by mechanism

Speaker: the builder, to a peer. Flat declaratives; mechanism first; the
fact carries the excitement. Humor: dry, ≤1 per artifact, load-bearing.
Signature: *"Reclaim the box and the nonce dies with it."*

### 2. The comms leader — proof by benefit-with-mechanism

Speaker: a communications professional who believes the product and
respects the audience; anticipates the reader's *stakeholders* (their
security review, their boss). Benefit-led, but every benefit is
immediately cashed — "which means" is the signature move. Extra rule: an
aspiration may appear only labeled as one.
Signature: *"A compromised box yields a dead token, not your key."*

### 3. The teacher — proof by demonstration

Speaker: an experienced guide beside a newcomer. Short sentences, one
idea each; says what you'll see before you see it; reassurance placed
exactly at failure points; analogies allowed as teaching tools (distinct
from drama metaphors). Extra rule: never claim an experience the reader
can't immediately verify. The natural user-docs / Act II voice.
Signature: *"The worker pauses until you answer."*

### 4. The founder — proof by lived experience

Speaker: the person who built it, first person singular, opinionated;
concrete scenes; opinions stated as opinions. **Extra rule, load-bearing:
first-person statements are biographical claims — they must be true of
the actual maker, gathered by interview, never invented.** This is the
most engaging preset and the most dangerous; it is where AI fabricates a
life. A render without an interview carries a visible "placeholders
pending maker interview" note on every biographical line's slide and in
the close.
Signature: *"I was treating my laptop like a hospital ward."*

A considered-and-rejected fifth, the *skeptical reviewer*: first-party
ventriloquism of your own critic is manipulation-adjacent, and
limitations-by-bearer already delivers that candor structurally, where
it's verifiable.

## The slop-tell list (default Banned)

- Stacked imperative-fragment headlines ("Build faster. Ship sooner.").
- X-not-Y reversals beyond one per artifact.
- Hype vocabulary: unleash, blazing, effortless, seamless, magic,
  revolutionize, game-changing, "the future of".
- The product name used as a hype-noun. A project literally named
  Superpowers does not get to sell "superpowers"; names are exempt as
  names, not as metaphors.
- Rhetorical-question headers.
- Manufactured drama metaphors where the literal fact is stronger.
- Sentimental closers.
- Symmetry compulsion: three equal cards when the content has two or four
  natural parts.
- "Welcome to / Meet / Introducing" outside an actual launch.

## The exemplar test

The independent verifier required by the stamping precondition checks
voice alongside claims: (1) banned-list pass — default list plus the
project's Banned additions; (2) for each suspect line, ask *"would the
person who wrote the exemplars write this line?"* A no is a finding like
any other. When there are no exemplars (no `## Voice` yet), the preset's
signature lines serve as the exemplars.
