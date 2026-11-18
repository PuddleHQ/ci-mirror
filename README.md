# ci-mirror

Unmodified copies of third-party release binaries that [Puddle](https://github.com/PuddleHQ/puddle)'s CI
downloads, so a run does not fail when the upstream download host is unreachable.

Puddle's CI checks every file against a SHA-256 pinned in the Puddle repository (for example
`ci/forgejo.sha256`), whichever host it came from. A file here is used only when its checksum
matches that pin, so this mirror adds no trust of its own.

Each release of this repository holds one upstream release, named `<project>-v<version>`. The
binaries are byte-for-byte the upstream release assets. They are not modified or rebuilt.

| Release | Upstream | Licence | Corresponding source |
|---|---|---|---|
| `forgejo-v17.0.1` | [Forgejo 17.0.1](https://codeberg.org/forgejo/forgejo/releases/tag/v17.0.1) | GPL-3.0-or-later ([text](LICENSES/forgejo-GPL-3.0.txt)) | [codeberg.org/forgejo/forgejo, tag v17.0.1](https://codeberg.org/forgejo/forgejo/src/tag/v17.0.1); the source archive `forgejo-src-17.0.1.tar.gz` is on the same upstream release page |
| `gitea-v28.3.0` | [Gitea 28.3.0](https://github.com/go-gitea/gitea/releases/tag/v28.3.0) | MIT ([text](LICENSES/gitea-MIT.txt)) | [github.com/go-gitea/gitea, tag v28.3.0](https://github.com/go-gitea/gitea/tree/v28.3.0) |

Forgejo is free software under the GNU General Public License, version 3 or later. You can get the
complete corresponding source code for the Forgejo binary here from the upstream links above. If
those links stop working, open an issue in this repository and we will send you the source.

Copyright of the binaries stays with their authors. This README is under CC0-1.0.
