# Packages

Jamal Arcana is the umbrella docs repository. Package source code should live elsewhere.

## Repositories

| Repository | Role |
| --- | --- |
| [`jamal-arcana`](https://github.com/Noswad123/jamal-arcana) | Umbrella docs, ecosystem identity, lore, integration recipes |
| [`wisp`](https://github.com/Noswad123/wisp) | Generic floating terminal command runner |
| [`waystone`](https://github.com/Noswad123/waystone) | Path registry, fuzzy picker, clipboard/open workflows |
| [`homebrew-jamal-arcana`](https://github.com/Noswad123/homebrew-jamal-arcana) | Homebrew formulae for public installation |

## Package independence rules

Each package should:

- be installable without cloning `jamal-arcana`
- have its own README and license
- use the MIT license unless there is a specific reason to diverge
- have its own tests and CI
- expose `--help`
- avoid hardcoded personal paths
- link to Jamal Arcana for ecosystem docs

Each package should not:

- require another Jamal Arcana tool unless that dependency is explicit
- depend on dotfiles layout
- depend on private machine configuration

## Extraction status

- [x] Extract `wisp`.
- [x] Extract `waystone`.
- [x] Create Homebrew tap.
- [ ] Build public website pages.
- [ ] Decide whether MindWeaver, Djinn, and Ideomancer join the umbrella formally.
