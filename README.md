<p align="center"><img src="assets/havooch-app-icon.png" width="128" alt="Havooch's app icon: the head of Havuç, an orange tabby cat with pink ears, on a white rounded tile"></p>

<h1 align="center">havooch-mate</h1>

<p align="center">The agent skill for <a href="https://github.com/yahyabedirhan/havooch">Havooch</a>.</p>

## What is Havooch

[Havooch](https://github.com/yahyabedirhan/havooch) is a video player for your Mac that lets you give feedback to a coding agent the way you'd give it to a person.

Record your screen, or open any video of the thing you're building. Pause where something looks wrong, point at it on the frame, and write what you want changed. When you're done, send your comments to your agent. It gets each comment with the moment and the frame it's about, does the work, and answers you right there beside the video.

## What is havooch-mate

havooch-mate is the skill that teaches your coding agent its side of that loop. With it, your agent knows how to:

- wait for the comments you send from Havooch
- work through each one in your repository
- reply on the comment's thread, inside the player
- ask you there when something isn't clear

It works with Claude Code, Codex, Cursor, Pi and OpenCode.

## Install

1. [Install Havooch](https://github.com/yahyabedirhan/havooch#install).
2. Install the skill:

   ```sh
   npx skills add yahyabedirhan/havooch-mate --skill havooch-mate --global
   ```

Havooch's Connect view can also run this for you. To update the skill later, run the same command again.

## Licence

MIT. See [LICENSE](LICENSE).

If you use havooch-mate, or build on it or its ideas, please cite it. GitHub's **Cite this repository** button gives you the reference, from [`CITATION.cff`](CITATION.cff).
