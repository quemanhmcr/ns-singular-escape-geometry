# Navier–Stokes Singular Escape Geometry

Private research snapshot of a developing geometric/spectral approach to the 3D incompressible Navier–Stokes regularity problem.

> **Status:** research program / proof attempt. This repository does **not** claim a completed proof of the Clay Millennium problem. The purpose of this snapshot is to preserve the exact identities, reductions, barriers, and remaining lemma as of 2026-08-15.

## Central physical picture

The nonlinear Euler part is tangent to the energy shell,

\[
X_t=Y-\nu L^2X,\qquad \langle X,Y\rangle=0,
\]

so a hypothetical singularity need not escape by increasing the energy norm. Instead, it may move tangentially inside the bounded energy ball toward ever higher frequencies / stronger norms. We call this **singular escape**.

For the velocity field \(u\), with \(\Lambda=(-\Delta)^{1/2}\), define

\[
E=\|u\|_2^2,\qquad
K=\langle u,\Lambda u\rangle,\qquad
Z=\|\Lambda u\|_2^2,
\]

\[
m=\frac{K}{E},\qquad s=(\Lambda-m)u.
\]

Then

\[
\langle u,s\rangle=0,
\qquad
\|s\|_2^2=\frac{EZ-K^2}{E}.
\]

Thus \(D:=EZ-K^2\) is the centered spectral defect / variance quantity measuring departure from a single spectral shell.

The nonlinear escape coupling is

\[
\kappa=\langle s,F\rangle
       =\langle \omega,s\times u\rangle,
\]

where \(F=P(u\times\omega)\) is the Leray-projected Euler forcing.

With

\[
M_3=\|\Lambda^{3/2}u\|_2^2,
\qquad
\nu_E=\frac{\kappa}{M_3},
\]

one has the exact critical-norm identity

\[
K'=2M_3(\nu_E-\nu).
\]

This rewrites the competition between nonlinear transfer and physical viscosity as a scalar threshold \(\nu_E\gtrless\nu\).

See `docs/current-state.md` for the full derivation and `docs/proof-roadmap.md` for the remaining obstruction.
