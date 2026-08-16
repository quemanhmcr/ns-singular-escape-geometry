# Proof Roadmap and Open Lemma

## Objective

Convert the singular-escape identities into a rigorous global regularity argument for 3D incompressible Navier–Stokes.

This document deliberately separates **proved identities/reductions** from the **unproved closing lemma**.

## Established chain

1. **Energy tangency**
   \[
   \langle u,F\rangle=0,
   \qquad E'=-2\nu Z.
   \]

2. **Canonical escape coordinate**
   \[
   m=K/E,
   \qquad s=(\Lambda-m)u,
   \qquad D=EZ-K^2=E\|s\|_2^2.
   \]

3. **Exact nonlinear escape coupling**
   \[
   \kappa=\langle s,F\rangle
   =\langle\omega,s\times u\rangle.
   \]

4. **Critical norm dynamics**
   \[
   K'=2M_3(\nu_E-\nu),
   \qquad \nu_E=\kappa/M_3.
   \]

5. **Spectral-defect barrier**
   \[
   |\nu_E|\le C_*\sqrt{\frac{KD}{K^2+D}}.
   \]
   Therefore \(K'>0\) at large \(K\) forces a definite amount of \(D\).

6. **Finite budget**
   \[
   (E^2)'=-4\nu(K^2+D),
   \qquad
   \int_0^T(K^2+D)\,dt\le E(0)^2/(4\nu).
   \]

7. **Defect dynamics**
   \[
   D'=2E\Gamma
   -2\nu E\|\Lambda s\|_2^2
   -2\nu(Z/E)D.
   \]

8. **Commutator collapse**
   \[
   \Gamma=-\langle s,[\Lambda,u\cdot\nabla]u\rangle.
   \]

9. **Helical reduction**
   Critical nonlinear production requires both spectral defect and heterochiral coupling.

## False shortcuts already ruled out

The following are **not** sufficient and should not be reused as hidden assumptions:

- “Energy bounded implies no blow-up.” False in an infinite-dimensional state space.
- “A narrow spectral packet is invariant.” False; at \(s=0\), generally \(D''=2E\|QF\|_2^2\ge0\).
- “Narrow packet automatically makes all nonlinear interactions small.” False for heterochiral classes; same-helicity and opposite-helicity triads have different signed-wavenumber structures.
- Generic Hölder/Sobolev/Kato–Ponce estimates alone appear critical and do not close the argument.

## Closing target

A sufficient closing statement would be a theorem of the following form.

### Heterochiral Cascade Barrier Lemma (target, unproved)

There exists a universal quantitative mechanism, exploiting the exact helical/triadic symbol of incompressible Navier–Stokes, which prevents any smooth solution from sustaining an infinite sequence of times approaching a finite \(T_*\) for which

\[
K\to\infty,
\qquad
\kappa>\nu M_3,
\qquad
D\ge \frac{aK^2}{K-a}
\]

with \(a=\nu^2/C_*^2\), while also respecting the finite budget

\[
\int_0^{T_*}(K^2+D)\,dt<\infty.
\]

Equivalently, the dangerous regime should exhibit a structural depletion in the coherent heterochiral component of

\[
\Gamma=-\langle s,[\Lambda,u\cdot\nabla]u\rangle
\]

or directly in \(\kappa\), sufficient to force \(\nu_E\le\nu\) before \(K\) can escape to infinity.

## Next technical directions

1. Fix a scale-consistent packet/localization framework, then bound the relative-defect production action \(\mathfrak A_Q\) from true cross-output dynamics.
2. Bound the macroscopic reset action \(\mathfrak R_Q\); together with \(\mathfrak A_Q\), it controls the bypass entropy and all critical-norm growth.
3. Relate the macroscopic reset action to the microscopic phase/projective reset network, and relate this total-defect route to the within-spin \((\Gamma_{\rm sp})_+\) Riccati route without identifying the productions.
4. Stress-test each global estimate on explicit triads, cancellation ladders, symmetry quotients, diamonds, and critical stacks.
