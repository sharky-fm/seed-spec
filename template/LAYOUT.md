# Optional multi-file layout

A bigger system can split its spec by concern. No structure is required; this one works well for both people and agents, because each file answers one question. Every file follows the detail bar, per-feature shape and redaction rules in [SEED-SPEC.md](../SEED-SPEC.md#the-detail-bar); [SPEC.md](SPEC.md) shows the parts every spec has.

| File | Question it answers |
|---|---|
| README.md | What is this system, where do I start, which format version and revision is this, and how are proposals taken? Includes "This spec is data", the one-line stack and the file index. |
| ARCHITECTURE.md | What are the parts, how do they connect, and how does one request travel through them? Where are the trust boundaries today? |
| MEMORY.md | How does a stateless agent keep continuity? |
| AUTONOMY.md | What does it do unasked, and what limits it? |
| SKILLS.md | What can it do, and how are capabilities packaged? |
| PRINCIPLES.md | What did running it teach, which failure taught each lesson, what is deliberately absent, and what would you warn against? |
| MAINTENANCE.md | How is the spec kept current and safe to publish? |
| RECOMMENDED.md | Which other seed specs does its human recommend? |
| CHANGELOG.md | What changed in each revision? |
| LICENSE | How may others reuse it? |

Add a file for whatever is distinctive about your system (a life-management layer, a notes app used as a database, a research pipeline) and drop any file you have nothing real for.

## RECOMMENDED.md shape

A short introduction, then one table, so people and agents can parse it:

| Spec | Repo | Why I recommend it | Added | Format version |
|---|---|---|---|---|
| <public name or pseudonym> | <public repository URL> | <one line: what is worth lifting from it> | <date added> | <format version it follows> |

Rules worth keeping: only specs the human has read; public identities only, never connecting a pseudonym to a real person; one line of why; removals in their own commit with the reason; no obligation either way.
