# homebrew-tap

Shared [Homebrew](https://brew.sh) tap for the [mathomhaus](https://github.com/mathomhaus) family of CLI tools.

## Install a tool

```bash
brew install mathomhaus/tap/<tool>
```

Homebrew resolves `mathomhaus/tap` to `github.com/mathomhaus/homebrew-tap`
automatically — no explicit `brew tap` step is required.

## Available tools

| Tool | Install | Description |
|---|---|---|
| [**guild**](https://github.com/mathomhaus/guild) | `brew install mathomhaus/tap/guild` | Continuity and coordination for AI agents. One SQLite archive, no cloud, no vendor lock. |

More tools will land here as the mathomhaus family grows.

## How this tap works

Each tool in the [mathomhaus](https://github.com/mathomhaus) org runs its own
release pipeline. On a versioned tag push, the tool's `goreleaser`
configuration publishes binaries to its GitHub Release and drops (or updates)
its cask file here under `Casks/`. Tool releases are independent — a new
`guild` release does not disturb any sibling tool's cask.

## Verifying releases

Tools in this tap are cosign-signed (keyless, via Sigstore). To verify a
downloaded release manually, see the verification steps in the tool's own
repository — e.g. `guild`'s
[`SECURITY.md`](https://github.com/mathomhaus/guild/blob/main/SECURITY.md).

Homebrew itself verifies SHA256 checksums automatically on install.

## Issues

Report tool-specific bugs in the tool's own repo (not here). Use this repo's
issues only for tap-level problems (e.g. a broken cask file, stale version).

## License

Apache 2.0 — see [LICENSE](./LICENSE). Each tool distributed through this tap
carries its own license; see the tool's source repository.
