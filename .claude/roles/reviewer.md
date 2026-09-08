# reviewer, in this project

<!-- covers: none -->

The role itself is shared: `~/.claude/agents/reviewer.md`, from the workflow repository.
This file is the part that is only true here, and it wins where the two disagree.

**There is no gate and no pipeline.** A review rests on the diff and on the served feed having been fetched and parsed; say plainly that no automated check exists.

Check the version, the URL and the length and signature fields against the artefact they claim to describe, and check which of the two feeds the change is in. An entry that is well-formed and wrong reaches every machine on that channel.

The request host is **github**. Release notes here are `notes/<version>.html`, one per version.
