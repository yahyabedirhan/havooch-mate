# Decisions: publishing

How this repository gets its files. Read this file before you change anything here. Add an entry for each new decision: the date, what was decided, and why.

## 2026-10-08

- **This repository is a published copy.** The skill is maintained in `.agents/skills/havooch-mate/` of [yahyabedirhan/havooch](https://github.com/yahyabedirhan/havooch). Change it there, in the same pull request as the app change it describes.
- **Each Havooch release writes over the skill's files.** The `mate` job of havooch's `release.yml` runs `scripts/update-mate.sh`. The script removes each tracked file here and copies the skill in, then commits `havooch-mate <version>` on `main` and pushes. It keeps this repository's own files: `README.md`, `LICENSE`, `AGENTS.md`, `CLAUDE.md` and everything under `docs/`. A new kind of file here needs its path in `own_files` in that script first.
- **No tags and no version match.** `main` holds the skill of the latest Havooch release. People install the latest skill and keep the app up to date.
- **Why a repository of its own:** the skills CLI clones the full repository of an `owner/repo` source. A clone of havooch is 269 MB. A clone of this repository is less than 1 MB.
- **The push uses the maintainer's token.** It is the Actions secret `TAP_TOKEN` in havooch, a fine-grained token with Contents: read and write on this repository and on `yahyabedirhan/homebrew-tap`. It expires after one year. havooch's `docs/decisions/release-publishing.md` says how to renew it.
- **This repository stays public.** The skills CLI clones it without a login.
