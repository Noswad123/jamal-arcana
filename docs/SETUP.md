# Setup Plan

This is the path from personal dotfiles utility to shareable package while keeping Jamal Arcana as the umbrella docs repository.

## 1. Keep the public packages clean

Each package should avoid:

- `~/.dotfiles` references
- personal project paths
- private config assumptions
- hardcoded usernames

Each package should include:

- `bin/<tool>`
- `README.md`
- clear dependencies
- `--help`
- basic validation instructions

## 2. Extract each package into its own repository

Recommended repositories:

```text
jamal-arcana         # umbrella docs and ecosystem map
wisp                 # generic floating command runner
waystone             # path registry and fuzzy picker
homebrew-jamal-arcana
```

Initial extraction steps per package:

1. Create a new repo under `~/Projects/<tool>`.
2. Copy only the package source, README, license, and tests.
3. Remove dotfiles assumptions.
4. Add an install script local to that package.
5. Link back to Jamal Arcana for ecosystem documentation.

Override with:

```bash
## 3. Test package installs

```bash
cd ~/Projects/wisp
./install.sh
wisp --help

cd ~/Projects/waystone
./install.sh
waystone --help
```

For `waystone`:

```bash
waystone add ~/Projects/jamal-arcana jamal-arcana
waystone list
waystone nvim
```

For floating workflows:

```bash
wisp nvim README.md
wisp waystone nvim
```

## 4. Document publicly

Use Jamal Arcana for ecosystem-level docs and the personal website for polished public presentation.

Suggested flow:

1. Package READMEs explain installation and local usage.
2. Jamal Arcana explains how tools fit together.
3. Personal website showcases lore, demos, screenshots, and project cards.

## 5. Homebrew later

The Homebrew tap should expose separate formulae:

```bash
brew install jamal-arcana/tap/wisp
brew install jamal-arcana/tap/waystone
```

Optional bundle formula:

```bash
brew install jamal-arcana/tap/arcana
```
