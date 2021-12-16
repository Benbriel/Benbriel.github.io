---
title: 'Testing Latex'
date: 2021-12-16
permalink: /posts/2021/12/testing-latex/
tags:
  - Latex
  - electrodynamics
  - classical mechanics
---

This post tests the usage of $\LaTeX$ on this website. For example, the contravariant formulation of classical electromagnetism states that

\\[\begin{equation} \label{GaussAmpere} \partial_{\alpha} F^{\alpha \beta} = \mu_0 J^{\beta} \end{equation} \\]

\\[\begin{equation} \label{GaussFaraday} \partial_{\alpha} \left( \frac{1}{2} \epsilon^{\alpha \beta \gamma \delta} F_{\gamma \delta} \right) = 0 \end{equation} \\]

Where $F^{\alpha \beta}$ is the [electromagnetic tensor](https://en.wikipedia.org/wiki/Electromagnetic_tensor), $J^{\alpha}$ the [four-current](https://en.wikipedia.org/wiki/Four-current) and $\epsilon^{\alpha \beta \gamma \delta}$ the [Levi-Civita symbol](https://en.wikipedia.org/wiki/Levi-Civita_symbol). Equations can even be referenced, like \eqref{GaussAmpere} or \eqref{GaussFaraday}.

Classical Mechanics Example
======

For example, one can write the Lagrangian of a point particle moving in one dimension space under a certain potential as $\mathcal{L}=T-V$, meaning

\\[\mathcal{L}=\frac{m}{2} \dot{q}^2 - V(q) \\]

where $m$ is the mass of the particle, $q$ is its position, and $\dot{q}$ is its velocity. In Hamiltonian mechanics, the momentum $p$ is defined as $p=\partial_q \mathcal{L}=m \dot{q}$. The Hamiltonian is defined as $H=p \dot{q} - \mathcal{L}$, so replacing $\dot{q}$, it yields

\\[H = \frac{p^2}{2 m} + V(q) \\]

Now, one could use the Hamilton equations of motion to solve for the position and momentum, however, we're taking the long way. Due to the simmetries of the Hamiltonian, $H'=H + \partial_t S$ gives the same equations of motion, where $S=S(q,p,t)$ is any function of the position, momentum and time. The idea is to look for an action $S$ such that the new Hamiltonian is zero, thus forming the Hamilton-Jacobi equation. This is a very general problem, so in this case it turns tedious and much longer than using the Euler-Lagrange equations. If one defines $\partial_q S=p$, then one gets a differential equation for the action $S$, of the form

\\[\frac{\left( \partial_q S \right)^2}{2 m} + V(q) + \partial_t S = 0 \\]

This equation is generally hard to solve. However, identifying cyclic coordinates, or the direct coordinate independence of $H$. In this case, $\partial_t H=0$. This lets one choose an action $S=W(q) - E t$, where in this case $E$ corresponds to the total energy of the particle. Replacing this new $S$,

\\[\frac{W'^2}{2 m} + V(q) = E \Rightarrow W(q) = \int \sqrt{2 m (E - V(q))} dq \\]

Then, having solved for $S$, the chosen canonical transformations result in $\partial_E S = \beta$, where $\beta$ is another constant. This implies

\\[\beta = -t + \int \frac{dq}{\sqrt{\frac{2}{m} \left( E - V(q) \right)}} \\]

Replacing $V(q)$ for a specific potential does not assure that one can write $q$ as $q(t)$ but t(q), however, for most simple cases, the integral can be solved, and the solution $q(t)$ is found.

For example, a harmonic oscillator has a potential that can be written as $V(q)=\frac{k}{2}q^2$, where $k$ is a constant. Replacing on the above equation and solving the integral, one gets

\\[\sqrt{k m}(t+\beta) = m \arcsin{\left( \sqrt{\frac{k}{2 E}} q \right)} \\]

Finally, one can simplify for $q(t)$ to get

\\[q(t) = \sqrt{\frac{2 E}{k}} \sin{\left( \sqrt{\frac{k}{m}}(t + \beta) \right)} \\]

Where $E$ can be interpreted as the initial energy of the system, and $\beta$ as the initial phase. This returns a sine wave, as expected.



Aren't headings cool?
------