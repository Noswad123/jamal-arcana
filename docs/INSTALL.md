# Install

The recommended public install path is Homebrew.

## Homebrew

```bash
brew tap Noswad123/jamal-arcana
brew install wisp
brew install waystone
```

Or install directly from the tap:

```bash
brew install Noswad123/jamal-arcana/wisp
brew install Noswad123/jamal-arcana/waystone
```

## Verify

```bash
which wisp
which waystone
wisp --help
waystone --help
```

On Apple Silicon Macs, Homebrew usually installs commands under:

```text
/opt/homebrew/bin
```

## Development installs

Package repositories also support source installs:

```bash
cd ~/Projects/wisp
./install.sh

cd ~/Projects/waystone
./install.sh
```

Source installs default to:

```text
~/.local/bin
```

If `~/.local/bin` appears before `/opt/homebrew/bin` in `PATH`, local development copies will override Homebrew copies. Remove the local copy to test the released Homebrew version:

```bash
rm ~/.local/bin/wisp
rm ~/.local/bin/waystone
```

## Shell completions

Both package installers and Homebrew formulae install zsh and bash completions.

For zsh, restart the shell after installation:

```bash
rm -f ~/.zcompdump*
exec zsh
```
