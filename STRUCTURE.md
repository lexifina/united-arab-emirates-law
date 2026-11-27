# Structure of united-arab-emirates-law (federal law)

Folder names are in Arabic, the language federal law is enacted in. Each change to a text is one commit,
dated 12:00 UAE time on the day it took effect. Emirate law (Dubai, Abu Dhabi, ...) is in its own repositories.

| Folder | What it holds | Path pattern |
| --- | --- | --- |
| `الدستور/` | the Constitution | `الدستور/art-NNN.md` |
| `القوانين-الاتحادية/` | federal laws (قانون اتحادي) | `القوانين-الاتحادية/<السنة>/<رقم>.md` |
| `المراسيم-بقوانين-اتحادية/` | federal decree-laws (مرسوم بقانون اتحادي) | `المراسيم-بقوانين-اتحادية/<السنة>/<رقم>.md` |
| `قرارات-مجلس-الوزراء/` | Cabinet decisions and implementing regulations | `قرارات-مجلس-الوزراء/<السنة>/<رقم>.md` |
| `أنظمة-المصرف-المركزي/` | regulations, standards and other instruments of the Central Bank of the UAE in force, as its rulebook (rulebook.centralbank.ae) publishes them in Arabic | `أنظمة-المصرف-المركزي/<العنوان>.md` |
| `الأحكام/المحكمة-الاتحادية-العليا/` | judgments of the Federal Supreme Court, from the yearly volumes of its Technical Office, one file per judgment | `الأحكام/المحكمة-الاتحادية-العليا/<الدائرة>/<السنة>/<الشهر>/<اليوم>/<الرقم>-<سنة الطعن>.md` |
| `data/`, `tools/`, `visualisations/`, `vulnerabilities/` | tables, scripts and reports about the record | |

A law is one file, holding its text as the source last showed it, with its amendments listed in the header. The
source is the federal legislation portal (uaelegislation.gov.ae), read from Internet Archive copies because the live
site answers with a browser challenge; each commit names the capture (`Source:` and `Archive-capture:`).

Every commit carries `Kind:`, `In-force:` and `In-force-basis:` (the clause that sets the day). A text whose in-force
day cannot be read is not committed.

Until 2026-11-26 the Constitution was in `constitution/`; the folder was renamed in one commit (`data/paths.json`).

Next to an act's Arabic file, `<رقم>.en.md` holds the English text the portal publishes for it (an official translation; the Arabic text prevails), with the same day.


## Judgments

- `الأحكام/المحكمة-الاتحادية-العليا/` holds judgments of the Federal Supreme Court as its Technical Office
  prints them in the yearly volumes (مجموعة الأحكام: headnotes, then the judgment), one file per judgment,
  committed at 12:00 UAE time on the session day; the volume's index and the judgment's header must give
  the same day. The volumes are the Ministry of Justice's PDFs, read from Internet Archive captures
  (`Source:` and `Archive-capture:` on every commit), text layer only. Judgments the Ministry put up
  one by one as PDFs (2023-2025) are taken the same way, dated by the session day in their header.
- Personal-status judgments, and judgments about minors or sexual offences, are not published here.
