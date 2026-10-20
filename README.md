# Response Shifts and Tipping in Nonlinear Maps

Analytical and numerical study of discrete-time maps driven by zero-mean oscillatory forcing near a stable fixed point $x^* $. Two questions are addressed: (i) how far the long-time average state shifts away from $x^* $ and (ii) at which forcing amplitude $\varepsilon_c$ the response can no longer stay near $x^* $ (tipping). This is the discrete-time counterpart of the continuous-time work of Thümler, Schröder and Timme (2022).

---

## Setup

$$
x_{t+1}=F(x_t)+\varepsilon\, g(t),\qquad g(t)=\cos(\Omega t+\varphi),
$$

where $F$ is a nonlinear map with a stable fixed point $x^*$ and $\varepsilon$ is the forcing strength. The alternating forcing $g(t)=(-1)^t$ is the case $\Omega=\pi$, $\varphi=0$. The worked model is $F(x)=ax+bx^2$ (numerics use $a=\tfrac12$, $b=1$).

---

## Main Results

**1. Weak forcing: quadratic response shift.** The average shift is

$$
\Delta \bar{x} = \frac{F''(x^{*})}{4(1-F'(x^{*}))(1+F'(x^{*})^2-2F'(x^{*})\cos(\Omega))}\varepsilon^2 + O(\varepsilon^3)
$$

- The derivation uses only boundedness of the orbit, so $\Omega/2\pi$ may be rational or irrational.
- It comes with explicit confinement and remainder bounds.
- $\Omega=\pi$ is exceptional and gives twice the value above.
- For the quadratic map, the bounds give $\varepsilon_c\ge(1-a)^2/(4|b|)$.

**2. Tipping as a fold of the stroboscopic map.** For $\Omega=2\pi/p$ the periodic response approaches the critical orbit with a square-root law,

$$
|x-x_c|=A(p)\,|\varepsilon-\varepsilon_c|^{1/2},\qquad A(p)=\sqrt{\frac{2G_{p,\varepsilon}}{G_{p,xx}}},
$$

where $G_p$ is the stroboscopic map. The derivatives $G_{p,\varepsilon}$ and $G_{p,xx}$ are given in closed form along the critical orbit for general $p$.

**3. Large-period limit.** Harmonic balance for the critical orbit combined with Laplace's method gives $A(p)\propto e^{-pS(\theta_*)/4\pi}$. Harmonic balance reproduces the pseudo-arclength critical amplitude to $6\times10^{-9}$ at $p=30$.

**4. Numerical checks.**
- The confinement and remainder bounds hold.
- The $\varepsilon^2$ law is confirmed (fitted exponent $2.000\pm0.002$ for $p=2,3,5,10$ and the golden-mean frequency).
- The square-root scaling is confirmed (fitted exponent $0.501$ at $p=2$).
- $A(p)$ decays exponentially in $p$ .

---

## Repository Structure

```text
.
├── research-log.md
├── src/
├── figures/
├── manuscript/
└── README.md
```

---

## Current Status

Done: weak-forcing theory with bounds, fold scaling for general $p$, harmonic-balance and Laplace analysis, numerical verification.

Ongoing:
- Analytical evaluation of $S(\theta_*)/4\pi$ to compare with the fitted decay rate.
- Resolving the ~1% harmonic-balance vs. continuation mismatch at $p=40$.
- Manuscript preparation.

---

## References

- M. Thümler, M. Schröder, M. Timme, *Nonlinear and divergent responses of fluctuation-driven systems*, IFAC-PapersOnLine **55**, 254 (2022).
- Y. A. Kuznetsov, *Elements of Applied Bifurcation Theory*, Springer (2010).

---

## Author

**Arkaprava Bose**

Integrated BS-MS, IISER Kolkata

Supervisor: Marc Timme, TU Dresden
