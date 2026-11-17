# scoop-vaultfold

The Scoop bucket for [vaultfold](https://vaultfold.app/), a team secrets manager that keeps encrypted vaults in git or any dumb blob store.

## Install

```
scoop bucket add vaultfold https://github.com/bendechrai/scoop-vaultfold
scoop install vaultfold
```

The manifest covers Windows on x64 (`64bit`) and arm64. It installs `vaultfold.exe` and `vaultfold-native-host.exe`, the helper the browser extension talks to. Upgrade with `scoop update vaultfold`.

## How this repository is maintained

Do not edit it by hand. Every vaultfold release writes the manifest `vaultfold.json` at the root of this repository with [GoReleaser](https://goreleaser.com/), from the project's `.goreleaser.yaml`, with the release's download URLs and SHA-256 sums. Pre-releases never update the bucket. Because every release pushes a current manifest, it has no `checkver` or `autoupdate` section. A change made here directly is overwritten by the next release.

Until the first release this repository holds only this README.

## Signing

The binaries are not yet signed with Authenticode, so Windows SmartScreen may warn the first time they run. Every release's `checksums.txt` is signed with the project's minisign key, which is the integrity guarantee. How to verify a release is in the vaultfold repository's `docs/release.md`, "Verifying a release".

vaultfold is also published to winget as `Vaultfold.Vaultfold`.

## Problems

Report problems with the manifest or the install in the [vaultfold repository](https://github.com/bendechrai/vaultfold/issues), not here.
