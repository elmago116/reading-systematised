---
title: cultarc / cultarc-collection-explorer
source: https://gitlab.com/cultarc/cultarc-collection-explorer
author:
  - Darredondo
published: 2026-10-03
created: 2026-10-15
description: An open web explorer for cultural archive collections, using BERTopic embedding maps as point clouds or images, showing what the model leaves out alongside what it groups.
tags:
  - op/doc/projects
  - op/doc/similar
  - bibliometrics
---
[**README.md**](https://gitlab.com/cultarc/cultarc-collection-explorer/-/blob/main/README.md?ref_type=heads)

## cultarc-collection-explorer

**CULT/ARC Digital Archive Collection Explorer (embedding-based topic maps)**

An open web interface for exploring records of cultural digital archives as interactive 2D embedding maps, as a point cloud coloured by topic, or as the images themselves, using topic structures extracted with [BERTopic](https://maartengr.github.io/BERTopic/).

Part of the [CULT/ARC project](https://www.upf.edu/web/area-tallers/projectes/-/asset_publisher/1Tpg1ZEsssFR/content/cultur-arc/maximized), developed at the [EnResidència 2025–2026 programme](https://www.upf.edu/web/area-tallers/en-residencia) by Universitat Pompeu Fabra, Barcelona.

---

[![CULT/ARC Explorer demo capture, mapping topics of Filmoteca de Catalunya's image repository](https://gitlab.com/cultarc/cultarc-collection-explorer/-/raw/main/demo/cultarc_demo_01.gif)](https://gitlab.com/cultarc/cultarc-collection-explorer/-/raw/main/demo/cultarc_demo_01.gif)

## About

This explorer is one of a series of open-source prototypes developed within **CULT/ARC**, a transdisciplinary applied research project exploring how participatory design and AI-driven pipelines with open models can help transform static digital archives into more accessible, interpretable, and discovery-driven platforms.

The central concern of this prototype is enabling both distant and close readings of digitized cultural collections: surfacing semantic structures latent in archival metadata (such as titles or descriptions), and making them legible and navigable for researchers, archive technicians, and curious general audiences alike.

Where the companion notebook, [cultarc-topic-modeller](https://gitlab.com/cultarc/cultarc-topic-modeller), handles the modelling side (cleaning, embedding, clustering, and topic extraction), this repository is the **interface side**: a dataset-agnostic web explorer that loads any collection preprocessed with that pipeline and turns it into a navigable map.

---

## What it does

Given a preprocessed collection (see [Bring your own collection](#bring-your-own-collection)), the explorer provides:

- **Two synchronized views of the same map** — a fast GPU point cloud ([cosmos.gl](https://cosmos.gl/) v3) and an image view of the records' own images (PixiJS v8), sharing one canonical coordinate space so positions match across views.
- **Topic structure at a glance** — cluster labels floating over the map, sized by topic weight, plus a colour-coded legend.
- **Filtering and selection** — click a topic label or legend entry to focus a topic (shift-click to combine several); non-selected points, labels, and legend entries de-emphasize together.
- **Keyword search** — scoped to the active topic filter, highlighting hits on the map.
- **Close reading** — hover tooltips (title, date, topic, provenance, description), a documents panel with top / random / selected tabs, and a full-screen image modal linking back to the source catalogue record.
- **Honest about the model** — records the clustering left unassigned stay on the map as a toggleable background layer, showing the topics they lean toward (weak leans marked as weak); a histogram shows how firmly the model holds the selected topics' records; and an *About this graph* panel discloses the pipeline, what the map leaves out, and its limits.
- **Considered interaction details** — points fly from off-screen into their embedding positions on load, eased trackpad/wheel zooming, spacebar-to-pan, drag and zoom that work even when starting over a label, and native touch/pen support.
- **Performance by design** — a lazy, viewport-culled, two-resolution image pipeline (tiny sprites for the map, on-demand thumbnails for close-ups), drawing images only for the records each topic holds most firmly (the rest on hover), keeps GPU memory bounded on collections of tens of thousands of records.

The code is documented in place: each module opens with a comment describing its role, and [`src/lib/data/processed.ts`](https://gitlab.com/cultarc/cultarc-collection-explorer/-/blob/main/src/lib/data/processed.ts), where the dataset becomes everything the interface draws, is a good place to start reading.

---

## Bring your own collection

The explorer is **collection-agnostic**: it renders whatever dataset you place at `src/sentences.ts`, in the row format produced by the companion pipeline:

1. **Preprocess your archive** with [cultarc-topic-modeller](https://gitlab.com/cultarc/cultarc-topic-modeller) — a notebook that cleans CSV archive records, generates sentence embeddings with open models, reduces them to 2D (UMAP), clusters them (HDBSCAN), and extracts topics (BERTopic).
2. **Run the last-mile notebook** [`notebooks/last_mile_preprocessing.ipynb`](https://gitlab.com/cultarc/cultarc-collection-explorer/-/blob/main/notebooks/last_mile_preprocessing.ipynb) on the pipeline's export (`data_documents_topics_2D_*.csv`, placed in `data/`). It validates the export and writes `src/sentences.ts` (documents, topic centroids, soft-membership candidates and provenance), so the browser never parses CSV. The row format is documented in [`src/sentences.template.ts`](https://gitlab.com/cultarc/cultarc-collection-explorer/-/blob/main/src/sentences.template.ts).
3. **Optionally add imagery** — two sizes per record, named by the record's `archive_id`: tiny map sprites and larger thumbnails. Conventions are documented in [`public/imgs/sprites/sprites.md`](https://gitlab.com/cultarc/cultarc-collection-explorer/-/blob/main/public/imgs/sprites/sprites.md) and [`public/imgs/thumbs/thumbs.md`](https://gitlab.com/cultarc/cultarc-collection-explorer/-/blob/main/public/imgs/thumbs/thumbs.md). Records without images degrade gracefully to topic-coloured points. The `.gitignore` keeps everything under `public/imgs/` out of version control, apart from those notes.

**About the dataset.** The repository ships the notebook ran with metadata of the [Filmoteca de Catalunya](https://repositori.filmoteca.cat/) photograph collection (September 2026 export), which is not included in the repo. Datasets already processed in the related CULT/ARC Topic Modeller notebooks should be placed for in `data/` for populating the provenance card (“About this graph”) and generate a new `src/sentences.ts`, so the app runs out of the box. **Images are not included and optional**, as the interface automatically detects if image sprites are available and disables the “Image View” if not found. Sample datasets built from openly licensed sources (such as [Europeana](https://www.europeana.eu/)) will be added later, along with linked examples.

A small synthetic dataset in the same format, [`src/sentences.template.ts`](https://gitlab.com/cultarc/cultarc-collection-explorer/-/blob/main/src/sentences.template.ts), documents the row format and is a starting point for other collections.

---

## Motivation and research context

This prototype grows out of ongoing applied research on how participatory design and representation learning can support meaningful interaction with large-scale cultural and historical archives. It currently draws on case studies from the [Filmoteca de Catalunya](https://repositori.filmoteca.cat/), [Europeana](https://www.europeana.eu/), and personal artist archives, such as the [Arxiu Muntadas](https://arxiumuntadas.org/database/) by multidisciplinary artist Antoni Muntadas.

A persistent challenge in working with digitized heritage collections is that rich metadata is often underexplored: buried in flat search interfaces, difficult to browse at scale, and rarely surfaced in ways that reveal thematic patterns or unexpected connections. Mapping collections over semantic embeddings is one methodological approach to begin opening up these latent structures not as a replacement for human annotation, but as a tool for exploration, hypothesis generation, and interface design.

The implementation deliberately targets **accessible environments**: it is a static site with no backend, deployable to any static host, and its rendering strategies (GPU point clouds, lazy two-resolution imagery) are designed so that collections of tens of thousands of records remain explorable on ordinary hardware.

---

## Built with

| Package | Role |
| --- | --- |
| [`svelte`](https://svelte.dev/) 4 | UI components and reactive stores |
| [`vite`](https://vitejs.dev/) 5 | Dev server and bundler |
| [`typescript`](https://www.typescriptlang.org/) | Types throughout |
| [`@cosmos.gl/graph`](https://cosmos.gl/) 3.1 | GPU point-cloud view (luma.gl / WebGL 2), GPU transitions, highlight/outline selection |
| [`pixi.js`](https://pixijs.com/) 8 | Image-sprite view with custom pan/zoom and lazy texture loading |

---

## Requirements

- **Node.js ≥ 18**
- **pnpm 10**, pinned in `package.json` (`packageManager`, read by Corepack). The repo ships a `pnpm-lock.yaml`; npm/yarn will work but won't reuse the lockfile.

---

## Quickstart

```shell
# 1. Clone this repository
git clone <repo-url> && cd cultarc-collection-explorer

# 2. Install dependencies
pnpm install

# 3. Run the dev server (opens the included collection)
pnpm dev
```

For a production build: `pnpm build` (output in `dist/`), previewable with `pnpm preview`.

To try the synthetic sample instead, copy `src/sentences.template.ts` over `src/sentences.ts` (17 records, 3 topics). To load another collection, run `notebooks/last_mile_preprocessing.ipynb` on its pipeline export. Imagery is optional and local: see the notes in `public/imgs/*/`.

---

## Deploy

The repository is ready to deploy on [Netlify](https://www.netlify.com/) from GitHub. [`netlify.toml`](https://gitlab.com/cultarc/cultarc-collection-explorer/-/blob/main/netlify.toml) sets the build (`pnpm build`, published from `dist/`), the Node.js version, and the dev server that Netlify's Preview Server runs. Once the repository is connected, the default branch deploys to production and every pull request gets a Deploy Preview.

Deploy through git-based builds only. The images are never in the repository, so those builds never contain them; a `dist/` built locally, on the other hand, includes whatever sits in `public/imgs/`.

---

## CULT/ARC project

**CULT/ARC** is an interdisciplinary framework for ideation and prototyping aimed at helping museums and cultural institutions reimagine their digital archives. It combines open technical prototypes with a facilitation playbook, aimed to support structured participatory design sessions, to catalyze collaboration between archival, curatorial, and technical stakeholders.

The project proposes a framework organized around three components: refining search strategies to make them more intuitive and semantically rich; expanding exploratory visualization of large digitized collections; and designing more personalized, discovery-driven user experiences. Together, these aim to transform static archives into dynamic and participatory platforms.

CULT/ARC was initiated as a final project in the *Digital Museography and Online Cultural Activities* course of the Master's in Digital Culture and Emerging Media at UPF by Diego Arredondo and Farah Darwish, and is currently in its incubation phase within the [EnResidència 2025–2026 programme](https://www.upf.edu/web/area-tallers/projectes/-/asset_publisher/1Tpg1ZEsssFR/content/cultur-arc/maximized).

---

## Citation and credit

Interface and repository created and maintained by **Diego Arredondo Ortiz**

This code was implemented and presented, with the Filmoteca de Catalunya's photograph repository as case study, at the following academic poster sessions:

- Arredondo-Ortiz, D. (2026). CULT/ARC. Explainable representation learning and interactive visualization for cultural archives. [Workshop on AI/ML Applied Methods in Computational Social Sciences and Humanities Research](https://cssh-workshop.es/), Barcelona Supercomputing Center.
- Arredondo-Ortiz, D. (2026). From distant viewing to close reading: embedding visualization and retrieval for meaningful exploration of cultural archives. [6th IAPR TC10/TC11 Summer School Next-Gen Document Understanding](https://ssdag.cvc.uab.es/). Computer Vision Center, Unversitat Autònoma de Barcelona.

If you use or adapt this explorer in your work, please cite:

```md
Arredondo-Ortiz, D. (2026). cultarc-collection-explorer [Software]. CULT/ARC Project, EnResidència 2025–2026, Universitat Pompeu Fabra. https://gitlab.com/cultarc/cultarc-collection-explorer
```

---

## Acknowledgments

Developed within the CULT/ARC Project at the [En Residència 2025–2026 programme](https://www.upf.edu/web/area-tallers/projectes-tots/-/asset_publisher/67I8tXJLTWkv/content/cultur-arc/maximized), at Universitat Pompeu Fabra, Barcelona, with the support of the UPF En Residència and ARSENAL team: Teresa Roig, Andrea Olmedo and Pablo Cavero. Thanks to the project's mentors, Javier Pantoja (Barcelona Supercomputing Center), Víctor Fancelli (Open Resource Center Karlsruhe), and Carlos Castillo (ICREA Research Professor, UPF). Special thanks to Anna Fors and Miquel Àngel Pintanel at the Filmoteca de Catalunya, and to Andrea Nacach at the Arxiu Muntadas, for facilitating access to the datasets used as case studies. Farah Darwish is the co-author of the CULT/ARC model, during its initial stages, as a transdisciplinary model for ideation and prototyping aimed at helping museums and cultural institutions improve their digital archives.

---

## License

This project is released under the [MIT License](https://gitlab.com/cultarc/cultarc-collection-explorer/-/blob/main/LICENSE).