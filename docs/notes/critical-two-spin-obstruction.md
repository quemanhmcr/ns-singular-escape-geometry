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
Where the Gram matrix is nonsingular, this is explicitly the orthogonal projection with
\[
\binom ab=
\begin{pmatrix}E&H\\H&Z\end{pmatrix}^{-1}
\binom KJ,
\qquad
H:=\langle u,\omega\rangle,
\quad J:=\langle\Lambda u,\omega\rangle,
\]
and \(\mathcal Y=Z-(K,J)\begin{pmatrix}E&H\\H&Z\end{pmatrix}^{-1}(K,J)^\top\). At a Gram-degenerate point, \(\omega\) is proportional to \(u\), hence \(\Lambda u\) already lies in their span and \(r=0\); the formulas below are understood by continuity there.
Since \(r\perp u,\omega\) and the Euler forcing \(F=P(u\times\omega)\) satisfies
\[
\langle u,F\rangle=\langle\omega,F\rangle=0,
\]
the critical production is exactly
\[
\boxed{\kappa=\langle\Lambda u,F\rangle=\langle r,F\rangle}.
\]
Put \(\mathcal L=\Lambda-a-b\operatorname{curl}\), so \(r=\mathcal Lu\), and define
\[
\Gamma_r:=\langle\mathcal Lr,F\rangle.
\]
For \(\mathcal Y=\|r\|_2^2\), stationarity of the minimizer and commutation of \(\mathcal L\) with \(\Lambda^2\) give the exact balance
\[
\boxed{\mathcal Y'=2\Gamma_r-2\nu\|\Lambda r\|_2^2}.
\]
The derivatives of \(a,b\) disappear because \(r\perp u,\omega\). For the nonlinear term, \(\mathcal L\) commutes with the Leray projection and
\(\langle r,u\cdot\nabla r\rangle=0\), which gives the exact commutator form
\[
\boxed{
\Gamma_r
=-\langle r,[\Lambda-b\operatorname{curl},u\cdot\nabla]u\rangle.}
\]

This projection yields a second scale-invariant defect action. Set
\[
R:=E\mathcal Y,
\qquad
\mathfrak A_r(I):=\int_I E\,(\Gamma_r)_+\,dt.
\]
Under Navier--Stokes scaling the minimizer obeys \(a_\lambda=\lambda a\), \(b_\lambda=b\), hence \(\mathcal Y_\lambda=\lambda\mathcal Y\) and \((\Gamma_r)_\lambda=\lambda^3\Gamma_r\). Since \(E\) has weight \(-1\), both \(R\) and \(\mathfrak A_r\) are scale invariant. Combining the preceding balance with \(E'=-2\nu Z\) gives
\[
R'=2E\Gamma_r-2\nu E\|\Lambda r\|_2^2-2\nu Z\mathcal Y,
\qquad
R(t)\le R(t_0)+2\mathfrak A_r([t_0,t]).
\]

It also gives a sharper critical barrier. From \(\kappa=\langle r,u\times\omega\rangle\),
\[
|\kappa|\le C_*\mathcal Y^{1/2}Z^{1/2}M_3^{1/2}.
\]
If \(K'>0\), then \(\kappa>\nu M_3\). Using \(Z^2\le KM_3\) and \(Z\ge K^2/E\), one obtains
\[
\boxed{
|\nu_E|\le C_*\sqrt{\frac RK},
\qquad
K'>0\ \Longrightarrow\ R>\frac{\nu^2}{C_*^2}K.}
\]
Consequently, if \(R_*:=R(t_0)+2\mathfrak A_r([t_0,T))<\infty\), then \(K'\le0\) whenever \(K\ge R_*/a\), where \(a=\nu^2/C_*^2\). A first-crossing argument proves
\[
\boxed{\sup_{t_0\le t<T}K(t)\le\max\{K(t_0),R_*/a\}.}
\]
More locally, if \(K(t_0)<L\) and \(t_L\) is the first upward hitting time of \(L\), smoothness supplies positive-growth times approaching \(t_L\). The barrier then gives \(\sup_{[t_0,t_L]}R\ge aL\), hence
\[
\boxed{\mathfrak A_r([t_0,t_L])\ge\frac12\bigl(aL-R(t_0)\bigr)_+.}
\]
Thus critical-norm escape forces \(\mathfrak A_r([0,T_*))=\infty\), with a linear scale-invariant action cost for every new critical level.

This is not a closure: \(\Gamma_r\) is a two-invariant centered commutator, not automatically the same production as \(\Gamma_{\rm sp}\). It is, however, the cleanest entropy presently available: it removes both Euler-tangent directions before measuring escape, and needs no separate spin-mixing or reset term once its action is controlled.

The entropy retains an exact triadic symbol. For a helical triad with transfer rates \(T_i\), put
\[
\ell_i:=(1-\sigma_i b)|k_i|-a.
\]
Its Euler contribution is exactly
\[
\boxed{2\Gamma_{r,\tau}=\sum_{i\in\tau}\ell_i^2T_i.}
\]
For a homochiral triad of sign \(\sigma\), energy and helicity cancel the constant and linear parts of \(\ell_i^2\), leaving
\[
\boxed{
2\Gamma_{r,\tau}
=(1-\sigma b)^2(p-k)(q-k)(p-q)J.}
\]
Thus the two-invariant defect preserves the cubic radial-difference depletion of homochiral leakage. The heterochiral part, where the three \(\ell_i\) have different signed slopes, is exactly the remaining symbol-aware network problem.

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

## 4. Corrected sum-mirror lemma

Let \(K^\sigma,Q^\sigma\) be same-helicity modes with
\[
q:=|Q|>k:=|K|,
\qquad
P:=Q-K,\ p:=|P|,
\qquad
M:=Q+K,\ m:=|M|.
\]
Put
\[
S=q+k,\qquad \Delta=q-k,\qquad A=|Q\times K|.
\]
For \(a+b=c\), the normalized helical coefficient has modulus proportional to
\[
 |s_a a-s_b b|\frac{|a\times b|}{abc}
 |s_a a+s_b b+s_c c|.
\]
This follows by expanding in the helical frame adapted to the triad plane. Hence the \(-\sigma\)-catalyst at \(P\) and the **same-spin** sum output at \(M\) satisfy, up to the same universal factor,
\[
|C_{\rm cat}|=\Delta\frac{A}{pqk}(S-p),
\qquad
|C_{\rm sum}|=\Delta\frac{A}{mqk}(S+m).
\]
Therefore
\[
\boxed{\frac{|C_{\rm sum}|}{|C_{\rm cat}|}=\frac{p(S+m)}{m(S-p)}}.
\]
Since \(p,m\le S\),
\[
\boxed{|C_{\rm sum}|\ge \frac{p}{S}|C_{\rm cat}|}.
\]

The opposite-spin output at \(M\) instead carries \(S-m\), and its ratio to the catalyst vanishes for nearly aligned parents. It cannot supply a uniform mirror bound.

For the corresponding pair forcings, reality gives equal parent amplitudes at \(K\) and \(-K\), hence
\[
|G_{\rm sum}|\ge \frac{p}{S}|G_{\rm cat}|.
\]
Since the catalyst transfer obeys \(\kappa_\tau=pT_P\),
\[
\boxed{|\kappa_\tau|\le C S\,|z_{-\sigma}(P)|\,|G_{\rm sum}|}.
\]
Thus a critical catalyst forces a same-spin sum potential. The sum triad is homochiral, so it is leakage rather than a second source of \(K\)-production.

## 5. Pair potential, reset, and diamond propagation

Consider a dyadic family \(\mathcal T_N\) with parent radii \(N\le k_\tau,q_\tau\le2N\). Let
\[
d_P:=\max_P\#\{\tau\in\mathcal T_N:P_\tau=P\}
\]
be catalyst multiplicity, and define the sum-mirror pair potential
\[
\mathcal P_{\rm sum}:=\sum_{\tau\in\mathcal T_N}|G_{{\rm sum},\tau}|^2.
\]
For a selected positive family, write \(\kappa_{\mathcal T}:=\sum_{\tau\in\mathcal T_N}\kappa_\tau\).
Summing the pairwise estimate and using Cauchy gives
\[
\boxed{\kappa_{\mathcal T}\le C N d_P^{1/2}E_{-\sigma}^{1/2}\mathcal P_{\rm sum}^{1/2}},
\]
therefore
\[
\boxed{\mathcal P_{\rm sum}\ge c\frac{\kappa_{\mathcal T}^2}{N^2d_PE_{-\sigma}}}.
\]
If the family carries a fixed fraction of a positive event with \(\kappa\gtrsim\nu M_{3,N}\), its sum-mirror pair potential is quantitatively large.

Pair potential is not yet actual forcing because many pairs may share one sum output. For each output \(m\), let
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
This is an algebraic decomposition, not yet a global trichotomy.

Two exact local facts sharpen the cancellation branch. First, for one positive handoff set \(e_K=|z_\sigma(K)|^2\), \(e_Q=|z_\sigma(Q)|^2\), and \(\rho=e_Q/e_K\). Then
\[
(\log\rho)'_\tau
=-J\left(\frac{p+k}{e_Q}+\frac{q+p}{e_K}\right)>0,
\qquad
\Gamma_{\sigma,\tau}>0
\Longleftrightarrow
\rho<\sqrt{\frac{p+k}{q+p}}.
\]
Positive flux therefore exhausts a finite variance-recharge window unless another triad resets \(\rho\). Its full centered contribution is
\[
\boxed{
2\Gamma_{{\rm sp},\tau}
=\frac{\kappa_\tau}{p}
\left[p(S-2m_\sigma)+kq-m_\sigma^2+(p-m_{-\sigma})^2\right].
}
\]
The bracket has no fixed sign, so a pointwise \(\kappa>0\Rightarrow\Gamma_{\rm sp}>0\) argument is unavailable.

Second, if two sum-pair contributions \(g_1,g_2\) share an output and
\[
|g_1+g_2|^2\le\eta^2(|g_1|^2+|g_2|^2),\qquad \eta<1,
\]
their additive diamond \(D=Q_1-Q_2=K_2-K_1\) has cross-pair contributions \(h_Q,h_K\) obeying
\[
\boxed{
\max\{|h_Q|^2,|h_K|^2\}
\ge\frac{1-\eta^2}{2}
\frac{|C_QC_K|}{|C_1C_2|}(|g_1|^2+|g_2|^2).
}
\]
Thus substantial two-pair cancellation propagates pair potential unless the relevant coefficient ratio is degenerate.

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

## 7. Closing target

The corrected sparse conclusion is organized by the true convolution rather than by an isolated triad tree:
\[
\boxed{\text{selected positive escape}\Rightarrow\text{same-spin sum-mirror pair potential}.}
\]
Static cancellation/diamond algebra does not yet close this implication: an exact two-pair state has \(\kappa>0\), a symmetry-protected vanishing sum output, and \(\Gamma_{\rm sp}<0\) at the same instant; arbitrarily long scalar cancellation ladders also defeat a uniform graph-only forcing bound. See `docs/notes/network-closure-audit.md`.

The remaining lemma must therefore be genuinely dynamical and symbol-aware: it must control weighted cancellation ladders and the subsequent cross-output evolution with scale-consistent localization, then convert that cost into the two-invariant action \(\mathfrak A_r<\infty\), or into \((\Gamma_{\rm sp})_+\in L^1_t\) for the Riccati route. This is still unproved.

There is also a complementary total-defect route: the scale-invariant relative defect \(Q=D/K\) has a logarithmic barrier cost on monotone epochs that follow the critical-growth barrier. It reduces the remaining work to controlling broad-defect bypasses and reset intervals; see `docs/notes/network-closure-audit.md`.
