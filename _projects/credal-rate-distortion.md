---
layout: project
title: "Credal Rate–Distortion Theory"
date: 2026-07-01
author: "Nicolò Bonacorsi"
topics: ["Information Theory", "Credal Uncertainty", "Rate–Distortion", "Uncertainty Quantification", "Robust Compression"]
image: "/images/publications/credal.svg"
question: "How should rate–distortion theory change when the source law is not known exactly, but belongs to a credal set?"
key_idea: "Replace single-law compression by a robust formulation in which distortion constraints must hold uniformly over a family of plausible source distributions."
results: "The project studies reverse-inclusion phenomena, robust operational limits, finite-window behavior, and graph-theoretic compression regimes."
math: true
---

This project develops a robust version of rate--distortion theory under credal uncertainty.

You can write equations here, for example:

\begin{equation}
R_{\mathcal P}(D)
=
\inf_{P_{\widehat X|X}}
I_{\mathcal P}(X;\widehat X).
\label{eq:credal-rd}
\end{equation}

Equation \eqref{eq:credal-rd} is a schematic form of the robust variational problem.
