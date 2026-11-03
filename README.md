# Junha Chun - academic website

A simple academic homepage for GitHub Pages, with a short biography, publication figures and one-sentence summaries, education, and grants. No build step, JavaScript framework, external fonts, or analytics are required.

## Preview

From this directory:

```sh
python3 -m http.server 8765 --bind 127.0.0.1
```

Open http://127.0.0.1:8765/. The site works at narrow mobile widths and includes keyboard focus indicators and semantic headings. There are no animations.

## Editing

- `index.html`: biography, publications and their summaries, education, and grants.
- `stylesheet.css`: layout, typography, responsive rules, and print styles.
- `Junha_Chun_CV.pdf`: retained CV file; the homepage does not link to it.
- `favicon.svg`: the local site icon.
- `images/junha-chun.jpg`: the supplied portrait, displayed on the right of the introduction.
- `images/`: local publication figures. Each thumbnail links to its full-size image.

In the parent CV workspace, `JunhaChun_CV_261013.md` is the editable CV source and `scripts/build_cv.py` produces the two-page PDF with ReportLab and pypdf, then synchronizes this directory's downloadable copy. The original Markdown CV is preserved under `../originals/`.

```sh
cd ..
python3 scripts/build_cv.py
```

Use a Python environment containing `reportlab` and `pypdf`. Output: `output/pdf/Junha_Chun_CV.pdf`.

## Hosting

The source branch in this repository is `master`. Configure GitHub Pages to publish the desired branch from its root directory. The inherited `CNAME` pointed to `jonbarron.info`; it has been removed so it cannot redirect this personal site to the original template author's domain. Add a custom domain only when an owned domain is configured. Local changes must be reviewed and pushed before they affect the live site.

## Content verification - November 2026

- Conference statuses were checked against the [Sparse Imagination](https://nikriz1.github.io/sparse_imagination/), [VILA](https://joon-stack.github.io/VILA/), and [PoLAR](https://joon-stack.github.io/PoLAR/) project pages.
- Sparse Imagination's 40.5% planning-time reduction is the reported simulation average at 50% token dropout (69.7% success versus 69.8% for full tokens); it is not a general claim of identical performance on every task.
- The IEEE Access title and year follow publisher-deposited [Crossref metadata](https://api.crossref.org/works/10.1109/access.2024.3480791): **Toward** Generalized Visualization System for Various CNN Models: Module and Layer View, **2024**.
- The segmentation preprint identifier is [2007.03169](https://arxiv.org/abs/2007.03169), correcting the original CV's 2007.03194.
- The world action model priors preprint is [2610.29168](https://arxiv.org/abs/2610.29168). The homepage lists it as an arXiv preprint without review status.
- The March 2019 Ph.D. start date and advisor transition follow the existing homepage. No graduation date has been inferred.
- The original CV's CoRL 2026 workshop reference for the priors paper did not specify the workshop name or whether it was accepted. It is omitted pending confirmation, rather than presented as an accepted publication.
- The homepage omits the CV and GitHub profile links and displays six publications focused on robot learning and world models.
- The concise CV omits street address, mobile number, GPA, and expired English test scores. Those details remain in the preserved original. Language proficiency and JLPT N2 are retained.

The earlier site was based on [Jon Barron's academic website](https://github.com/jonbarron/jonbarron_website).

## Publication images

The homepage uses the following author-provided or paper figures. Their original proportions are preserved; no generated scientific figures are used.

| Local asset | Source |
| --- | --- |
| `images/wam-priors.svg` | [Figure 1, representational priors paper](https://arxiv.org/html/2610.29168v1#S1.F1) |
| `images/polar.png` | [PoLAR project overview](https://joon-stack.github.io/PoLAR/) |
| `images/joint-faults.png` | [Figure 1, joint-level faults paper](https://arxiv.org/html/2606.10501v1#S1.F1) |
| `images/vila.png` | Existing VILA figure from this repository; [project page](https://joon-stack.github.io/VILA/) |
| `images/sparse-planning.png` | [Sparse Imagination planning overview](https://nikriz1.github.io/sparse_imagination/) |
| `images/ocwm.png` | Existing object-centric world-model diagram from this repository; [paper](https://arxiv.org/abs/2503.06170) |

Publication summaries follow the linked papers or project pages. The object-centric paper’s coauthor is Soonwoo Cha, as listed in its arXiv record; the homepage now corrects the previously expanded name.
