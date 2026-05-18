# Release Roadmap

## MVP

- [ ] Confirm public names: `wisp`, `waystone`, `Jamal Arcana`.
- [ ] Decide license.
- [ ] Create standalone `wisp` repository.
- [ ] Create standalone `waystone` repository.
- [ ] Add package-level install scripts.
- [ ] Add package-level smoke tests.
- [ ] Add package-level CI with `bash -n` and ShellCheck.
- [ ] Add shell completions in each package repo.

## Homebrew

Create a tap repository later:

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
