# moggi-lang.org

The website. Hand-written HTML and CSS, no build step, no framework: served from
this directory as-is. `logo.svg` is the mark beside the title and the favicon;
`icon.png` is the same artwork at 128×128, for `apple-touch-icon` and browsers
that take no SVG favicon.

## Where it points

| link | assumes |
| --- | --- |
| Download | `github.com/moggi-lang/moggi/releases/download/<release>/`, the archives the packaging workflow attaches |
| Documentation, Quickstart, Differences to Haskell | `docs.moggi-lang.org`, rendering the repository's `docs/*.md` |
| Standard library | `registry.moggi-lang.org/docs/base/<version>/`, the tree the bundled `base` release published |
| Packages | `registry.moggi-lang.org`, the registry in `../registry-data/` |
| Source, Releases | `github.com/moggi-lang/moggi` |

Rename or re-point any of those in `index.html`; nothing else depends on them.

The standard library link names a **release**, because that is what its pages
belong to: `docs/base/0.2.0/index.html` is the tree that release published, and
the registry serves it under the version it was published as. Bumping the bundled
`base` means re-pointing that link at the new version. `docs.moggi-lang.org/stdlib/`
is no longer generated — a release's documentation has one home, and it is the
release's own, not a second copy rendered somewhere else.
