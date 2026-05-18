# Packages

Jamal Arcana is the umbrella docs repository. Package source code should live elsewhere.

## Repositories

| Repository | Role |
| --- | --- |
| `jamal-arcana` | Umbrella docs, ecosystem identity, lore, integration recipes |
| `wisp` | Generic floating terminal command runner |
| `waystone` | Path registry, fuzzy picker, clipboard/open workflows |
| `homebrew-jamal-arcana` | Homebrew formulae for public installation |

## Package independence rules

Each package should:

- be installable without cloning `jamal-arcana`
- have its own README and license
- have its own tests and CI
- expose `--help`
- avoid hardcoded personal paths
- link to Jamal Arcana for ecosystem docs

Each package should not:

- require another Jamal Arcana tool unless that dependency is explicit
- depend on dotfiles layout
- depend on private machine configuration

## Current extraction order

1. `wisp`
2. `waystone`
3. Homebrew tap
4. Documentation pages on the personal website
5. Later: decide whether MindWeaver, Djinn, and Ideomancer join the umbrella formally
