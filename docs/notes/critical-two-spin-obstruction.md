# Critical two-spin obstruction and endgame reduction

**Date:** 2026-08-16
**Claim level:** structural reduction only; no completed Navier–Stokes regularity proof is claimed.

This note records the current endgame after the helical within-spin reduction. It is intentionally compact: only results that materially change the proof architecture are kept here.

## 1. Scaling audit: the last channel is genuinely critical

For the Navier–Stokes scaling
\[
u_\lambda(x,t)=\lambda u(\lambda x,\lambda^2t),
\]
the helical moments satisfy
\[
E_{\pm,\lambda}=\lambda^{-1}E_\pm,\qquad
K_{\pm,\lambda}=K_\pm,\qquad
Z_{\pm,\lambda}=\lambda Z_\pm.
\]
Hence
\[
\boxed{\Xi:=\frac{\sqrt{K_+K_-}}{\nu^2}}
\]
is scale invariant. Therefore the remaining local balanced heterochiral channel cannot be closed by claiming that viscosity becomes stronger merely because the active frequency tends to infinity.

If at scale \(N\)
\[
K_{+,N}\sim K_{-,N}\sim c\nu^2,
\]
then the corresponding energy is only
\[
E_N\sim \frac{c\nu^2}{N}.
\]
Thus a critical packet at octave \(2^jN\) costs energy of order \(2^{-j}\). No fixed positive energy cost per octave can follow from the coarse energy budget.

## 2. Classification of diagonal quadratic invariants

Work first on a finite Galerkin helical network. For mode \(i\), write
\[
h_i=\sigma_i|k_i|.
\]
For a nondegenerate triad \(\tau=(i,j,k)\), the transfer direction is
\[
(\lambda_i,\lambda_j,\lambda_k)
=(h_j-h_k,\ h_k-h_i,\ h_i-h_j).
\]
It obeys
\[
\lambda_i+\lambda_j+\lambda_k=0,
\qquad
h_i\lambda_i+h_j\lambda_j+h_k\lambda_k=0.
\]

Let
\[
Q=\sum_i q_i|z_i|^2
\]
be diagonal quadratic. Conservation of \(Q\) for arbitrary signed current on this triad requires
\[
q_i\lambda_i+q_j\lambda_j+q_k\lambda_k=0.
\]
For a nondegenerate triad, the orthogonal complement of \((\lambda_i,\lambda_j,\lambda_k)\) is spanned by \((1,1,1)\) and \((h_i,h_j,h_k)\). Hence
\[
(q_i,q_j,q_k)=A_\tau(1,1,1)+B_\tau(h_i,h_j,h_k).
\]
On a connected nondegenerate triad network, overlap propagates the same affine coefficients, so
\[
\boxed{q_\sigma(k)=A+B\sigma k},
\qquad
\boxed{Q=A E+B\mathcal H}.
\]
Degenerate or disconnected Galerkin components must be handled separately before an infinite-dimensional limit; the statement above is the connected-network classification used here.

## 3. No positive two-spin critical quadratic invariant

A positive scale-critical quadratic weight would need growth comparable to \(|k|\) on both helicity sectors. But
\[
q_+(k)=A+Bk,\qquad q_-(k)=A-Bk.
\]
For \(B\neq0\), one sign is eventually negative. Positivity on both spin sectors for arbitrarily high frequency therefore forces \(B=0\), leaving energy only.

Thus, in the class above,
\[
\boxed{\text{full two-spin Euler has no positive scale-critical diagonal quadratic invariant}.}
\]
This explains the contrast with a one-sign helical system, where helicity is positive and equals the critical \(\dot H^{1/2}\)-level quantity.

## 4. Why the optimal defect is the natural variable

Define \(a,b\) by minimizing
\[
\|\Lambda u-au-b\omega\|_2^2,
\]
and set
\[
r=\Lambda u-au-b\omega,\qquad \mathcal Y=\|r\|_2^2.
\]
Then
\[
r\perp u,\qquad r\perp\omega.
\]
For the Euler part \(F=P(u\times\omega)\),
\[
\langle u,F\rangle=0,\qquad \langle\omega,F\rangle=0,
\]
so the critical nonlinear production collapses exactly to
\[
\boxed{\kappa=\langle\Lambda u,F\rangle=\langle r,F\rangle}.
\]
Thus \(r\) is precisely the part of \(\Lambda u\) not protected by the two available quadratic conservation directions.

Because \(a,b\) are minimizers, the stationarity conditions remove the \(a'\), \(b'\) terms from the derivative of the minimized defect. Hence
\[
\boxed{\mathcal Y'=2\Gamma-2\nu\|\Lambda r\|_2^2}.
\]
The defect is therefore a modulated Lyapunov-type quantity, not a new invariant.

## 5. Critical-stack consistency test

Consider only a consistency model, not an NSE solution. Let \(N_j=2^j\) and suppose up to a top index \(J(t)\),
\[
K_{+,j}=K_{-,j}=c\nu^2.
\]
Then
\[
K(t)\sim C\nu^2J(t),\qquad E(t)\lesssim C\nu^2.
\]
If
\[
2^{J(t)}\sim(T-t)^{-1/2},
\]
then
\[
Z(t)\sim(T-t)^{-1/2}\in L_t^1,
\qquad
K(t)\sim C\log\frac1{T-t}\to\infty.
\]
Thus energy and parabolic dissipation budgets alone do not exclude a critical stack. This rules out a proof strategy based only on global moment budgets or a fixed energetic loss at each octave.

## 6. What the true vector geometry still contributes

For an actual Fourier triad \(k=p+q\), incompressibility gives
\[
|q\cdot\widehat u(p)|
\le |q|\sin\theta\,|\widehat u(p)|,
\]
where \(\theta\) is the angle between \(p\) and \(q\).

For two inputs of size \(N\), an output approaching the maximal radial jump \(2N\) requires \(\theta\to0\), exactly where the convection coefficient vanishes. Hence maximal radial jumps are geometrically depleted.

This does **not** rule out a local geometric cascade: a fixed nondegenerate angle gives order-one coupling and a fixed scale ratio greater than one. Therefore the last obstruction is not collinear high-high transfer, but a repeated nondegenerate local heterochiral cascade.

## 7. Current last channel

After the reductions established so far, the unresolved configuration is simultaneously:

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

The other channels already carry extra depletion in the present framework: homochiral interactions carry higher radial-difference factors; far-nonlocal heterochiral interactions carry a scale-ratio gain; pure-spin states lose the critical escape channel.

## 8. Closing target

A closing argument cannot be another positive quadratic invariant, nor a fixed energy loss per octave. It must be a genuinely non-quadratic, scale-invariant rigidity of the true heterochiral network.

**Balanced Heterochiral Stack Rigidity Lemma (unproved).**
Rule out a smooth finite-time trajectory that maintains, across an unbounded sequence of adjacent scales,
\[
\text{balanced critical spin mass}
+\text{nondegenerate angular geometry}
+\text{forward phase coherence}.
\]

A proof of this rigidity statement, with constants compatible with exact Navier–Stokes scaling, would close the remaining channel. Until such a lemma is proved, this remains a structural reduction rather than a Millennium proof.
