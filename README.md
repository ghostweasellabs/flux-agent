# flux-agent

Public distribution repository for the Flux tunnel agent CLI.

Binaries are built by GitHub Actions from the [ghostweasellabs/flux](https://github.com/ghostweasellabs/flux) monorepo (or this repo once split) and published to [Releases](https://github.com/ghostweasellabs/flux-agent/releases).

## Install

```bash
# Latest release (linux amd64 example)
curl -fsSL -o flux-agent \
  https://github.com/ghostweasellabs/flux-agent/releases/latest/download/flux-agent-linux-amd64
chmod +x flux-agent
./flux-agent http 8080
```

## Documentation

https://ghostweasellabs.github.io/flux/agent.html

## CI

This directory is the scaffold for the public repo. Copy contents to `ghostweasellabs/flux-agent` and configure:

- `FLUX_SOURCE_CHECKOUT_TOKEN` — read access to `ghostweasellabs/flux` monorepo
- `FLUX_SOURCE_REPO` variable (optional) — defaults to `ghostweasellabs/flux`

Workflow: `.github/workflows/flux-agent-releases.yml` (publishes releases **in this repo**, not the monorepo).

## Source

Development happens in the `flux` monorepo under `cmd/flux-agent`.