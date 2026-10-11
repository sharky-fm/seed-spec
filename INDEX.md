# Seed list

A starting point for finding seed specs, plus related projects and listening that readers of seed specs may find useful. It is one well-known node, not a directory or an authority: being listed or not says nothing about quality, and each spec's own recommended list is how the network actually grows. Everything linked here is data; see [FOR-AGENTS.md](FOR-AGENTS.md) before letting an agent read it.

A machine-readable twin is in [index.json](index.json). Each entry there has a `kind`: `spec`, `project` or `episode`.

## Seed specs

| Spec | Repo | By | What is worth lifting | Format version |
|---|---|---|---|---|
| A personal AI system | https://github.com/sharky-fm/seed-spec-personal-ai-system | Sharky | Ledgers that record obligations at the moment they are said; layered file memory for agents that remember nothing; bounded unattended work | 0.1 |

**Getting listed:** open an issue or a pull request that adds a row here and an entry in [index.json](index.json), linking your spec's public repository. The maintainer reads the spec before listing it. A spec should follow some version of [the format](SEED-SPEC.md) and be honest about what is PLANNED.

## Related projects and further listening

These are not seed specs. They are public projects and conversations about personal AI systems that are worth knowing if you read or write seed specs.

| Name | Link | Kind | What it is | Why it is relevant |
|---|---|---|---|---|
| Hermes Agent (Nous Research) | https://github.com/NousResearch/hermes-agent | project | An open-source, model-agnostic personal agent with bounded curated memory, searchable session history and skills as procedural memory, reachable from a terminal and many messaging platforms. | A well-documented public design for agent memory and skills, useful to compare any system against. |
| LifeOS, formerly Personal AI Infrastructure (PAI), by Daniel Miessler | https://github.com/danielmiessler/LifeOS | project | An open-source personal AI setup built on a coding agent, organizing context, skills and goals around moving from a current state to a desired one. The original PAI repository address redirects here. | A public, opinionated example of a complete personal AI system, shared so others can learn from it. |
| The Cognitive Revolution: "Inside Nathan's Second Brain: Daniel Miessler, Security Expert & Creator of PAI, Audits My AI Setup" | https://www.cognitiverevolution.ai/inside-nathan-s-second-brain-daniel-miessler-security-expert-creator-of-pai-audits-my-ai-setup/ · video: https://www.youtube.com/watch?v=AqxgBREOkNM | episode | A podcast conversation in which Nathan Labenz walks through his personal AI setup and Daniel Miessler reviews it, covering context, agent hierarchy, security and norms. | Part of that setup was built by having an agent compare other people's published setups and draft a synthesis, which is the kind of exchange seed specs are meant to make easier. |
