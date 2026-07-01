---
layout: project
title: "Bayesian Modeling of Collatz Stopping Times"
date: 2026-03-01
author: "Nicolò Bonacorsi"
topics: ["Bayesian Inference", "Probabilistic Machine Learning", "Number Theory", "Monte Carlo", "Heavy Tails"]
image: "/images/publications/collatz.svg"
question: "Can Collatz stopping times be modeled probabilistically through Bayesian and machine-learning tools?"
key_idea: "Treat stopping-time behavior as a statistical object and study its empirical distribution, uncertainty, and tail behavior."
results: "The project connects number-theoretic dynamics with Bayesian modeling, simulation, and probabilistic prediction."
math: true
---

This project studies Collatz stopping times from a probabilistic machine-learning perspective.

For the Collatz map,

\begin{equation}
T(n)
=
\begin{cases}
n/2, & n \equiv 0 \pmod 2,\\
3n+1, & n \equiv 1 \pmod 2.
\end{cases}
\label{eq:collatz-map}
\end{equation}

Equation \eqref{eq:collatz-map} defines the basic deterministic dynamics.
