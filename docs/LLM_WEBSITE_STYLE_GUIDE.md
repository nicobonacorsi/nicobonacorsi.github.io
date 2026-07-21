# Nicolò Bonacorsi Website — Permanent LLM Style Guide

This file defines the permanent rules for editing this Jekyll academic website.

The goal is not to create something similar. The goal is to preserve the exact academic graphic style already used on the website.

## Absolute rule

Do not invent a new layout.

Do not invent new CSS classes.

Do not replace the current academic style with a generic Jekyll, markdown, or custom layout.

When adding a new project, publication, blog post, image, PDF, or page, first inspect the existing file that already has the correct style, then clone its structure and replace only the content.

## Canonical project template

The canonical project detail template is:

projects/credal-rate-distortion.html

Before creating a new project page, inspect this file and reuse its real classes.

The real project-detail classes currently used by the site are:

- project-website
- project-hero
- project-hero-title
- project-meta-block
- project-meta-label
- project-owner
- project-hero-paper-authors
- project-affiliations
- project-logos
- project-logo-card
- project-logo
- project-venue
- project-buttons
- project-button
- project-layout
- project-toc
- project-toc-title
- project-main
- project-section
- project-figure
- back-to-projects

These are the correct classes.

Do not use these invented or wrong classes for project pages:

- project-detail
- project-title
- project-shell
- project-page
- project-hero-content
- svd-project
- custom one-off wrappers

unless they already exist in the canonical template.

## Correct project page structure

A project detail page must follow the same skeleton as projects/credal-rate-distortion.html:

1. YAML front matter.
2. The same style block as the canonical project page.
3. section with class project-website.
4. div with class project-hero.
5. h1 with class project-hero-title.
6. metadata blocks using project-meta-block and project-meta-label.
7. project-owner when relevant.
8. project-hero-paper-authors when relevant.
9. project-affiliations.
10. project-logos only if real logos exist.
11. project-venue.
12. project-buttons containing project-button links.
13. div with class project-layout.
14. aside with class project-toc.
15. main with class project-main.
16. repeated section blocks with class project-section.

The table of contents must stay on the left.

The content must stay on the right.

The page must visually match Credal Rate-Distortion Theory.

## Project hero rules

Use project-hero-title for the main title.

Do not use another title class.

Do not add a large thumbnail image inside the project detail page unless the canonical page has one.

Project thumbnails belong in projects.html.

The hero must stay centered.

The metadata must use project-meta-block and project-meta-label.

## Logos and affiliations

Do not invent logos.

Do not create fake university logos.

Only use real logos that exist in the repository.

If a real logo is not available, use text-only affiliation.

If a logo is added, it must use:

- project-logos
- project-logo-card
- project-logo

Do not use random image sizes or random logo containers.

## Project buttons

Buttons must use:

- project-buttons
- project-button

Good button targets are:

- PDF
- Code
- Paper
- arXiv
- #mathematical-formulation
- #results
- #face-recognition
- #interactive-demo
- #bibtex

Do not create new button styling.

If adding a PDF to a project, place the PDF in:

files/

Use a clean filename, for example:

files/Face_Recognition_SVD_Project.pdf

Use this href format:

{{ '/files/Face_Recognition_SVD_Project.pdf' | relative_url }}

## Main project content sections

Use this section pattern:

<section id="abstract" class="project-section">
  <h2>Abstract</h2>
  <p>Text here.</p>
</section>

Every main section must use:

class="project-section"

Recommended sections:

- Abstract
- Research question
- Key idea
- Mathematical formulation
- Results
- Conclusions
- BibTeX when applicable

For mathematical projects, also use domain-specific sections such as:

- Crime data PCA
- Regression model
- SVD-based face recognition
- Rank-dependent accuracy
- Interactive demo
- Images and video

## Math rules

Inline math uses dollar signs.

Example:

$R^2_{adjusted}$

Display math uses MathJax display syntax.

Example:

\[
A = U\Sigma V^T.
\]

Numbered equations use equation environments.

Example:

\begin{equation}
R = \frac{Z^T Z}{n-1}.
\label{eq:correlation}
\end{equation}

Equation references must be written as:

Equation $\eqref{eq:correlation}$

Do not include raw LaTeX document commands in website pages:

- documentclass
- usepackage
- begin document
- maketitle
- tableofcontents
- end document

Those belong to PDF/LaTeX documents, not website pages.

## Projects listing page

The canonical projects listing page is:

projects.html

When adding a new project card:

