# architect, in this project

<!-- covers: none -->

The role itself is shared: `~/.claude/agents/architect.md`, from the workflow repository.
This file is the part that is only true here, and it wins where the two disagree.

Plans go at the repository root.

What failure costs here is **every installed copy at once**. An updater reads these feeds; a malformed or wrong entry can offer the wrong build, a downgrade, or nothing at all to every machine on that channel, and the people affected did not do anything to cause it.

The constraints: Sparkle's appcast format, two independent channels (release and beta) whose builds carry different bundle identifiers, and GitHub Pages serving at a custom domain fixed by `CNAME`.
