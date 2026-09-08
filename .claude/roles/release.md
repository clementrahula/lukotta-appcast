# release, in this project

<!-- covers: none -->

The role itself is shared: `~/.claude/agents/release.md`, from the workflow repository.
This file is the part that is only true here, and it wins where the two disagree.

The artefacts are `appcast.xml`, `beta/appcast.xml` and the rendered notes under `notes/`.

The channel is GitHub Pages at `updates.lukotta.com`, publicly reachable, fixed by `CNAME`.

Publishing is a push to the default branch; Pages serves the tree directly, so a merge IS the release.

Verify from outside by fetching both feed URLs over the network, confirming each parses, and confirming the newest entry points at an artefact that downloads - not by reading the files in the tree, which is what was pushed rather than what is served.
