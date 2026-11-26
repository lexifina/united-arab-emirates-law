# Structure of united-arab-emirates-law (federal law)

Folder names are in Arabic, the language federal law is enacted in. Each change to a text is one commit,
dated 12:00 UAE time on the day it took effect. Emirate law (Dubai, Abu Dhabi, ...) is in its own repositories.

| Folder | What it holds | Path pattern |
| --- | --- | --- |
| `الدستور/` | the Constitution | `الدستور/art-NNN.md` |
| `القوانين-الاتحادية/` | federal laws (قانون اتحادي) | `القوانين-الاتحادية/<السنة>/<رقم>.md` |
| `المراسيم-بقوانين-اتحادية/` | federal decree-laws (مرسوم بقانون اتحادي) | `المراسيم-بقوانين-اتحادية/<السنة>/<رقم>.md` |
| `قرارات-مجلس-الوزراء/` | Cabinet decisions and implementing regulations | `قرارات-مجلس-الوزراء/<السنة>/<رقم>.md` |
| `data/`, `tools/`, `visualisations/`, `vulnerabilities/` | tables, scripts and reports about the record | |

A law is one file, holding its text as the source last showed it, with its amendments listed in the header. The
source is the federal legislation portal (uaelegislation.gov.ae), read from Internet Archive copies because the live
site answers with a browser challenge; each commit names the capture (`Source:` and `Archive-capture:`).

Every commit carries `Kind:`, `In-force:` and `In-force-basis:` (the clause that sets the day). A text whose in-force
day cannot be read is not committed.

Until 2026-11-26 the Constitution was in `constitution/`; the folder was renamed in one commit (`data/paths.json`).
