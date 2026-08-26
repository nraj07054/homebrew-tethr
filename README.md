# Homebrew tap for Tethr

[Tethr](https://github.com/nraj07054/tethr) links an Android phone to your Mac
over your own Wi-Fi — no account, no cloud, everything stays on your LAN.

```sh
brew install --cask nraj07054/tethr/tethr
```

Needs macOS 26 (Tahoe) or later, on Apple silicon.

Homebrew installs without the quarantine attribute a browser download would set,
so the app opens without the "damaged" warning that unnotarised apps produce.

The cask here is a copy of `Casks/tethr.rb` in the main repo, which is where it
is edited. Each release updates `version` and `sha256` — the release workflow
prints the digest as a notice for exactly that.
