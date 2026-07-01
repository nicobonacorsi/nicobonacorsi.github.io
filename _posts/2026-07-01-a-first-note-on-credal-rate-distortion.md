---
layout: post
title: "A First Note on Credal Rate–Distortion"
date: 2026-07-01
categories: [scientific]
scientific_type: "Research Notes"
tags: [Information Theory, Credal Uncertainty, Rate-Distortion, Robust Compression]
math: true
---

This is a short technical note testing the scientific blog format. The goal is to write research notes that are not necessarily complete papers, but still precise enough to be useful later.

<!--more-->



## Motivation

Classical rate–distortion theory usually starts from a single source law $P_X$. A robust variant asks what happens when the true law belongs to a credal set

$$
\mathcal P \subseteq \Delta(\mathcal X).
$$

The operational question is then no longer

$$
\mathbb E_{P_X}[d(X,\widehat X)] \le D,
$$

but rather

$$
\sup_{P \in \mathcal P}
\mathbb E_{P P_{\widehat X|X}}
\big[d(X,\widehat X)\big]
\le D.
$$

## A numbered equation

The credal rate--distortion prototype can be written as the constrained variational problem in Equation \eqref{eq:credal-rd-prototype}.

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
\big[d(X,\widehat X)\big]
\le D.
\label{eq:credal-rd-prototype}
\end{equation}

The point of Equation \eqref{eq:credal-rd-prototype} is that the distortion constraint is no longer imposed under a single source law, but uniformly over the whole credal set.
