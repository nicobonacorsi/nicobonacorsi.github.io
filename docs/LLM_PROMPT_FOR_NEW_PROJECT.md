# Prompt for adding a new project

Add a new project to my Jekyll academic website.

Use the existing academic project style exactly.

Do not invent a new layout.

The canonical template is:

projects/credal-rate-distortion.html

Clone its structure and CSS classes.

The project detail page must use the real classes already used by the template:

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

Do not use:

- project-detail
- project-page
- project-shell
- custom wrappers

Do not add fake logos.

Only use real logos that already exist in the repository.

Do not insert a large project thumbnail inside the detail page unless the canonical template does that.

PDFs must go in files/.

Project thumbnails must go in images/publications/.

For the Projects listing page, edit projects.html by cloning one existing project-card.

Keep the exact same classes and hover animation.

Replace only:

- link
- image
- title
- metadata
- tags
- question
- key idea
- results

After adding the card, recalculate the topic counts in the sidebar from all project-card data-topics attributes.

Every filter button must include both data-topic-filter and data-filter.

For blog posts, use _posts and the correct category.

Scientific posts use categories: [scientific] and scientific_type.

Personal posts use categories: [personal] and city when relevant.

Use MathJax syntax for math.

Do not include LaTeX preamble commands.

Before committing, run:

rm -rf _site .jekyll-cache
bundle exec jekyll build
bundle exec jekyll serve

Check locally before pushing.
