# Scaling Laws in Periodically Forced Nonlinear Discrete-Time Maps

This repository investigates the response of nonlinear discrete-time dynamical systems to periodic external forcing, with emphasis on scaling behaviour near stable fixed points and near critical (tipping) transitions.

The project combines analytical perturbation theory, bifurcation analysis, and numerical simulations to understand how the forcing amplitude and frequency influence the long-time dynamics.

---

## Overview

We consider periodically forced nonlinear maps of the form

$$
x_{t+1}=F(x_t)+\varepsilon g(t),
$$

where

- $F(x)$ is a nonlinear discrete map,
- $\varepsilon$ is the forcing amplitude,
- $g(t)$ is a periodic forcing with zero time average.

The principal forcing considered is

$$
g(t)=e^{i(\Omega t+\varphi)},
$$

which naturally includes

$$
g(t)=(-1)^t
$$

as the special case

$$
\Omega=\pi,\qquad\varphi=0.
$$

---

## Objectives

The project addresses two complementary regimes.

### 1. Perturbative response near a stable fixed point

For weak forcing,

$$
\varepsilon\ll1,
$$

the long-time average response is derived analytically using perturbation theory.

The resulting quadratic response scales as

$$
\Delta\bar{x}
\propto
\varepsilon^2,
$$

with an explicit frequency-dependent prefactor.

---

### 2. Critical scaling near tipping

As the forcing amplitude approaches the critical value

$$
\varepsilon_c,
$$

the stable periodic orbit disappears via a saddle-node bifurcation of the corresponding stroboscopic map.

Near the critical point,

$$
|\bar{x}-\bar{x}_c|
\sim
C_c
|\varepsilon-\varepsilon_c|^{1/2},
$$

where

- the exponent \(1/2\) is universal,
- the critical prefactor \(C_c\) depends on the nonlinear dynamics and the forcing.

---

## Main Results

- Analytical perturbative response for general periodic forcing.
- Explicit frequency-dependent prefactor for weak forcing.
- Analytical derivation of the universal square-root scaling near tipping.
- Analytical expression for the critical prefactor in the two-period forcing case.
- Numerical verification of both perturbative and critical scaling laws.
- Comparison between theory and numerical simulations over several decades in forcing amplitude.

---

## Repository Structure

```text
.
├── research-log.md
│
├── numerics/
│   ├── python/
│   ├── matlab/
│   └── notebooks/
│
├── figures/
│
├── manuscript/
│
└── README.md
```

---

## Methodology

The analysis combines

- perturbation theory,
- nonlinear discrete dynamical systems,
- saddle-node bifurcation theory,
- stroboscopic maps,
- numerical continuation,
- direct numerical simulations.

---

## Current Status

Current progress includes

- analytical perturbation theory,
- numerical verification,
- critical scaling derivation,
- analytical prefactor for period-two forcing.

Ongoing work includes

- frequency dependence of the critical prefactor,
- extension to general periodic forcing,
- manuscript preparation.

---

## References

The analysis builds upon ideas from

- Steven H. Strogatz, *Nonlinear Dynamics and Chaos*.
- Yuri A. Kuznetsov, *Elements of Applied Bifurcation Theory*.
- Relevant literature on periodically forced discrete dynamical systems and saddle-node bifurcations.

---

## Author

**Arkaprava Bose**

Integrated BS-MS, IISER Kolkata

Supervisor : Marc Timme, TU Dresden
- Bifurcation Theory
- Dynamical Systems
- Network Dynamics
