# Composition

Jamal Arcana tools should compose through normal shell behavior instead of hardcoded knowledge of each other.

## Core rule

```text
Tools do not need to know each other. The shell introduces them.
```

## Example: `wisp` and `waystone`

`waystone` can pick a saved path and open it with an opener:

```bash
waystone nvim
```

That resolves to:

```bash
waystone open nvim
```

`wisp` can float any command:

```bash
wisp nvim README.md
```

Together:

```bash
wisp waystone nvim
```

This works because:

- `wisp` floats the command it receives.
- `waystone nvim` picks a saved path and opens it with Neovim.

Neither tool needs special-case code for the other.

## Good composition

```bash
wisp waystone nvim
wisp yazi ~/Downloads
waystone less
waystone open bat
```

## Avoid

- making `wisp` aware of `waystone`
- making `waystone` require `wisp`
- hiding dependencies in dotfiles-only wrappers

Wrappers can exist for personal workflows, but package behavior should remain simple and explicit.
