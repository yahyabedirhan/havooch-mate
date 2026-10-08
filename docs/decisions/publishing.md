# Decisions: publishing

How this repository gets its files. Read this file before you change anything here. Add an entry for each new decision: the date, what was decided, and why.

## 2026-10-08

- **This repository is a published copy.** The skill is maintained in `.agents/skills/havooch-mate/` of [yahyabedirhan/havooch](https://github.com/yahyabedirhan/havooch). Change it there, in the same pull request as the app change it describes.
- **The skill sits in `skills/havooch-mate/`, not at the root.** The skills CLI copies the whole folder that holds `SKILL.md`. At the root, an install also copied this repository's `README.md` into each person's skill folder. In its own folder, only the skill installs.
- **Each Havooch release writes over `skills/havooch-mate/`.** The `mate` job of havooch's `release.yml` runs `scripts/update-mate.sh`. The script replaces that folder with the skill, then commits `havooch-mate <version>` on `main` and pushes. It does not touch the rest of this repository.
- **No tags and no version match.** `main` holds the skill of the latest Havooch release. People install the latest skill and keep the app up to date.
- **Why a repository of its own:** the skills CLI clones the full repository of an `owner/repo` source. A clone of havooch is 269 MB. A clone of this repository is less than 1 MB.
- **The push uses the maintainer's token.** It is the Actions secret `TAP_TOKEN` in havooch, a fine-grained token with Contents: read and write on this repository and on `yahyabedirhan/homebrew-tap`. It expires after one year. havooch's `docs/decisions/release-publishing.md` says how to renew it.
- **This repository stays public.** The skills CLI clones it without a login.
