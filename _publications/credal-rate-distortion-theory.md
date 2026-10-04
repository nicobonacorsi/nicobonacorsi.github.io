---
layout: publication
title: "Credal Rate–Distortion Theory"
date: 2026-05-01
authors: ["Nicolò Bonacorsi", "Michele Caprio", "Francesca Meneghello", "Francesco Restuccia"]
author_items:
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
venue: "IEEE ITW 2026"
status: "Submitted"
topics: ["Information Theory", "Credal Uncertainty", "Rate–Distortion", "Robust Compression"]
image: "/images/publications/credal.svg"
pdf_url: "https://mentis.info/wp-content/uploads/2026/05/Credal_ITW_2026.pdf"
project_url: "/projects/credal-rate-distortion/"
abstract: "A robust rate–distortion framework for source coding under credal uncertainty, where the true source law is not known exactly but belongs to a set of plausible distributions."
math: true
bibtex: |
  @misc{bonacorsi2026credal,
    title={Credal Rate--Distortion Theory},
    author={Bonacorsi, Nicolò and Caprio, Michele and Meneghello, Francesca and Restuccia, Francesco},
    year={2026}
  }
---

This page contains extended notes, figures, proof sketches, and links related to the paper.

The robust rate--distortion prototype can be written schematically as

\begin{equation}
R_{\mathcal P}(D)
=
\inf_{P_{\widehat X|X}}
I_{\mathcal P}(X;\widehat X).
\label{eq:credal-rd-paper}
\end{equation}

Equation $\eqref{eq:credal-rd-paper}$ represents the robust variational principle behind the construction.
