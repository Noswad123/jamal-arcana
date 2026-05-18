# waystone

`waystone` is a path registry and fuzzy picker.

## Contract

```bash
waystone add <path> [label]
waystone [opener...]
waystone open [opener...]
waystone pick
waystone list
```

`waystone nvim` should resolve to `waystone open nvim`.

## Composition with wisp

```bash
wisp waystone nvim
```

`wisp` floats the command. `waystone` resolves and opens the selected path.

## Package repo

Planned standalone repository: `waystone`.
