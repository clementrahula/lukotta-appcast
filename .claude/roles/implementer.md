# implementer, in this project

<!-- covers: none -->

The role itself is shared and lives outside this repository, at `~/.claude/agents/implementer.md`.
If you have cloned this project that file will not be there, and nothing here depends
on it: what follows is a description of THIS repository's commands, paths and hazards,
which is useful on its own. Where both exist, this file wins.

There is no gate and no CI. What checks a change is fetching the served feed and confirming it parses and points at an artefact that exists.

Two feeds, not one: `appcast.xml` for release and `beta/appcast.xml` for beta. They are independent, and a change made to one is not a change to the other however similar they look.

Release notes are `notes/<version>.html`, one file per version, rendered from the application repository's `releases/<version>.md`. They are what a person reads in the update dialog, so they are written for that reader and never generated from a commit log.

Errors surface as an updater silently not offering an update, which is why the served feed is fetched rather than the file read.
