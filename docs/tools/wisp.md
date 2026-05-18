# wisp

`wisp` is a generic floating command runner.

## Contract

```bash
wisp <command> [args...]
```

`wisp` should float the command it receives. It should not know about `waystone` or any other specific tool.

## Examples

```bash
wisp nvim README.md
wisp yazi ~/Downloads
wisp waystone nvim
```

## Package repo

Planned standalone repository: `wisp`.
