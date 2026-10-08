<p align="center"><img src="assets/havooch-app-icon.png" width="128" alt="Havooch's app icon: the head of Havuç, an orange tabby cat with pink ears, on a white rounded tile"></p>

<h1 align="center">havooch-mate</h1>

The agent skill for [Havooch](https://github.com/yahyabedirhan/havooch).

**Havooch** is a native macOS video player for giving feedback to coding agents. You pause a video, point at its frame and comment. Cmd+Enter sends your comments as one batch to your agent, with the timestamp, the keyframe and the transcript around each one. The agent does the work and answers beside the video.

**havooch-mate** teaches your coding agent to be the listener: it waits for each batch from Havooch, does what each comment asks in your repository, and answers on its thread inside the player. When it can't tell what you mean, it asks you there. It works with Claude Code, Codex, Cursor, Pi and OpenCode.

## Install

Install [Havooch](https://github.com/yahyabedirhan/havooch#install) first. Then install the skill:

```sh
npx skills add yahyabedirhan/havooch-mate --skill havooch-mate --global
```

Havooch's Connect view runs the same command for the agent you pick. To update the skill, run the command again.
