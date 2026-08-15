# Critical two-spin obstruction and endgame reduction

**Date:** 2026-08-16
**Claim level:** structural reduction only; no completed Navier–Stokes regularity proof is claimed.

## 1. Scaling audit

For the Navier–Stokes scaling
\[
u_\lambda(x,t)=\lambda u(\lambda x,\lambda^2t),
\]
the helical moments obey
\[
E_{\pm,\lambda}=\lambda^{-1}E_\pm,\qquad
K_{\pm,\lambda}=K_\pm,\qquad
Z_{\pm,\lambda}=\lambda Z_\pm.
\]
Hence
\[
\boxed{\Xi:=\frac{\sqrt{K_+K_-}}{\nu^2}}
\]
is exactly scale invariant. The remaining local balanced heterochiral channel therefore cannot be closed by saying that viscosity becomes stronger merely because the active frequency tends to infinity.

If \(K_{+,N}\sim K_{-,N}\sim c\nu^2\), then
\[
E_N\sim \frac{c\nu^2}{N}.
\]
A critical packet at octave \(2^jN\) costs energy of order \(2^{-j}\). Thus no strictly positive energy cost per octave follows from the coarse budgets alone; any closing cost must be scale invariant and tied to coherence, phase, angular packing, or another feature of the true nonlinearity.

## 2. Quadratic-invariant classification

Work first on a finite Galerkin helical network. A mode \(i\) has signed wavenumber
\[
h_i=\sigma_i|k_i|.
\]
For a nondegenerate triad \((i,j,k)\), the transfer direction is
\[
(\lambda_i,\lambda_j,\lambda_k)
=(h_j-h_k,\ h_k-h_i,\ h_i-h_j),
\]
and satisfies
\[
\lambda_i+\lambda_j+\lambda_k=0,\qquad
h_i\lambda_i+h_j\lambda_j+h_k\lambda_k=0.
\]

For a diagonal quadratic functional \(Q=\sum_i q_i|z_i|^2\), conservation for arbitrary signed current on this triad requires
\[
q_i\lambda_i+q_j\lambda_j+q_k\lambda_k=0.
\]
The orthogonal complement of the nondegenerate transfer direction is spanned by \((1,1,1)\) and \((h_i,h_j,h_k)\). Therefore
\[
(q_i,q_j,q_k)
=A_\tau(1,1,1)+B_\tau(h_i,h_j,h_k).
\]
On a connected nondegenerate triad network, overlap propagates the same affine coefficients, giving
\[
\boxed{q_\sigma(k)=A+B\sigma k},
\qquad
\boxed{Q=A E+B\mathcal H}.
\]
Degenerate or disconnected Galerkin components must be handled separately before an infinite-dimensional limit; the statement above is the connected-network classification used here.

## 3. No positive critical quadratic invariant for both spins

A positive scale-critical quadratic weight must grow like \(|k|\) on both helicity sectors. But
\[
q_+(k)=A+Bk,\qquad q_-(k)=A-Bk.
\]
For \(B\ne0\), one sign becomes negative at sufficiently large \(k\). Positivity for both signs at arbitrarily high frequency forces \(B=0\), leaving energy alone. Thus, in this class,
\[
\boxed{\text{full two-spin Euler has no positive scale-critical quadratic invariant}.}
\]
This explains the sharp difference from a one-sign helical system, where helicity is positive and coincides with the critical \(\dot H^{1/2}\)-level quantity.

## 4. Why the optimal defect is natural

Define
\[
r=\Lambda u-a u-b\omega
\]
by minimizing \(\|\Lambda u-a u-b\omega\|_2^2\). Then
\[
r\perp u,\qquad r\perp\omega,\qquad \mathcal Y:=\|r\|_2^2.
\]
For the Euler part \(F=P(u\times\omega)\),
\[
\langle u,F\rangle=0,\qquad \langle\omega,F\rangle=0,
\]
so the critical nonlinear production collapses exactly to
\[
\boxed{\kappa=\langle\Lambda u,F\rangle=\langle r,F\rangle.}
\]
Thus \(r\) is precisely the part of \(\Lambda u\) not protected by the two available quadratic conservation directions.

Because \(a,b\) are minimizers, stationarity removes the \(a'\), \(b'\) terms from the derivative of the minimized defect, yielding
\[
\boxed{\mathcal Y'=2\Gamma-2\nu\|\Lambda r\|_2^2.}
\]
The variable \(\mathcal Y\) is therefore a modulated dynamic defect, not a new invariant.

## 5. Critical-stack consistency test

A coarse dyadic stack with
\[
K_{+,j}=K_{-,j}=c\nu^2,\qquad N_j=2^j,
\]
up to a top index \(J(t)\) has
\[
K(t)\sim C\nu^2J(t),\qquad E(t)\lesssim C\nu^2.
\]
If \(2^{J(t)}\sim(T-t)^{-1/2}\), then
\[
Z(t)\sim(T-t)^{-1/2}\in L^1_t,
\]
while
\[
K(t)\sim C\log\frac1{T-t}\to\infty.
\]
This is only a consistency model, not an NSE solution. It shows that energy, helicity and parabolic dissipation budgets alone do not exclude a critical stack.

## 6. True vector geometry still gives depletion

For a true Fourier triad \(k=p+q\), incompressibility implies
\[
|q\cdot\widehat u(p)|
\le |q|\sin\theta\,|\widehat u(p)|,
\]
where \(\theta\) is the angle between \(p\) and \(q\). For two inputs of size \(N\), an output approaching the maximal jump \(2N\) requires \(\theta\to0\), exactly where this convection coefficient vanishes.

Thus maximal radial jumps are geometrically depleted. This does not forbid a local geometric cascade: a fixed nondegenerate angle gives order-one coupling and a fixed scale ratio greater than one.

## 7. Current last channel

After the preceding reductions, the unresolved channel is simultaneously:

- heterochiral;
- local/comparable in frequency;
- non-collinear and nondegenerate;
- balanced in critical spin mass;
- forward-phase coherent;
- repeated through arbitrarily many scales.

Schematically, a dangerous sequence requires
\[
\boxed{\frac{\sqrt{K_{+,N}K_{-,N}}}{\nu^2}\gtrsim1}
\]
for arbitrarily large \(N\), together with sustained signed heterochiral flux.

Homochiral interactions have higher radial-difference depletion; far-nonlocal heterochiral interactions have a scale-ratio gain; pure-spin states lose the escape channel. The local balanced heterochiral stack is therefore the remaining critical configuration in the present framework.

## 8. Closing target

A closing argument cannot be another positive quadratic invariant or a fixed energy loss per octave. It must be genuinely non-quadratic and scale invariant, exploiting phase coherence, angular packing, or another rigidity of the true heterochiral network.

**Balanced Heterochiral Stack Rigidity Lemma (target, unproved).** Rule out a smooth finite-time trajectory that maintains, across an unbounded sequence of adjacent scales,
\[
\text{balanced critical spin mass}
+\text{nondegenerate angular geometry}
+\text{forward phase coherence}.
\]
A proof with constants compatible with exact Navier–Stokes scaling would close the remaining channel. Until then this is a structural reduction, not a Millennium proof.
