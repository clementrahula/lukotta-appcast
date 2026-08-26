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
