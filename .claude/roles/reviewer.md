# reviewer, in this project

<!-- covers: none -->

The role itself is shared and lives outside this repository, at `~/.claude/agents/reviewer.md`.
If you have cloned this project that file will not be there, and nothing here depends
on it: what follows is a description of THIS repository's commands, paths and hazards,
which is useful on its own. Where both exist, this file wins.

**There is no gate and no pipeline.** A review rests on the diff and on the served feed having been fetched and parsed; say plainly that no automated check exists.

Check the version, the URL and the length and signature fields against the artefact they claim to describe, and check which of the two feeds the change is in. An entry that is well-formed and wrong reaches every machine on that channel.

The request host is **github**. Release notes here are `notes/<version>.html`, one per version.
