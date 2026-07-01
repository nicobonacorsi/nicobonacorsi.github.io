---
layout: publication
title: "Bayesian Modeling of Collatz Stopping Times: A Probabilistic Machine Learning Perspective"
date: 2026-03-01
authors: ["Nicolò Bonacorsi", "Matteo Bordoni"]
venue: "arXiv"
status: "Preprint"
topics: ["Bayesian Inference", "Probabilistic Machine Learning", "Number Theory", "Monte Carlo", "Heavy Tails"]
image: "/images/publications/collatz.svg"
arxiv_url: "https://arxiv.org/abs/2603.04479"
paper_url: "https://arxiv.org/abs/2603.04479"
project_url: "/projects/bayesian-collatz/"
abstract: "A probabilistic study of Collatz total stopping times over n ≤ 10^7, combining Bayesian Negative Binomial regression with stochastic odd-block generative models to study overdispersion, modular structure, and predictive uncertainty."
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

This paper studies the empirical law of Collatz total stopping times for \(n \leq 10^7\). We compare a Bayesian hierarchical Negative Binomial regression, based on \(\log n\) and \(n \bmod 8\), with stochastic generators derived from the odd-block decomposition \(K = v_2(3m+1)\).

The regression model gives the strongest held-out predictive performance, while the odd-block models provide a mechanistic explanation of heavy tails and arithmetic heterogeneity.