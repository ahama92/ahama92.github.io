---
title: '1D Shock Tube'
date: 2020-04-06
permalink: /posts/2020/04/1d-sohck-tube/
tags:
  - compressible
  - shock wave
  - shock tube
  - inviscid
  - flow simulation
---

## The Inviscid Compressible 1D Flow

The inviscid compressible 1-dimensional flow is analyzed numerically using the finite volume method in the present project. The problem in question is the famous shock tube which is simulated from an initial condition to $t=0.15$ seconds. The domain length is 1 unit which is long enough so that no flow feature would reach either of the ends of the tube. The Euler equations are the governing equations of this problem. Two flux vector splitting schemes of Steger-Warming and Roe are utilized for this purpose. Time integration is fully explicit (implicit methods are readily applicable as well) including Explicit Euler and several Runge-Kutta methods. To prevent overshoots in the solution, several flux limiters are introduced, including, Superbee, Van Leer, and 2nd order upwind limiters.

<embed src="/files/2020-04-06-post-511-compressible/report.pdf" type="application/pdf" height="100%" width="100%">