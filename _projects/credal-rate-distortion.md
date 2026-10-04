---
layout: project
title: "Credal Rate–Distortion Theory"
date: 2026-07-01
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
  - name: "Michele Caprio"
    url: "https://research.manchester.ac.uk/en/persons/michele-caprio/"
    affiliation: "University of Manchester"
    logo: "/images/logos/manchester-official.png"
  - name: "Francesca Meneghello"
    url: "https://coe.northeastern.edu/people/meneghello-francesca/"
    affiliation: "Northeastern University"
    logo: "/images/logos/northeastern-monogram.png"
  - name: "Francesco Restuccia"
    url: "https://coe.northeastern.edu/people/restuccia-francesco/"
    affiliation: "Northeastern University"
    logo: "/images/logos/northeastern-monogram.png"
affiliations:
  - name: "Columbia University"
    logo: "/images/logos/columbia-crown.webp"
  - name: "University of Manchester"
    logo: "/images/logos/manchester-official.png"
  - name: "Northeastern University"
    logo: "/images/logos/northeastern-monogram.png"
topics: ["Information Theory", "Credal Uncertainty", "Rate–Distortion", "Uncertainty Quantification", "Robust Compression"]
image: "/images/publications/credal.svg"
publication_url: "/publications/credal-rate-distortion-theory/"
pdf_url: "https://mentis.info/wp-content/uploads/2026/05/Credal_ITW_2026.pdf"
abstract: "A robust rate–distortion framework for compression under credal uncertainty, where the source law is not known exactly but belongs to a set of plausible distributions."
question: "How should rate–distortion theory change when the source law is not known exactly, but belongs to a credal set?"
key_idea: "Replace single-law compression by a robust formulation in which distortion constraints must hold uniformly over a family of plausible source distributions."
results: "The project studies reverse-inclusion phenomena, robust operational limits, finite-window behavior, and graph-theoretic compression regimes."
interactive_demo: "Interactive demos and simulations can be inserted here with iframes, Plotly HTML exports, videos, or Python-generated animations."
media_notes: "Figures, animations, and videos can be uploaded through the site editor and embedded directly in this section."
math: true
bibtex: |
  @misc{bonacorsi2026credal,
    title={Credal Rate--Distortion Theory},
    author={Bonacorsi, Nicolò and Caprio, Michele and Meneghello, Francesca and Restuccia, Francesco},
    year={2026}
  }
---

A schematic robust rate--distortion problem can be written as

\begin{equation}
R_{\mathcal P}(D)
=
\inf_{P_{\widehat X|X}}
I_{\mathcal P}(X;\widehat X)
\quad
\text{subject to}
\quad
\sup_{P \in \mathcal P}
\mathbb E_{P P_{\widehat X|X}}
[d(X,\widehat X)]
\le D.
\label{eq:credal-project}
\end{equation}

Equation $\eqref{eq:credal-project}$ highlights the main difference from the classical formulation: the distortion constraint is imposed uniformly over the whole credal set.
