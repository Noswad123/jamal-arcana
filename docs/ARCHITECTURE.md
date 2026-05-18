# Architecture

Jamal Arcana is a tool ecosystem, not a framework. The main architectural rule is that each utility should remain independently useful and independently packaged.

## Package boundaries

Package source code should live in separate repositories. This repository documents the boundaries and integration patterns.

### `wisp`

`wisp` is a generic floating command runner.

It should know how to float commands. It should **not** know about specific tools like `waystone`, `mind-weaver`, or `djinn`.

Examples:

```bash
wisp nvim README.md
wisp yazi ~/Downloads
wisp waystone nvim
```

### `waystone`

`waystone` is a path registry and fuzzy picker.

It should know how to save paths, pick paths, copy paths, and open paths with a command. It should **not** require `wisp`.

Examples:

```bash
waystone add ~/Projects/app app
waystone
waystone nvim
waystone open less
```

### Composition

Integration should happen through shell composition:

```bash
wisp waystone nvim
```

This keeps both tools simple:

- `wisp` floats the command it receives.
- `waystone nvim` resolves to `waystone open nvim`.

## State and config

Tools should prefer XDG paths:

```text
${XDG_STATE_HOME:-~/.local/state}/waystone/paths.tsv
${XDG_CONFIG_HOME:-~/.config}/waystone/config
```

Avoid hardcoded dotfile paths in packages.

## Release strategy

Each package should graduate independently:

1. Start in its own repository.
2. Add source install instructions.
3. Add shell completions.
4. Add GitHub releases with tarballs.
5. Add Homebrew formulae.

Jamal Arcana remains the shared docs, design language, and discovery surface.
