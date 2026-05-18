# Releases

## MVP

- [x] Confirm public names: `wisp`, `waystone`, `Jamal Arcana`.
- [x] Decide license: MIT.
- [x] Create standalone `wisp` repository.
- [x] Create standalone `waystone` repository.
- [x] Add package-level install scripts.
- [x] Add package-level smoke tests.
- [x] Add package-level CI with `bash -n` and ShellCheck.
- [x] Add shell completions in each package repo.

## Current package releases

| Tool | Version | Release |
| --- | --- | --- |
| `wisp` | `v0.1.0` | <https://github.com/Noswad123/wisp/releases/tag/v0.1.0> |
| `waystone` | `v0.1.0` | <https://github.com/Noswad123/waystone/releases/tag/v0.1.0> |

## Homebrew

- [x] Create tap repository scaffold.
- [x] Add `wisp` formula.
- [x] Add `waystone` formula.
- [x] Push tap repository to GitHub.
- [ ] Smoke-test install from the public tap.

Tap repository:

```text
homebrew-jamal-arcana
  Formula/wisp.rb
  Formula/waystone.rb
```

Formulae should install package bins independently.

## Repository shape

```text
jamal-arcana        # umbrella docs and ecosystem overview
wisp                # standalone package
waystone            # standalone package
homebrew-jamal-arcana
```

Avoid putting package source in `jamal-arcana` except for tiny examples or documentation snippets.
