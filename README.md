# Jamal Arcana

Beautiful local-first tools for navigating your machine, summoning workflows, and shaping knowledge.

Jamal Arcana is the umbrella and documentation home for the fantasy-inspired tool ecosystem that grew out of my personal setup.

It is not the source repository for each package. Each tool lives in its own repository with its own installation path, release cadence, and issue tracker. Jamal Arcana explains the shared design language, package boundaries, lore, and integration recipes.

## Tools

| Tool | Purpose | Repo |
| --- | --- | --- |
| `wisp` | Open a command in a floating terminal window | [`Noswad123/wisp`](https://github.com/Noswad123/wisp) |
| `waystone` | Save, fuzzy-pick, copy, and open frequently used paths | [`Noswad123/waystone`](https://github.com/Noswad123/waystone) |

Planned/adjacent tools that may stay in their own repositories:

| Tool | Purpose |
| --- | --- |
| MindWeaver | Notes, todos, cheatsheets, and local knowledge |
| Djinn | Shell alias/function discovery |
| Ideomancer | Project manifests and validation workflows |

## Design principles

1. **Modular by default** — every tool should work on its own.
2. **Composable by convention** — tools can integrate through normal shell commands.
3. **No dotfiles dependency** — personal config is an integration layer, not a runtime requirement.
4. **XDG-friendly state** — runtime state lives under `XDG_STATE_HOME` or `~/.local/state`.
5. **Small sharp tools** — avoid turning the ecosystem into one monolith.

## License

Jamal Arcana docs and package repositories use the MIT License unless a future package explicitly says otherwise.

## Documentation

Start here:

- [`docs/VISION.md`](docs/VISION.md) — purpose, philosophy, and tool criteria
- [`docs/TOOLS.md`](docs/TOOLS.md) — catalog of current and future tools
- [`docs/INSTALL.md`](docs/INSTALL.md) — Homebrew and source installation paths
- [`docs/COMPOSITION.md`](docs/COMPOSITION.md) — how tools work together through the shell
- [`docs/LORE.md`](docs/LORE.md) — naming, worldbuilding, and tone
- [`docs/ARCHITECTURE.md`](docs/ARCHITECTURE.md) — ecosystem rules and package boundaries
- [`docs/RELEASES.md`](docs/RELEASES.md) — release status and roadmap
- [`docs/WEBSITE.md`](docs/WEBSITE.md) — website integration plan

## Composition example

```bash
waystone nvim
wisp waystone nvim
```

This works because `wisp` is generic and `waystone nvim` resolves to `waystone open nvim`.

