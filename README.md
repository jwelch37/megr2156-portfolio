# MEGR 2157 – Design Portfolio Template

This repository is an MkDocs site (same engine Fab Academy uses) with the Analyze / Decide / Communicate framework built into every assignment page. The rendered site — with the left-hand navigation to every assignment — lives in `docs/`; this README is just for people working with the repo itself.


## Don't do, possible save for later. Preview locally

```bash
pip install -r requirements.txt
mkdocs serve
```
### sub header

Then open http://127.0.0.1:8000 in your browser. The sidebar nav updates automatically from `mkdocs.yml`.

## Publish

Push to `main` — the included GitHub Actions workflow (`.github/workflows/deploy.yml`) builds the site and publishes it to GitHub Pages automatically.

## Structure

```
MEGR-2156-7-template/
├── .github/
│   └── workflows/
│       └── deploy.yml          <- GitHub Actions: auto-builds and deploys to Pages on every push
├── docs/
│   ├── index.md                <- Portfolio homepage (About Me, Homepage Identity, Decision Standard)
│   ├── portfolio-overview.md   <- Running index of all assignments with status
│   ├── aboutme/
│   │   └── index.md            <- About Me page
│   └── assignments/
│       ├── A01/
│       │   └── index.md        <- A1: Build Your Professional Portfolio
│       ├── A02/
│       │   └── index.md        <- A2: Truss Stress Analysis
│       ├── A03/
│       │   └── index.md        <- A3: Parametric Design and FEA
│       ├── A04/
│       │   └── index.md        <- A4: Motor Mount
│       ├── A05/
│       │   └── index.md        <- A5: Bracket Stress
│       ├── A06/
│       │   └── index.md        <- A6: Bracket Drawing
│       ├── A07/
│       │   └── index.md        <- A7: Bracket FEA
│       ├── A08/
│       │   └── index.md        <- A8: Gear Box
│       ├── A09/
│       │   └── index.md        <- A9: Pulley System
│       ├── A09x-concept-selection/
│       │   └── index.md        <- A9x: Pugh Matrix — Gear vs. Pulley vs. Lead Screw
│       ├── A10/
│       │   └── index.md        <- A10: Lead Screw Part 1
│       ├── A11/
│       │   └── index.md        <- A11: Lead Screw Part 2 / Motor Selection
│       └── A12/
│           └── index.md        <- A12: [Final Assignment]
├── templates/
│   └── assignment-template.md  <- Blank assignment page for reference (not published)
├── .gitignore
├── mkdocs.yml                  <- Controls site nav (left sidebar) — do not restructure
├── requirements.txt            <- Python dependencies for MkDocs Material
└── README.md                   <- This file
```

## Adding or renaming an assignment

1. Add a new folder under `docs/assignments/` with an `index.md`.
2. Add a matching line to the `nav:` section of `mkdocs.yml` — this is what makes it appear in the sidebar on every page.
