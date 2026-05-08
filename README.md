# protocols

Engineering protocols for Claude Code `/plan` mode workflows.

## What this is

A small, opinionated set of non-negotiable protocols I follow when planning and implementing software with Claude Code. They cover ADRs, specs, TDD, feature branches, changelogs, releases, dependency hygiene, README accuracy, DRY, agent usage, and frontend security.

→ [`protocols.md`](protocols.md)

## How to use it

Reference the protocols file from your prompt when entering plan mode:

```
Follow /plan mode, do xyz, follow @protocols.md
```

Claude Code resolves `@protocols.md` from your project's working directory. Either:

1. **Vendor the file into each project** — copy `protocols.md` to your project root (or `docs/`) and reference it directly. Pin to a specific commit if you want stability.
2. **Submodule or subtree** — add this repo as a git submodule under e.g. `protocols/` and reference `@protocols/protocols.md`.
3. **Symlink** — for local-only workflows, symlink `protocols.md` into each project from a single working copy.

I generally vendor — copy and pin — because the protocols are short and stable, and a vendored copy survives offline sessions and submodule confusion.

## What's in the file

The 12 always-on protocols and 1 optional Svelte-only protocol:

| # | Protocol | Always on? |
|---|---|---|
| 1 | Architecture Decision Records | yes |
| 2 | Specifications | yes |
| 3 | Test-Driven Development | yes |
| 4 | Feature Branches | yes |
| 5 | Changelog | yes |
| 6 | Releases | yes |
| 7 | Context7 MCP for Language Research | yes |
| 8 | Production-Ready Code Only | yes |
| 9 | Claude Agent Teams | yes |
| 10 | Latest Stable Dependencies | yes |
| 11 | README Accuracy | yes |
| 12 | Don't Repeat Yourself | yes |
| 13 | Frontend Security — `{@html}` Protocol | **only for Svelte projects** |

## Author

Chris Barlow — [github.com/cgbarlow](https://github.com/cgbarlow)
