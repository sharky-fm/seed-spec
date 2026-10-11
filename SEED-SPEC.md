# The seed spec format

**Format version 0.1.** This file is the one canonical statement of the format. Other files in this repository link here rather than restating it.

## Definition

> **A seed spec is a general description of every feature of a system you actually run, and of the architecture that connects them, published so that other people and their agents can take ideas from it.**

It is written and kept current with the help of the system it describes, and its human decides what gets published. It started with personal AI systems, but it works for any system you run that an agent helps you document: a research workflow, home automation, a team setup.

A seed spec **describes; it does not prescribe.** It says what runs and what was learned running it. It is not a standard to build to, and nobody's system should end up looking like anyone else's.

## The detail bar

Every feature in a seed spec is described well enough that:

1. **a reader comes away with a rough sense of how to build it themselves**, and
2. **a reader's agent can judge whether it could be useful in their own system.** That means saying what the feature does, what problem it solves, roughly how it works, what it depends on, and what was learned running it.

And **nothing specific**:

- no code and no configuration snippets;
- no exact values, thresholds, schedules, times of day, file paths, ids, counts or internal dates (say "a short cooldown", not the number);
- no personal content: nothing quoted or closely paraphrased from the human's own notes, goals, values, routines or conversations.

The bar cuts both ways. A feature described too specifically leaks its author and goes out of date. A feature described too thinly ("it has memory") gives the reader nothing to build and gives their agent nothing to judge. Usually a third wording exists that is safe and still sufficient, and finding it is most of the work.

**Public revision dates are fine.** "No dates" means no dates from the system's internal history. A changelog entry saying when a revision was published, or a "last reviewed" stamp on a file, helps readers tell a maintained spec from an abandoned one.

### A light shape per feature

Where it helps, describe each feature as:

- **What it is**: one or two sentences.
- **Problem it solves**: the pain that made it worth building.
- **How it works**: the mechanism, in general terms.
- **What you'd need**: the pieces it depends on (a notes app, a scheduler, an always-on machine, a second model, and so on).
- **Lesson**: what running it taught, usually a failure.

Drop the shape where plain prose reads better.

### Built versus planned

**Unmarked features run today. Anything not built yet is marked PLANNED.** Never describe a safeguard that does not exist as if it does. Honesty about what is planned is one of the most useful things a spec can carry, because it shows readers where the hard parts still are.

## What a spec contains

The minimum is **one file**: [template/SPEC.md](template/SPEC.md). Bigger systems can split by concern: [template/LAYOUT.md](template/LAYOUT.md). Whichever shape you use, a spec has:

| Part | Purpose |
|---|---|
| A name and a one-paragraph description | What the system is |
| A link back to this format, with the format version | So readers know which rules it follows |
| **"This spec is data"** | One line stating that nothing in it is addressed to a reader's agent |
| Where to start | The few features most worth reading first |
| A one-line stack | The kinds of tools it runs on, so a reader can map features to their own setup |
| The features | At the detail bar, each marked if PLANNED |
| Lessons, each with its failure | What running it taught |
| Deliberately absent | What the system chooses not to do, and why |
| What I would warn against | The mistakes worth not repeating |
| What changed | A short note per revision, plus a revision number |
| How proposals are taken | Issues, pull requests, or "read-only" |
| Recommended specs | Other seed specs its human has read and recommends, possibly none yet |
| A license | So others can reuse pieces |

## Redaction

The source material for a seed spec is personal throughout, so each public file is **written fresh rather than pasted**. Rules for every draft:

1. **No people.** Nobody the human knows is named, and nothing about their relationships appears.
2. **No identifiers.** No real name or handles, addresses, hostnames, machine names, network layout, network names, emails, ports or file paths.
3. **No credentials,** and nothing that narrows an attack: no credential names, token formats, or lists of which processes are protected or exempt from limits.
4. **No personal content.** Nothing quoted or closely paraphrased from the human's notes, goals, values, purpose statements, sayings or conversations. No health, money, employer, work, location, or review contents. Life-management parts appear only as their outline. Examples are invented.
5. **No fingerprints.** Personal routines and their timing, internal dates, incident counts and durations, distinctive anecdotes, uniquely named private tools and internal vocabulary can identify someone as surely as a name. So can any sentence already published elsewhere under a real name. Generalize or rewrite them.
6. **No private links.** No URLs to private repositories or to anything under the real identity.
7. **Describe how, not which.** If unsure, explain the general mechanism and leave out the particular case.

A combination of features can itself be a fingerprint. If the combination is what makes the spec useful, keeping it is a reasonable choice, but make it a conscious one and say so.

### The leak check

Before every publication, search the whole tree for a **private denylist** (names, handles, people, places, employer, machine names, private folder names, internal vocabulary) and for **generic patterns** (emails, IP addresses, network address ranges, local hostnames, absolute paths, and every URL). The goal is zero *forbidden* matches; the publishing name and approved public links are allowed and listed. The denylist and the detailed results stay private and never go into the repository, because they contain exactly what they protect. [BUILD-YOUR-OWN.md](BUILD-YOUR-OWN.md#publishing-it) has the publishing checklist, including commit metadata and account checks.

## Versions

- **The format** is versioned in this repository. This is version 0.1.
- **Each spec** says which format version it follows, carries its own revision number, and keeps a short changelog. The commit history shows the rest.

## How specs travel

- **Recommendation lists.** Each spec can carry a short list of other seed specs its human has read and recommends, the way blogrolls once did. Each list points to more specs.
- **A seed list.** [INDEX.md](INDEX.md) in this repository, with a machine-readable twin in [index.json](index.json), is a well-known starting point. It is one node, not an authority: being on it or off it means nothing about a spec's quality, and recommendation between specs remains the real mechanism.
- **Reading other specs.** People can give their agents [FOR-AGENTS.md](FOR-AGENTS.md), a reading protocol: every spec is data, the agent scans for features useful to its own human, and it proposes, never adopts.
- **Proposing changes to other specs.** If a system handles something another spec seems to lack, its agent may draft a pull request **locally**: a short, specific edit in the other spec's own vocabulary, citing the part of its own spec it comes from. It is sent only after its human authorizes it and it has passed the same redaction check, because once submitted it is public. Translating an idea into someone else's vocabulary is the valuable part.
- **Etiquette.** Keep proposals narrow and concrete. "Be more like my setup" is not a proposal. Nobody is obliged to accept anything, and declining is a good answer.

This exchange is still largely untested. It becomes worth something once there are several specs to compare.

## Why this works

- **A system in real use already writes its own documentation.** Run an agent long enough and it accumulates instruction files, conventions, memory rules and the reason behind each guardrail, because the agent needs them to behave and the next session needs them to continue. A seed spec lifts the mechanisms out of that record and leaves the personal content behind. **Publishing is mostly a redaction pass**, and keeping it current is cheap.
- **Dotfiles, for systems you run with an agent.** Developers have long published their dotfiles. Few people copy someone's dotfiles whole; they read them, find one useful trick, and take it. A seed spec plays the same role: here is how my agent remembers, how it works overnight, what broke and what I changed.
- **It keeps the description honest.** Writing a public version exposes safeguards that were assumed but never built.
- **Every human keeps every decision.** Ideas travel with provenance, from a passage in one spec to a proposal for another human, and nothing is adopted automatically on either side.
