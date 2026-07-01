# Prompt for adding a new project

Use this prompt when asking an LLM to add a new project to the website.

I need you to add a new project to my Jekyll academic website.

Use the existing academic project style exactly.

Do not invent a new layout.

The canonical template is:

projects/credal-rate-distortion.html

Clone its structure and CSS classes.

The new project page must use:

- project-website
- project-hero
- project-hero-title
- project-meta-block
- project-meta-label
- project-owner
- project-hero-paper-authors
- project-affiliations
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
- custom page-specific wrappers

Do not add fake logos.

Only add logos if they are real and already available in the repository.

Do not put a large thumbnail image inside the detail page unless the template already does that.

For the projects listing page, edit projects.html by cloning one existing project-card.

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

Use MathJax syntax.

Inline math:

$...$

Display math:

\[
...
\]

Do not include LaTeX preamble commands such as documentclass, usepackage, begin document, maketitle, tableofcontents, or end document.

Before committing, run:

rm -rf _site .jekyll-cache
bundle exec jekyll build
bundle exec jekyll serve

Check locally before pushing.
