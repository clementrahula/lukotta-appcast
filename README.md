# Lukotta update feed

Two appcasts, served over GitHub Pages at `updates.lukotta.com`:

| Feed | Address |
| --- | --- |
| Release | <https://updates.lukotta.com/appcast.xml> |
| Beta | <https://updates.lukotta.com/beta/appcast.xml> |

[Lukotta](https://github.com/clementrahula/lukotta) checks the release feed.
The beta build has its own bundle identifier and checks the beta feed, so the
two can sit on one Mac without either offering the other's updates.

Each feed has a `notes` directory beside it holding the release notes its
entries link to. The archives are not here: they are attached to the releases
in the app's repository.

`scripts/release.sh` in the app's repository writes the feed entry and the
notes into a checkout of this repository, which is then committed.

Separate from the app's repository because a GitHub Pages site carries one
custom domain, and the project's own site already uses it.

## Maintaining

| Fact | Value |
| --- | --- |
| Artefacts | `appcast.xml`, `beta/appcast.xml`, the rendered notes beside each |
| Channel | GitHub Pages at `updates.lukotta.com`, public, fixed by `CNAME` |
| Publishing | a push to `main`; Pages serves the tree directly, so a merge is the release |
| CI | none |
| Claims | `scripts/checks.tsv`: both appcasts are well-formed XML |
| Checking a change | fetch the served feed; it parses and its entry points at an artefact that exists |
| Verifying a release | fetch both feed URLs over the network; each parses; the newest entry's artefact downloads |
| Request host | GitHub |
| Release notes | `notes/<version>.html`, one per version, rendered from the app repository's `releases/<version>.md` |
| Documents | `README.md`; plans and research go at the root |
| Visibility | public |

- A wrong or malformed entry reaches every installed copy on that channel at once: wrong build, downgrade, or no update.
- The two feeds are independent: a change to one is not a change to the other.
- A feed error shows only as the updater silently offering nothing: check the served feed, not the file in the tree.
- Check `version`, URL, `length` and signature against the artefact they describe, and which feed the entry is in.
- Feed validity depends on the Sparkle version the app embeds: appcast schema and signature requirements are read for that version.
- Release notes are shown in the app's update dialog, written for that reader, never generated from a commit log.
- Audit: both feeds parse, every artefact URL resolves, the channels are not crossed, `CNAME` matches the domain the app asks for.
- The feed addresses in the table at the top are configured against: they do not change silently.
