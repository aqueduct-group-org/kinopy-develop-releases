# kinopy-develop-releases

Release binaries for **[Kinopy Develop](https://github.com/aqueduct-group-org/kinopy-develop-client)** — the desktop git client with built-in AI coding agents.

Source code lives in the **private** sibling repo `kinopy-develop-client`. This repo holds only the signed `.app.tar.gz` + minisign signature + `latest.json` manifest that the in-app Tauri updater fetches.

## How releases get here

Auto-published by CI on every merge to `main` of the source repo. The release tag is `v<semver>` from the source `'s `src-tauri/tauri.conf.json` `version` field. **Do not open PRs against this repo** — releases are produced by automation, not manual upload.

## Integrity

Every `.app.tar.gz` is signed with a minisign key whose public counterpart is embedded in the desktop app at build time. The Tauri updater verifies the signature before installing. Anyone can download these binaries; only signed bundles will install.

## Install

See the install instructions in the source repo: <https://github.com/aqueduct-group-org/kinopy-develop-client>.
