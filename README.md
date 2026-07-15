# Jacobs Barbers — Website Concepts

Three concept directions for jacobsbarbers.ca, built for Lucyna Jacobs' review. All three share the same real business details (address, phone, $45 flat pricing, online booking link) and the same core colour direction she requested — white, pale grey, charcoal, and a soft spring green for the booking button. They differ in typography and how far the layout leans into an editorial, high-fashion feel.

## The three versions

| | Version | What it is |
|---|---|---|
| 1 | [**Live / Reference**](v1-live/) | Typography matched to the gubynska.com reference (EB Garamond throughout). Full-bleed hero photo with the logo and address overlaid directly on the image. |
| 2 | [**Classic**](v2-classic/) | Same layout and content as Version 1, with softer, more traditional typography (Instrument Serif + Inter) instead of the EB Garamond match. |
| 3 | [**Concept**](v3-concept/) | The most ambitious direction — oversized editorial type, a bold full-bleed spring-green statement section, an asymmetric masonry gallery, scroll-triggered reveal animations, and a numbered "editorial index" treatment for the services list. Same palette and business details throughout. |

## Still pending real content (all three versions)

- Beard trim and cut-and-beard-combo pricing (currently marked `TBD`)
- Full weekly hours (currently marked `TBD` except Mon/Sun closed)
- Real gallery photos (currently grey placeholders — see `HOW-TO-UPDATE-PHOTOS.txt` inside each version's folder)
- Real "banner" photo, if the drifting banner section gets re-enabled (currently hidden in v1 and v2; not used in v3's design)

Once any of these are finalized, they can be dropped into all three versions in one pass.

## Structure

```
.
├── README.md
├── v1-live/
│   ├── index.html
│   ├── HOW-TO-UPDATE-PHOTOS.txt
│   └── images/
├── v2-classic/
│   ├── index.html
│   ├── HOW-TO-UPDATE-PHOTOS.txt
│   └── images/
└── v3-concept/
    ├── index.html
    └── images/
```

Each version is fully self-contained — no build step, no dependencies beyond Google Fonts and a Google Maps embed.

## Viewing locally

Open any version's `index.html` directly in a browser, or serve the whole repo:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000/v1-live/  (or v2-classic/, v3-concept/)
```

## Deploying with GitHub Pages

1. Push this repo to GitHub (see below).
2. In the repo's Settings → Pages, set Source to "Deploy from a branch," branch `main`, folder `/ (root)`.
3. Each version will be reachable at:
   ```
   https://<username>.github.io/<repo-name>/v1-live/
   https://<username>.github.io/<repo-name>/v2-classic/
   https://<username>.github.io/<repo-name>/v3-concept/
   ```

## Pushing to GitHub

This folder is already an initialized git repository with one commit. To push to a new GitHub repo:

```bash
git remote add origin https://github.com/<your-username>/<your-repo-name>.git
git branch -M main
git push -u origin main
```
