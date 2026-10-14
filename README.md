# BiATA archive

Archive website of **BiATA**, the international conference
"Bioinformatics: from Algorithms to Applications" (2017–2021):
<https://andrewprzh.github.io/BiATA_archive/>

Each edition has a page with its dates, invited speakers, committees and
a link to the book of abstracts, plus a separate schedule page. The site is built with
[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).

## Layout

```
mkdocs.yml               site config and navigation
docs/index.md            home page with the list of editions
docs/<year>/index.md     edition overview: speakers, committees, links
docs/<year>/schedule.md  schedule (2017-2020 from Sched; 2021 talk order
                         from the book of abstracts)
docs/abstracts/          books of abstracts (PDF)
docs/assets/logos/       yearly BiATA logos
docs/assets/speakers/    invited speaker headshots
docs/assets/photos/      event photos
docs/files/              other documents (flyers)
docs/stylesheets/        colour and layout tweaks
```

## Editing

Pages are plain Markdown. To add an edition, copy an existing `docs/<year>/` folder,
add it to `nav` in `mkdocs.yml` and add a card to `docs/index.md`.
Put the book of abstracts into `docs/abstracts/` and link it from the page.

Preview locally:

```bash
pip install -r requirements.txt
mkdocs serve
```

## Deployment

Every push to `main` builds the site and publishes it to GitHub Pages
(`.github/workflows/deploy.yml`). In the repository settings,
**Pages → Build and deployment → Source** must be set to **GitHub Actions**.

## Sources

Content was taken from the original conference websites
(`biata<year>.spbu.ru`, captured in February 2024) and, for 2021,
from the Internet Archive. Schedules come from the conferences' Sched pages.
The 2017 photos, the 2018 flyer and the 2018 participant numbers come from
the organizers' Google Drive. The 2019-2021 abstracts were also published in
BMC Bioinformatics.
