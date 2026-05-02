# homebrew-deepend

Homebrew tap for [Deepend](https://github.com/deepen-stha/deepend-releases) — a free,
cross-platform desktop app that bundles JSON, text, PDF, API, and image developer
utilities, running 100% offline.

## Install

```sh
brew tap deepen-stha/deepend
brew install --cask deepend
```

That's it. Subsequent `brew upgrade` will pick up new releases automatically
(detected via this tap's `livecheck` against the public releases repo).

## Why a self-hosted tap and not the main `homebrew/homebrew-cask`?

Two reasons, both temporary:

1. **Notarization.** The official Cask repo requires every app to be signed
   and notarized by Apple ($99/yr Apple Developer Program + a Developer ID
   certificate + a notarization step in CI). Deepend's `.dmg` is not signed
   yet, so the official audit rejects it. macOS will warn "Apple cannot
   verify this app" on first launch — right-click → **Open** to bypass.

2. **Notability.** The official Cask repo also requires self-submitted apps
   to have 225+ stars or 90+ forks/watchers on the homepage repo. Deepend
   is brand new.

Once both are satisfied, the cask will move to the official repo and you
can drop the `brew tap` step.

## Uninstall

```sh
brew uninstall --cask deepend
brew untap deepen-stha/deepend   # optional
```

## License

MIT — see [LICENSE](./LICENSE).
