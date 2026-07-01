---
layout: post
title: "Course Note: A Minimal Optimal Stopping Principle"
date: 2026-07-02
categories: [scientific]
scientific_type: "Course Notes"
tags: [Probability, Optimal Stopping, Stochastic Processes]
math: true
---

A short course-style note on the basic principle behind optimal stopping.

<!--more-->



Let $(X_t)_{t \ge 0}$ be a Markov process and let $g$ be a reward function.

$$
V(x) = \sup_{\tau} \mathbb E_x \left[ e^{-r\tau} g(X_\tau) \right].
$$

The continuation region is where waiting has positive value, while the stopping region is where immediate exercise is optimal.
