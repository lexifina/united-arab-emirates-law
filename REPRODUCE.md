# How this repository was made (United Arab Emirates)

This file is written by the build on 2026-10-30, the day the source data was retrieved.

## Sources

| Source | Address | Retrieved | Licence |
| --- | --- | --- | --- |
| UAE Legislation, Arabic act page for the Constitution (id 1000), Internet Archive capture 20250529114023 | <https://web.archive.org/web/20250529114023id_/https://uaelegislation.gov.ae/ar/legislations/1000/> | 2026-10-28 | Official text of the UAE federal government; no reuse licence stated on the site. |

Every word of law in this repository comes from these sources. Lexifina reads them and records each act's dated versions, and the laws that made each change, in one corpus file. This repository is built from that file.

## What is in it

| Act | Title | Versions | Span |
| --- | --- | ---: | --- |
| `constitution` | دستور دولة الإمارات العربية المتحدة | 1 | 2023-03-29 to 2023-03-29 |

The build made 1 commits:

| Commits | Kind |
| ---: | --- |
| 1 | first version of an act |
| 0 | one law on its in-force day |
| 0 | changes no amendment note explains, credited to the publisher |

Other counts:
- 0 commits on the branch `future`: laws not yet in force on 2026-10-30.
- 0 commits dated 1 January 1970: in force before 1970, with the real day in their `In-force` trailer.
- 0 laws in the record.
- 1 tags.

## Dates

Each commit is dated at noon (Asia/Dubai) on the day the change took effect. The other dates, enacted and published, are trailers.

When a law gives no date of its own, the default rule applies: Constitution art. 111: federal laws are published in the Official Gazette within two weeks of signature and come into force one month after publication unless the law provides otherwise. Each act's own in-force clause overrides this. https://uaelegislation.gov.ae/ar/legislations/1000

## How the history is built

`tools/build.py` turns the corpus into this history in one pass: one commit per law, on the day it took effect. The same corpus always gives the same commit hashes. `tools/check_repo.py` reads every version back from git and compares it with the corpus. `tools/on.py` shows the law as it stood on any date. The corpus format is described in `tools/SCHEMA.md`.

- Corpus: sha256 `b1900109158165d450ec3eecc797d9c6893a495e2b069d30cb65bb5bf96b397d` (96509 bytes).
- Builder blob hashes (`git hash-object`): `build.py` `a4faa25af85facb64b956b372f6b528aafdd7ec1`, `check.py` `3e59cb6f05eccb94a9ec14431a7f6781221e83ef`, `on.py` `644a6c0857fbcc72562032b58d57aa113fee0641`.
- Python 3.12.10; git version 2.46.0.windows.1.

## Checks

Not yet run for this build.

No second build of this corpus has been compared yet.

## Decisions made by hand

- Interim build: the Constitution is one "oldest version available" version (first_law null), dated 2023-03-29, the date the publisher gives for its last update, and credited to the publisher.
- Arabic is the authoritative text and is what is built; the English version on the same site is a reference only.
- Part and chapter headings are not yet kept as units; the preamble (loaded by the site via ajax) is not yet included.

## What AI did and did not do

The scripts that read the sources and build this repository were written by Claude Code running Claude Opus 5.5 (`claude-opus-5-5`) under Lexifina's direction.

No model wrote, translated or corrected legal text. No model runs at build time. Every word of law in this repository comes from the official sources above.

The commit messages are written by `build.py` from the source data.

Model use at data-build time:
- none: no model wrote, summarised or corrected any legal text; parsing is rule-based.
