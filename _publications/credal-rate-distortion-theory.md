---
layout: publication
title: "Credal Rate–Distortion Theory"
date: 2026-05-01
authors: ["Nicolò Bonacorsi", "Michele Caprio", "Francesca Meneghello", "Francesco Restuccia"]
venue: "IEEE ITW 2026"
status: "Submitted"
topics: ["Information Theory", "Credal Uncertainty", "Rate–Distortion", "Robust Compression"]
image: "/images/publications/credal.svg"
pdf_url: "https://mentis.info/wp-content/uploads/2026/05/Credal_ITW_2026.pdf"
project_url: "/projects/credal-rate-distortion/"
abstract: "We develop a rate–distortion framework for source coding under credal uncertainty, where each input is represented by a set of plausible probability laws rather than a single distribution. The theory connects safe credal aggregation with directed distortion, graph coloring, graph entropy, and robust compression."
math: true
bibtex: |
  @misc{bonacorsi2026credal,
    title={Credal Rate--Distortion Theory},
    author={Bonacorsi, Nicolò and Caprio, Michele and Meneghello, Francesca and Restuccia, Francesco},
    year={2026}
  }
---

This paper studies compression when the object attached to each input is not a single probability law, but a credal set. We introduce a directed free-energy distortion for replacing several credal likelihoods by one aggregate credal set, and show that safe one-shot compression reduces exactly to a graph-coloring problem.

In the block setting, local observers lead to graph-entropy rates, while finite-window observers reveal an intermediate regime that is genuinely regularized and does not collapse to a single-letter formula.