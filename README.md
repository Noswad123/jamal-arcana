# Jamal Arcana

Beautiful local-first tools for navigating your machine, summoning workflows, and shaping knowledge.

Jamal Arcana is the umbrella and documentation home for the fantasy-inspired tool ecosystem that grew out of my personal setup. It is not my dotfiles repo, and it is not the source repository for each package.

Each tool should live in its own repository, with its own installation path, release cadence, and issue tracker. Jamal Arcana explains the shared design language, package boundaries, lore, and integration recipes.

## Tools

| Tool | Purpose | Package repo |
| --- | --- | --- |
| `wisp` | Open a command in a floating terminal window | `jamal-arcana/wisp` |
| `waystone` | Save, fuzzy-pick, copy, and open frequently used paths | `jamal-arcana/waystone` |

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

## Documentation

Start here:

- `docs/ARCHITECTURE.md` — ecosystem rules and package boundaries
- `docs/PACKAGES.md` — repository plan and package ownership
- `docs/WEBSITE.md` — how the personal website can host public docs/lore
- `docs/tools/wisp.md` — `wisp` concept and package contract
- `docs/tools/waystone.md` — `waystone` concept and package contract

## Composition example

```bash
waystone nvim
wisp waystone nvim
```

This works because `wisp` is generic and `waystone nvim` resolves to `waystone open nvim`.

## Repo shape

```text
docs/
  SETUP.md
  ARCHITECTURE.md
  PACKAGES.md
  WEBSITE.md
  RELEASE.md
  tools/
    wisp.md
    waystone.md
```
