# release, in this project

<!-- covers: none -->

The role itself is shared and lives outside this repository, at `~/.claude/agents/release.md`.
If you have cloned this project that file will not be there, and nothing here depends
on it: what follows is a description of THIS repository's commands, paths and hazards,
which is useful on its own. Where both exist, this file wins.

The artefacts are `appcast.xml`, `beta/appcast.xml` and the rendered notes under `notes/`.

The channel is GitHub Pages at `updates.lukotta.com`, publicly reachable, fixed by `CNAME`.

Publishing is a push to the default branch; Pages serves the tree directly, so a merge IS the release.

Verify from outside by fetching both feed URLs over the network, confirming each parses, and confirming the newest entry points at an artefact that downloads - not by reading the files in the tree, which is what was pushed rather than what is served.
