# Nicolò Bonacorsi Website — LLM Style Guide

This file is the permanent instruction file for editing the website.

The goal is not to create something similar. The goal is to preserve the exact academic graphic style already used on the website.

## Core rule

When adding a new project, clone the existing academic project style.

The canonical project template is:

projects/credal-rate-distortion.html

Do not invent a new layout.

Do not invent new CSS classes.

Do not use a different visual system.

Do not replace the academic pages style with a generic Jekyll page, markdown page, or custom layout.

## Correct project page classes

A project detail page must use the same class system as the Credal project page.

The important classes are:

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

These classes define the exact academic-page style.

## Wrong classes

Do not use these unless they already exist in the canonical template:

- project-detail
- project-title
- project-shell
- project-page
- project-hero-content
- svd-project
- custom wrapper classes invented for one page

These create a different page style and are not allowed.

## Correct project page structure

Every project page must follow this structure:

1. YAML front matter
2. style block copied from the canonical project page
3. section with class project-website
4. div with class project-hero
5. h1 with class project-hero-title
6. metadata blocks using project-meta-block and project-meta-label
7. optional affiliations and logos only if real
8. div with class project-buttons
9. div with class project-layout
10. aside with class project-toc
11. main with class project-main
12. sections with class project-section

The table of contents must stay on the left.

The content must stay on the right.

## Hero rules

The project title must use:

project-hero-title

The hero must stay centered.

The title must use the same large academic style as the Credal Rate-Distortion project.

Do not add a large internal thumbnail image inside the project page unless the existing canonical page uses one.

Project thumbnails belong in projects.html, not inside the detail page.

## Logos and affiliations

Do not invent logos.

Do not create fake university logos.

Only use logos that already exist in the repository and are correct.

If a real logo is not available, use text-only affiliation.

## Buttons

Buttons must use:

project-buttons
project-button

Good button targets are internal anchors such as:

#mathematical-formulation
#results
#face-recognition
#interactive-demo
#bibtex

Do not create new button styling.

## Content sections

Use this section format:

<section id="abstract" class="project-section">
  <h2>Abstract</h2>
  <p>Text here.</p>
</section>

Every main content section must use:

class="project-section"

Preferred section titles:

- Abstract
- Research question
- Key idea
- Mathematical formulation
- Results
- Conclusions
- BibTeX

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

## Do not include raw LaTeX document commands

Website pages must not include:

- \documentclass
- \usepackage
- \begin{document}
- \maketitle
- \tableofcontents
- \end{document}

Those commands belong to PDF/LaTeX documents, not website pages.

## Projects listing page

The canonical projects listing page is:

projects.html

When adding a new project card:

1. Do not rewrite the whole file.
2. Do not modify the existing cards.
3. Remove any previous broken card for the same project.
4. Clone an existing article with class project-card.
5. Keep the exact same classes.
6. Replace only the link, image, title, metadata, tags, question, key idea, and results.
7. Make sure the card link points to the correct project page.

Never mix old project content into a new card.

If cloning a Credal or Collatz card, replace every old title, old link, old question, old key idea, old result, old tag, and old image.

## Publications page

The canonical publications listing page is:

publications.html

Do not change:

- publication card image size
- hover animation
- author logos
- topic filters
- year filters

unless explicitly requested.

## Home page

The home page is:

index.html

Do not modify it unless explicitly requested.

Preserve:

- portrait image
- academic bio
- icon links for CV, Email, Scholar, GitHub, LinkedIn

## Global files

Do not casually edit these files:

- _layouts/default.html
- _includes/head.html
- _includes/header.html
- _includes/footer.html
- _includes/mathjax.html

Only edit global files if the user explicitly asks for a global layout change.

## Safe workflow for adding a new project

1. Create backups in _dev_backups.
2. Use projects/credal-rate-distortion.html as the template.
3. Replace the front matter.
4. Replace the hero content.
5. Replace the table of contents.
6. Replace the main project content.
7. Add one clean card to projects.html.
8. Run a local Jekyll build.
9. Check the page locally before committing.
10. Commit only if the rendering is correct.

## Anti-disaster checks

After building the site, front matter must not appear in the generated page.

Use this check:

grep -R "layout: default" _site/projects/PROJECT-SLUG/ && echo "BROKEN FRONT MATTER" || echo "OK front matter"

Check that the new page does not accidentally contain text from an old project:

grep -n "Credal\|Collatz" projects/PROJECT-SLUG.html

If unrelated old project text appears, fix it before committing.

## Standard LLM instruction

When asking an LLM to add a project, say:

Use the existing academic project style exactly. Do not create a new layout. Clone the structure and CSS classes from projects/credal-rate-distortion.html. Preserve the visual system: centered hero, project-hero-title, metadata blocks, black pill buttons, left project-toc, right project-main, and repeated project-section blocks. Add the new project content using the same structure. Then add one card to projects.html by cloning an existing project-card and replacing only the content. Do not modify global layout files.
