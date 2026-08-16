# Critical two-spin obstruction and endgame reduction

**Date:** 2026-08-16
**Claim level:** structural reduction only; no completed Navier–Stokes regularity proof is claimed.

This note keeps only proof architecture that survives the latest audits. Earlier overclaims about global quadratic-invariant classification are corrected here.

## 1. Critical scaling and the optimal escape defect

For the Navier–Stokes scaling
\[
u_\lambda(x,t)=\lambda u(\lambda x,\lambda^2t),
\]
\[
E_{\pm,\lambda}=\lambda^{-1}E_\pm,\qquad
K_{\pm,\lambda}=K_\pm,\qquad
Z_{\pm,\lambda}=\lambda Z_\pm,
\]
so
\[
\Xi:=\frac{\sqrt{K_+K_-}}{\nu^2}
\]
is scale invariant. No argument based on a fixed energy cost per octave can close the last channel.

Let \(a,b\) minimize
\[
\|\Lambda u-au-b\omega\|_2^2,
\qquad
r:=\Lambda u-au-b\omega.
\]
Since \(r\perp u,\omega\) and the Euler forcing \(F=P(u\times\omega)\) satisfies
\[
\langle u,F\rangle=\langle\omega,F\rangle=0,
\]
the critical production is exactly
\[
\boxed{\kappa=\langle\Lambda u,F\rangle=\langle r,F\rangle}.
\]
For \(\mathcal Y=\|r\|_2^2\), stationarity of the minimizer gives
\[
\boxed{\mathcal Y'=2\Gamma-2\nu\|\Lambda r\|_2^2}.
\]
Thus singular escape must repeatedly leave the energy-helicity protected directions.

## 2. Corrected topology of diagonal quadratic invariants

For a nondegenerate helical triad \(\tau=(i,j,k)\), write
\[
h_i=\sigma_i|k_i|,
\qquad
(\lambda_i,\lambda_j,\lambda_k)
=(h_j-h_k,h_k-h_i,h_i-h_j).
\]
A diagonal quadratic weight \(q\) is triadwise invariant iff
\[
q_i\lambda_i+q_j\lambda_j+q_k\lambda_k=0,
\]
so on each single triad
\[
(q_i,q_j,q_k)=A_\tau(1,1,1)+B_\tau(h_i,h_j,h_k).
\]

**Correction.** One-mode overlap of distinct Fourier triads does not force the same \(A_\tau,B_\tau\) globally. For a triad tree with \(T\) triads, the mode count is \(V=2T+1\); the \(T\) triad constraints are independent, hence
\[
\boxed{\dim\mathcal I=T+1}.
\]
Sparse/tree subnetworks therefore possess many local quadratic invariants. Only sufficiently cross-linked networks can collapse this space further.

A useful exact anchoring fact remains. On one triad, if two distinct **same-helicity** endpoints are forced to carry the critical positive weights \(q=k\) and \(q=q\), affine interpolation in signed wavenumber forces the opposite-helicity third weight to be negative. Conversely, local **spin-flipping** handoffs can admit a positive critical-adapted tree invariant. Therefore the dangerous tree channel is the same-spin radial handoff.

## 3. Same-spin handoff and catalyst identity

Take same-spin endpoints \(k<q\) and an opposite-spin catalyst of radius \(p\). With an oriented current \(J\),
\[
T_k=(q+p)J,\qquad
T_q=-(p+k)J,\qquad
T_p=(k-q)J.
\]
The total critical production satisfies
\[
\boxed{\dot K_\triangle=2pT_p},
\]
and in fact
\[
\boxed{\dot K_{\sigma,\triangle}=\dot K_{-\sigma,\triangle}=pT_p=\tfrac12\dot K_\triangle}.
\]
Hence positive critical escape necessarily creates opposite-spin catalyst critical mass.

For two consecutive positive handoffs, a downstream triad can reset the donor/child ratio of the upstream triad **without reverse \(K\)-flux**. Thus reset cost cannot be identified with an opposite signed flux. The correct obstruction comes from the full convolution algebra: consecutive selected handoffs automatically create missing diamond corners and cross-pair forcing.

## 4. Exact mirror/catalyst coefficient comparison

Let \(K^\sigma,Q^\sigma\) be same-helicity modes with
\[
q:=|Q|>k:=|K|,
\qquad
P:=Q-K,\ p:=|P|,
\qquad
M:=Q+K,\ m:=|M|.
\]
The catalyst is taken in helicity \(-\sigma\), and choose the mirror output \(M\) also in helicity \(-\sigma\). Put
\[
S=q+k,\qquad \Delta=q-k,\qquad A=|Q\times K|.
\]
Using the full helical coefficient, both catalyst and mirror couplings contain the same factors \(\Delta A/(qk)\). More precisely, up to the same universal normalization,
\[
|C_{\rm cat}|=\Delta\frac{A}{pqk}(S+p),
\qquad
|C_{\rm mir}|=\Delta\frac{A}{mqk}(S+m).
\]
Therefore
\[
\boxed{\frac{|C_{\rm mir}|}{|C_{\rm cat}|}=\frac{p(S+m)}{m(S+p)}}.
\]
Since \(p,m\le S\),
\[
\boxed{|C_{\rm mir}|\ge \frac{p}{2S}|C_{\rm cat}|}.
\]
There is no independent angular-degeneracy loophole: if the area factor \(A\) vanishes, both couplings vanish together. In a local comparable channel \(p\gtrsim S\), mirror and catalyst couplings are comparable by an absolute constant.

For the corresponding pair forcings, reality gives equal parent amplitudes at \(K\) and \(-K\), hence
\[
|G_{\rm mir}|\ge \frac{p}{2S}|G_{\rm cat}|.
\]
Since the catalyst transfer obeys \(\kappa_\tau=pT_P\),
\[
\boxed{|\kappa_\tau|\le 4S\,|z_{-\sigma}(P)|\,|G_{\rm mir}|}.
\]
Thus the same true nonlinear interaction that creates critical escape necessarily creates an off-channel mirror forcing of comparable normalized size.

## 5. Sparse-family mirror leakage inequality

Consider a dyadic family \(\mathcal T_N\) with parent radii \(N\le k_\tau,q_\tau\le2N\). Let
\[
d_P:=\max_P\#\{\tau\in\mathcal T_N:P_\tau=P\}
\]
be catalyst multiplicity, and define the mirror pair potential
\[
\mathcal P_{\rm mir}:=\sum_{\tau\in\mathcal T_N}|G_{{\rm mir},\tau}|^2.
\]
Summing the pairwise estimate and using Cauchy gives
\[
\boxed{\kappa_{\mathcal T}\le C N d_P^{1/2}E_{-\sigma}^{1/2}\mathcal P_{\rm mir}^{1/2}},
\]
therefore
\[
\boxed{\mathcal P_{\rm mir}\ge c\frac{\kappa_{\mathcal T}^2}{N^2d_PE_{-\sigma}}}.
\]
If the family carries a fixed fraction of a positive event with \(\kappa\gtrsim\nu M_{3,N}\), its mirror pair potential is quantitatively large.

Pair potential is not yet actual forcing because many pairs may share one mirror output. For each output \(m\), let
\[
G_m=\sum_{\alpha=1}^{R_m}g_{m,\alpha},
\qquad
P_m=\sum_\alpha|g_{m,\alpha}|^2,
\]
and
\[
D_m:=R_mP_m-|G_m|^2
=\sum_{\alpha<\beta}|g_{m,\alpha}-g_{m,\beta}|^2.
\]
A simple partition yields the rigorous trichotomy
\[
\boxed{\text{sparse positive escape}\Longrightarrow
\begin{cases}
\text{large actual mirror forcing},\\
\text{large internal many-to-one deficit }\sum_mD_m,\\
\text{or large forcing from additional cross-pairs.}
\end{cases}}
\]
The first branch leaves the sparse skeleton; the second is precisely the projective/Pexider coherence branch; the third means the supposedly sparse dynamics has already densified.

## 6. A finite global budget for actual leakage

For the full nonlinear forcing
\[
F=-P(u\cdot\nabla u),
\]
\[
\|\Lambda^{-1}F\|_2\lesssim\|u\otimes u\|_2=\|u\|_4^2.
\]
The three-dimensional Gagliardo-Nirenberg estimate gives
\[
\|u\|_4\lesssim\|u\|_2^{1/4}\|\nabla u\|_2^{3/4},
\]
so
\[
\boxed{\|\Lambda^{-1}F\|_2^{4/3}\lesssim E^{1/3}Z}.
\]
Using energy dissipation,
\[
\boxed{\int_0^T\|\Lambda^{-1}F(t)\|_2^{4/3}\,dt\lesssim \frac{E_0^{4/3}}{\nu}}.
\]
Hence the actual-leakage branch has a genuine finite a-priori action budget. This exponent alone is not yet sufficient for regularity, but it converts one branch of the sparse-escape trichotomy into an integrably controlled quantity.

## 7. Updated closing target

The remaining endgame is now organized by the true convolution rather than by an isolated triad tree:
\[
\boxed{\text{sparse escape}\Rightarrow\text{mirror/cross-pair leakage or densification/cancellation}.}
\]
A candidate singular cascade must therefore repeatedly move into a dense many-to-one interaction network whenever it avoids the finite leakage budget.

The next proof target is twofold:

1. show that repeated ``large additional cross-pair forcing'' forces effective multiplicity into the dense regime after a quantitatively controlled number of steps;
2. on the dense/cancellation branch, convert the many-to-one deficit into a lower bound for Pexider/projective motion during positive critical flux.

Closing these two statements with scale-invariant constants would connect the sparse mirror-leakage mechanism to the dense coherence-rigidity mechanism. Until then this remains a structural reduction, not a completed Navier–Stokes regularity proof.
