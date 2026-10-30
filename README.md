# United Arab Emirates: law history in git

The law of United Arab Emirates as a git history: one file per provision, one commit per law on the day it took effect, and the law that made each change as the commit's author. `git blame` names the law behind every paragraph; `git log` lists every change; picking a date gives the text in force that day.

It follows the shared design of [lexifina/global-law](https://github.com/lexifina/global-law).

**What is in it now (a first build, not complete)**

| Folder | Act | Versions | History |
| --- | --- | ---: | --- |
| `constitution/` | دستور دولة الإمارات العربية المتحدة (Constitution of the United Arab Emirates) | 1 | One version: the text on the UAE Legislation portal, whose last-update date is 29 March 2023. No earlier versions are online. |

**Language.** Arabic, the authoritative text. The English version on the same portal is not used. This README is in English.

## Dates

The Constitution has no earlier version online, so its single commit is "oldest version available", dated by the portal's own last-update date (29 March 2023) and credited to the publisher.

## How it is checked

Every version is read back from git on the day it took effect and on the day before (`tools/check_repo.py`) and must match `corpus.json`; results are in `REPRODUCE.md`.

## What "author" means

The author of a commit is the law that made the change, with an e-mail address that cannot exist (`<law key>@uaelegislation.gov.ae.invalid`). For this single version the author is the publisher. The committer is always Lexifina.

## Limits

Only the current text is held, so there is no amendment history. Articles 1 to 152 are included; part and chapter headings are not kept, and the preamble (which the portal loads separately) is not included.
