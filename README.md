# Homebrew tap for Tethr

[Tethr](https://github.com/nraj07054/tethr) links an Android phone to your Mac
over your own Wi-Fi — no account, no cloud, everything stays on your LAN.

```sh
brew install --cask nraj07054/tethr/tethr
xattr -dr com.apple.quarantine /Applications/Tethr.app
```

Needs macOS 26 (Tahoe) or later, on Apple silicon.

The second line is not optional. Tethr is signed ad-hoc rather than notarised —
notarisation needs a paid Apple Developer account this project does not have —
and Homebrew quarantines every cask it installs, with no opt-out since Homebrew
6. Left tagged, macOS refuses to open the app: *"Apple could not verify 'Tethr'
is free of malware..."*. Clearing the tag does not weaken anything else;
Gatekeeper still checks the signature.

The cask here is a copy of `Casks/tethr.rb` in the main repo, which is where it
is edited. Each release updates `version` and `sha256` — the release workflow
prints the digest as a notice for exactly that.
