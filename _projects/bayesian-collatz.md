---
layout: project
title: "Bayesian Modeling of Collatz Stopping Times"
date: 2026-03-01
author: "Nicolò Bonacorsi"
project_of:
  - name: "Nicolò Bonacorsi"
    url: "/"
    affiliation: "Columbia University"
    logo: "/images/logos/columbia-crown.webp"
paper_authors:
  - name: "Nicolò Bonacorsi"
    url: "/"
    affiliation: "Columbia University"
    logo: "/images/logos/columbia-crown.webp"
  - name: "Matteo Bordoni"
    url: "https://www.linkedin.com/in/matteo-bordoni-4b710a206"
    affiliation: "Columbia University"
    logo: "/images/logos/columbia-crown.webp"
affiliations:
  - name: "Columbia University"
    logo: "/images/logos/columbia-crown.webp"
topics: ["Bayesian Inference", "Probabilistic Machine Learning", "Number Theory", "Monte Carlo", "Heavy Tails"]
image: "/images/publications/collatz.svg"
publication_url: "/publications/bayesian-collatz-stopping-times/"
arxiv_url: "https://arxiv.org/abs/2603.04479"
paper_url: "https://arxiv.org/abs/2603.04479"
abstract: "A probabilistic machine-learning study of Collatz total stopping times using Bayesian Negative Binomial regression and stochastic odd-block generative models."
question: "Can Collatz total stopping times be modeled probabilistically while preserving arithmetic structure and heavy-tail behavior?"
key_idea: "Use Bayesian regression for predictive performance and odd-block stochastic generators for a mechanistic explanation of modular effects and tail behavior."
results: "The regression model gives strong held-out prediction, while the odd-block models explain overdispersion, modular heterogeneity, and heavy-tail mechanisms."
interactive_demo: "Interactive plots or Python-generated animations can be inserted here after uploading them as HTML, GIF, MP4, or WebM."
media_notes: "Simulation figures, histograms, posterior predictive checks, and animated trajectories can be embedded in this section."
math: true
bibtex: |
  @misc{bonacorsi2026collatz,
    title={Bayesian Modeling of Collatz Stopping Times: A Probabilistic Machine Learning Perspective},
    author={Bonacorsi, Nicolò and Bordoni, Matteo},
    year={2026},
    eprint={2603.04479},
    archivePrefix={arXiv}
  }
---

For the Collatz map,

\begin{equation}
T(n)
=
\begin{cases}
n/2, & n \equiv 0 \pmod 2,\\
3n+1, & n \equiv 1 \pmod 2.
\end{cases}
\label{eq:collatz-project}
\end{equation}

Equation $\eqref{eq:collatz-project}$ defines the deterministic dynamics. The statistical model studies the empirical distribution of total stopping times and the stochastic structure induced by the odd-block valuation $K = v_2(3m+1)$.