1. Do not rewrite the whole page.
2. Do not modify existing cards.
3. Remove any previous broken card for the same project.
4. Clone an existing article with class project-card.
5. Keep the exact same class names.
6. Replace only the link, image, title, metadata, tags, question, key idea, and results.
7. Make sure the image src points to a real file.
8. Make sure the card link points to the correct project page.
9. Make sure the card hover animation is preserved.
10. Make sure author/name weight, tag shapes, and spacing match existing cards.

Important classes for project cards:

- project-card
- project-thumb
- project-card-title
- project-card-meta
- project-tags
- project-tag

Never mix content from an old project into a new card.

If cloning Credal or Collatz, replace every old title, link, image, tag, question, key idea, result, and project-specific text.

## Project thumbnail rule

If a card image is broken, check both:

1. the img src in projects.html;
2. the physical file in images/publications.

A safe src format for root GitHub Pages is:

/images/publications/file-name.svg

or, if the existing card uses Liquid paths, preserve the existing style.

After building, verify the file exists in:

_site/images/publications/file-name.svg

## Project tags and topic counts

The topic counts in the Projects sidebar must be regenerated whenever a new project card is added.

The counts must come from each project-card data-topics attribute.

Every project card must have:

data-topics="topic-slug another-topic-slug"

Every visible project tag button must use the same slug.

Every filter button must include both:

data-topic-filter="topic-slug"
data-filter="topic-slug"

The All topics count must equal the number of project-card articles.

A new project with tags must update:

- data-topics on the article;
- visible project-tag buttons;
- sidebar filter buttons;
- sidebar counts.

Do not hardcode wrong counts.

Do not leave a topic with count 1 if there are now 2 projects with that tag.

## Publications page

The canonical publications listing page is:

publications.html

Do not change:

- publication-card image size;
- hover animation;
- author logos;
- topic filters;
- year filters;
- publication card spacing;

unless explicitly requested.

Publication pages and cards should preserve:

- title;
- authors;
- author logos when available;
- venue;
- status;
- topics;
- buttons for PDF, Paper, arXiv, Code, Project when available.

## Home page

The home page is:

index.html

Do not modify it unless explicitly requested.

Preserve:

- portrait image;
- academic bio;
- icon links for CV, Email, Scholar, GitHub, LinkedIn.

If the icon links disappear, restore them.

## CV page

The CV page is:

cv.html

The downloadable CV should live in:

files/

Do not break the CV download button.

## Blog system

The site has a blog landing page and two blog sections:

- blog/index.html
- blog/scientific.html
- blog/personal.html

Do not create random standalone HTML blog pages.

Blog posts should be markdown files inside _posts.

## Scientific blog rules

Scientific blog posts must use category scientific.

Recommended front matter:

layout: post
title: "Post title"
date: YYYY-MM-DD
categories: [scientific]
scientific_type: "Research Notes"
tags: [Probability, Stochastic Control]
math: true

Allowed scientific_type values:

- Research Notes
- Course Notes
- Discovery Ideas

The scientific blog filters by:

- scientific_type;
- year;
- tags/topics.

When adding a scientific post, make sure the tags are meaningful and consistent with existing tag names.

If editing blog/scientific.html, preserve the existing card style, filters, and counts.

## Personal blog rules

Personal blog posts must use category personal.

Recommended front matter:

layout: post
title: "Post title"
date: YYYY-MM-DD
categories: [personal]
city: "New York"
tags: [Photography, Travel, Friends]

The personal blog filters by:

- year;
- city;
- tags/topics.

If editing blog/personal.html, preserve the existing card style, filters, and counts.

Do not mix personal posts into the scientific blog.

Do not mix scientific posts into the personal blog.

## Blog tag/count rules

Whenever a blog listing page has filters and counts, the counts must correspond to the posts actually shown on that page.

Do not hardcode outdated counts.

Do not create a new tag button without making sure filtering works.

Do not rename a tag in one place and forget to update the filter slug.

For scientific posts, filters should read categories scientific and scientific_type.

For personal posts, filters should read categories personal and city when available.

## Upload and media rules

Images for general use go in:

images/uploads/

Project/publication thumbnails usually go in:

images/publications/

Videos go in:

videos/uploads/

Interactive HTML exports go in:

assets/uploads/

PDFs and downloadable files go in:

files/

To embed an image:

<img src="{{ '/images/uploads/file.png' | relative_url }}" alt="Description">

To embed a video:

<video controls src="{{ '/videos/uploads/file.mp4' | relative_url }}"></video>

To embed an interactive HTML export:

<iframe src="{{ '/assets/uploads/file.html' | relative_url }}" width="100%" height="560"></iframe>

Do not assume Python can run on GitHub Pages.

Python outputs must be exported as PNG, GIF, MP4, WebM, or HTML and then embedded.

## Global files

Do not casually edit:

