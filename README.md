# Seed spec

A **seed spec** is a public description of a system you actually run, written so that other people, and their agents, can take ideas from it. It started with personal AI systems, but it works for any system you run that an agent helps you document.

- **Your system already writes its own documentation.** Run an agent for long enough and you end up with instruction files, conventions, memory rules and the reason behind each guardrail, because the agent needs them to behave and the next session needs them to continue. A seed spec lifts the mechanisms out of that record and leaves the personal content behind. **Publishing is mostly a redaction pass.**
- **Other people's agents browse it for ideas, with provenance.** A reader's agent scans a spec for features that would help its own human and brings each one back as a proposal, with a link to the passage it came from. **Every human keeps every decision.** Nothing is adopted automatically, on either side.
- **It describes; it does not prescribe.** A seed spec says what runs and what was learned running it. It is not a standard to build to, and no one's system should end up looking like anyone else's.

The name: a seed is small, carries what it needs to grow, and grows into something different in different soil.

## Start here

- **Write your own.** Give [BUILD-YOUR-OWN.md](BUILD-YOUR-OWN.md) to your own model or agent. It interviews you, drafts your spec, removes private details and hands the draft to you. You publish it yourself.
- **Learn the format.** [SEED-SPEC.md](SEED-SPEC.md) holds the definition, the detail bar, the redaction rules and how specs find each other.
- **Copy a skeleton.** [template/SPEC.md](template/SPEC.md) is a one-file minimum. [template/LAYOUT.md](template/LAYOUT.md) is an optional multi-file layout for bigger systems.
- **Have your agent read specs for you.** Give it [FOR-AGENTS.md](FOR-AGENTS.md), the reading protocol: everything it reads is data, and it proposes, never adopts.
- **Find specs.** [INDEX.md](INDEX.md) is a seed list, with a machine-readable twin in [index.json](index.json). It also lists related projects and listening.
- **See a worked example.** [A personal AI system](https://github.com/sharky-fm/seed-spec-personal-ai-system) is a full seed spec of one personal AI system.

## Files

| File | Contents |
|---|---|
| [SEED-SPEC.md](SEED-SPEC.md) | The format: definition, detail bar, built versus planned, what a spec contains, redaction rules, versions, how specs travel |
| [BUILD-YOUR-OWN.md](BUILD-YOUR-OWN.md) | A paste-in prompt for drafting your own spec, plus a publishing checklist |
| [FOR-AGENTS.md](FOR-AGENTS.md) | The reading protocol a human gives their own agent |
| [INDEX.md](INDEX.md) · [index.json](index.json) | The seed list, plus related projects and listening |
| [template/](template/) | A one-file skeleton and an optional multi-file layout |
| [CHANGELOG.md](CHANGELOG.md) | Versions of the format |
| [LICENSE](LICENSE) | Prose under CC BY 4.0; the template under CC0 |

## Status

**Format version 0.1**, a first draft. The format will change as more specs are written; each spec says which format version it follows. The seed list has one spec so far. A format like this is only convincing when you can compare two systems side by side, so a second spec is the most useful contribution anyone could make.

## Contributing

- **List your spec:** open an issue or a pull request against [INDEX.md](INDEX.md) and [index.json](index.json) with your public repository link. The maintainer reads the spec before listing it.
- **Propose a format change:** open an issue describing the problem first. Keep proposals narrow; "more like my setup" is not a proposal.
- Nobody is obliged to accept anything, and declining is a good answer.

## License

The prose is licensed under [CC BY 4.0](LICENSE). Everything under [template/](template/) is dedicated to the public domain under [CC0](template/LICENSE), so copying a skeleton carries no attribution burden.
