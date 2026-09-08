# auditor, in this project

<!-- covers: none -->

The role itself is shared and lives outside this repository, at `~/.claude/agents/auditor.md`.
If you have cloned this project that file will not be there, and nothing here depends
on it: what follows is a description of THIS repository's commands, paths and hazards,
which is useful on its own. Where both exist, this file wins.

There are no gates and no CI; that absence is the first finding, on a repository every installed copy reads.

Nothing here writes to the tree.

What is worth checking: that both feeds parse, that every entry's artefact URL still resolves, that the two channels have not been crossed, and that `CNAME` still matches the domain the application asks for.
