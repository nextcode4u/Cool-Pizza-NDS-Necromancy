# Contributing

Cool Pizza: Necromancy welcomes gameplay changes, new content, performance
improvements and DS-specific features. Describe changes to the gameplay baseline
explicitly and update the relevant tests. Original game credits belong in
[CREDITS.md](CREDITS.md).

Changes aimed at reproducing the original iOS game also belong in the
[faithful reconstruction](https://github.com/nextcode4u/Cool-Pizza-NDS-).

## Development

Install the SDK using [the build guide](docs/build.md). Prepared assets are
included in the repository.
For gameplay or rendering changes:

```sh
make -j2
make -f Makefile.host test
```

Use the existing C style and keep generated data changes in the asset preparation
scripts. Commit updated `source/original_data.c` and `nitro/audio/` outputs
when changing asset conversion so a fresh clone remains buildable.

## Bug reports

Include the device or emulator, ROM version/hash, affected wave or enemy and
steps to reproduce. Screenshots or a short recording help explain visual issues.
For behavior differences, include a reference to the original game when possible.

## Pull requests

Describe the resulting behavior and the checks run. Keep original IPA archives,
BIOS/firmware, emulator bundles, temporary recovery files and ROM build outputs
out of pull requests.
