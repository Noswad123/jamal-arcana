# Website Documentation

The personal website can be the polished public face of Jamal Arcana while this repository remains the canonical ecosystem docs source.

## Recommended roles

### Personal website

- project cards
- tool lore
- screenshots and demos
- high-level explanations
- links to package repos

### Jamal Arcana repo

- architecture decisions
- package boundary rules
- integration recipes
- release roadmap
- contributor-facing docs

### Package repos

- install instructions
- command reference
- troubleshooting
- tests and implementation details

## Suggested website project card

```json
{
  "title": "Jamal Arcana",
  "status": "Planning",
  "statusType": "in-progress",
  "description": "A fantasy-inspired ecosystem of local-first command-line tools for navigation, workflow summoning, and knowledge craft.",
  "githubUrl": "https://github.com/Noswad123/jamal-arcana",
  "techStack": ["Bash", "CLI", "Documentation"],
  "loreSlug": "jamal-arcana"
}
```

## Possible docs routes

If the website grows project detail pages, Jamal Arcana could use:

```text
/projects/jamal-arcana
/lore/jamal-arcana
/arcana/wisp
/arcana/waystone
```
*** Add File: /Users/jdawson/Projects/jamal-arcana/docs/tools/wisp.md
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
