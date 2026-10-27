# Kadal's Homebrew tap

[Kadal Deck](https://deck.kadal.cc/) for macOS: the desktop app and the `kadal-deck` command.

```sh
# The desktop app (one universal build for Apple Silicon and Intel, macOS 11 or later)
brew install --cask kadalcc/tap/kadal-deck

# The command-line tool, from npm @kadal/deck (needs Node, which Homebrew installs)
brew install kadalcc/tap/kadal-deck
```

Or tap once and use the short names: `brew tap kadalcc/tap`, then `brew install --cask kadal-deck`
and `brew install kadal-deck`. Homebrew 7 and later load a third-party tap's short names only once
you trust it: `brew trust kadalcc/tap` (the full `kadalcc/tap/…` names above work either way).

## The first launch

The app is not notarised by Apple yet, so macOS blocks it the first time. Open it from
Applications, click **Done** on the warning, then go to **System Settings → Privacy & Security** and
click **Open Anyway**. You do this once: the app updates itself afterwards, and every update is
checked against Kadal's signature before it installs. Steps with pictures:
<https://deck.kadal.cc/download/#macos>.

## What is here

| File                  | Installs                                                                 |
| --------------------- | ------------------------------------------------------------------------ |
| `Casks/kadal-deck.rb` | Kadal Deck.app, from `deck.kadal.cc/download/<version>/` (SHA-256 pinned) |
| `Formula/kadal-deck.rb` | `kadal-deck`, the npm package `@kadal/deck` installed into Homebrew's prefix |

The manifests are generated from the published files by Kadal's release pipeline; please open an
issue rather than a pull request that edits them. Bugs in the app or the CLI:
<https://github.com/kadalcc/deck/issues>.

The manifests in this repository are MIT-licensed. Kadal Deck itself is free to use
([terms](https://deck.kadal.cc/terms/)); the `@kadal/deck` engine and CLI are AGPL-3.0-or-later.