- _layouts/default.html
- _includes/head.html
- _includes/header.html
- _includes/footer.html
- _includes/mathjax.html

Only edit global files if the user explicitly asks for global layout changes.

## Safe workflow for adding a new project

1. Create backups in _dev_backups.
2. Clone projects/credal-rate-distortion.html.
3. Replace front matter.
4. Replace hero.
5. Replace table of contents.
6. Replace main content.
7. Add PDF button if a PDF exists.
8. Add one clean card to projects.html by cloning an existing project-card.
9. Recalculate sidebar topic counts.
10. Verify images exist.
11. Verify PDFs exist.
12. Run local Jekyll build.
13. Check locally before committing.
14. Commit only if the rendering is correct.

## Anti-disaster checks

After building, front matter must not appear in the generated page:

grep -R "layout: default" _site/projects/PROJECT-SLUG/ && echo "BROKEN FRONT MATTER" || echo "OK front matter"

Check that the new page does not accidentally contain old project names:

grep -n "Credal\|Collatz" projects/PROJECT-SLUG.html

Check that the project image exists:

test -s images/publications/IMAGE.svg && echo "OK image exists"

Check that it was copied into the built site:

test -s _site/images/publications/IMAGE.svg && echo "OK built image exists"

Check that the PDF exists:

test -s files/FILE.pdf && echo "OK PDF exists"

Check that it was copied into the built site:

test -s _site/files/FILE.pdf && echo "OK built PDF exists"

## Standard LLM instruction

Use the existing academic project style exactly. Do not create a new layout. Clone the structure and CSS classes from projects/credal-rate-distortion.html. Preserve project-website, project-hero, project-hero-title, project-layout, project-toc, project-main, and project-section. Add the new content using the same structure. Then add one card to projects.html by cloning an existing project-card and replacing only the content. Recalculate topic counts from data-topics. Verify images and PDFs exist. Do not modify global layout files.


## Quantitative research project pages

The public-data quant research bundle contains two independent projects and must be represented as two separate cards and two separate detail pages:

- Bootstrap-Calibrated Distributionally Robust Allocation
- Maturity-Safe Distributional Volatility Forecasting and Risk Control

Both pages must clone `projects/credal-rate-distortion.html` and preserve its exact style block and real classes. Do not merge them into one generic portfolio page.

Quant pages must preserve:
- development, validation, and confirmation chronology;
- mathematical definitions and optimization/forecasting equations;
- benchmarks, inference, negative results, and limitations;
- real result figures and a downloadable code/data bundle;
- exact `project-card`, thumbnail hover, topic chips, filters, and topic counts.

Do not claim alpha when the reported number is CAGR. Do not claim material dominance over Ledoit–Wolf. Do not claim the QLIKE improvement is statistically significant. Do not call the interlaced upper bound a finite-sample conformal guarantee.


## Full-paper project content rule

When a project is based on a supplied paper or research report, the website page must not be reduced to a short summary unless the user explicitly asks for an abbreviated page.

For the two July 2026 quantitative research projects, preserve all paper-level material relevant to each study:
- research design and chronology;
- data and accounting conventions;
- every mathematical definition and numbered equation;
- optimization or forecasting construction;
- complete benchmark tables;
- confidence intervals, HAC tests, coverage diagnostics, and sensitivity results;
- all relevant figures and captions;
- reproducibility and audit controls;
- limitations, negative results, scope, and research extensions;
- selected configuration tables and public-data sources;
- buttons for the full report PDF and the complete code/data bundle.

Do not omit unfavorable benchmark comparisons. Do not turn CAGR into alpha. Do not describe the small Ledoit–Wolf difference as economically material. Do not describe the QLIKE difference as statistically significant. Do not describe interlaced calibration as a finite-sample conformal guarantee.


## Downloadable code-package rule

When publishing source code for a project, create a clean code-only archive unless the user explicitly requests a complete reproducibility package.

The clean code archive may contain:
- source `.py` files;
- package `__init__.py` files;
- execution scripts;
- tests;
- `requirements.txt`.

Do not include:
- prompt files;
- LLM instructions;
- reviewer prompts;
- private notes;
- CV bullets;
- interview-defense documents;
- raw datasets;
- generated results;
- figures;
- research drafts.

Use a project button labeled `Code`, not `Code & Data`, when the linked archive contains code only.

## Home-page hyperlink rule

In the Home biography:
- link research topics to the corresponding English Wikipedia article;
- link professor names to their official university profile;
- open external links in a new tab with `target="_blank"` and `rel="noopener"`;
- preserve the existing biography text, typography, portrait, and button layout;
- use the existing subtle inline-link style rather than pill buttons inside prose.
