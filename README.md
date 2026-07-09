# Uncaged Homebrew tap

Homebrew tap for [Uncaged](https://getuncaged.dev) — the account-free,
bring-your-own-model fork of the open-source Warp terminal.

```bash
brew install --cask getuncaged/tap/uncaged
```

The cask in [`Casks/uncaged.rb`](Casks/uncaged.rb) points at the per-arch DMGs
of the matching [GitHub release](https://github.com/getuncaged/uncaged/releases)
and is pinned to a specific version + checksums. On each new Uncaged release,
bump `version` and both per-arch `sha256` in the cask (see "Updating the cask"
at the bottom of the file).

Uncaged is **ad-hoc signed** (no Apple Developer ID). Homebrew clears the
download quarantine for casks it installs; if Gatekeeper still complains, run:

```bash
xattr -dr com.apple.quarantine "/Applications/Uncaged.app"
```
