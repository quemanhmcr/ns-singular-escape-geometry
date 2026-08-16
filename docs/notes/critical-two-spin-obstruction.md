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

Let \(\alpha,\beta\) minimize
\[
\|\Lambda u-\alpha u-\beta\omega\|_2^2,
\qquad
r:=\Lambda u-\alpha u-\beta\omega.
\]
Where the Gram matrix is nonsingular, this is explicitly the orthogonal projection with
\[
\binom\alpha\beta=
\begin{pmatrix}E&H\\H&Z\end{pmatrix}^{-1}
\binom K{J_\omega},
\qquad
H:=\langle u,\omega\rangle,
\quad J_\omega:=\langle\Lambda u,\omega\rangle,
\]
and \(\mathcal Y=Z-(K,J_\omega)\begin{pmatrix}E&H\\H&Z\end{pmatrix}^{-1}(K,J_\omega)^\top\). At a Gram-degenerate point, \(\omega\) is proportional to \(u\), hence \(\Lambda u\) already lies in their span and \(r=0\); the formulas below are understood by continuity there.
Since \(r\perp u,\omega\) and the Euler forcing \(F=P(u\times\omega)\) satisfies
\[
\langle u,F\rangle=\langle\omega,F\rangle=0,
\]
the critical production is exactly
\[
\boxed{\kappa=\langle\Lambda u,F\rangle=\langle r,F\rangle}.
\]
Put \(\mathcal L=\Lambda-\alpha-\beta\operatorname{curl}\), so \(r=\mathcal Lu\), and define
\[
\Gamma_r:=\langle\mathcal Lr,F\rangle.
\]
For \(\mathcal Y=\|r\|_2^2\), stationarity of the minimizer and commutation of \(\mathcal L\) with \(\Lambda^2\) give the exact balance
\[
\boxed{\mathcal Y'=2\Gamma_r-2\nu\|\Lambda r\|_2^2}.
\]
The derivatives of \(\alpha,\beta\) disappear because \(r\perp u,\omega\). For the nonlinear term, \(\mathcal L\) commutes with the Leray projection and
\(\langle r,u\cdot\nabla r\rangle=0\), which gives the exact commutator form
\[
\boxed{
\Gamma_r
=-\langle r,[\Lambda-\beta\operatorname{curl},u\cdot\nabla]u\rangle.}
\]

This projection yields a second scale-invariant defect action. Set
\[
R:=E\mathcal Y,
\qquad
\mathfrak A_r(I):=\int_I E\,(\Gamma_r)_+\,dt.
\]
Under Navier--Stokes scaling the minimizer obeys \(\alpha_\lambda=\lambda\alpha\), \(\beta_\lambda=\beta\), hence \(\mathcal Y_\lambda=\lambda\mathcal Y\) and \((\Gamma_r)_\lambda=\lambda^3\Gamma_r\). Since \(E\) has weight \(-1\), both \(R\) and \(\mathfrak A_r\) are scale invariant. Combining the preceding balance with \(E'=-2\nu Z\) gives
\[
R'=2E\Gamma_r-2\nu E\|\Lambda r\|_2^2-2\nu Z\mathcal Y,
\qquad
R(t)\le R(t_0)+2\mathfrak A_r([t_0,t]).
\]

It also gives a sharper critical barrier. From \(\kappa=\langle r,u\times\omega\rangle\),
\[
|\kappa|\le C_*\mathcal Y^{1/2}Z^{1/2}M_3^{1/2}.
\]
Using \(Z^2\le KM_3\) and \(Z\ge K^2/E\), one obtains
\[
\boxed{
|\nu_E|\le C_*\sqrt{\frac RK},
\qquad
K'>0\ \Longrightarrow\ R>\frac{\nu^2}{C_*^2}K.}
\]
More importantly, optimizing the same estimate in \(M_3^{1/2}\) gives the pointwise growth--dissipation charge
\[
\boxed{
K'_+\le\frac{C_*^2}{2\nu}Z\mathcal Y
=\frac{\nu}{2a}Z\mathcal Y,
\qquad a:=\frac{\nu^2}{C_*^2}.}
\]
This turns the \(R\)-balance into an exact Perelman-style monotonicity identity. For \(I=[t_0,t_1]\), write
\[
\mathfrak A_r^-(I):=\int_I E\,(\Gamma_r)_-\,dt,
\qquad
\operatorname{Var}^+_I K:=\int_I(K')_+\,dt.
\]
Then
\[
\boxed{
\begin{aligned}
R(t_1)&+4a\operatorname{Var}^+_I K
+2\nu\int_I E\|\Lambda r\|_2^2dt
+2\mathfrak A_r^-(I)\\
&+\int_I\bigl(2\nu Z\mathcal Y-4a(K')_+\bigr)dt
=R(t_0)+2\mathfrak A_r(I).
\end{aligned}}
\]
Every term on the left is nonnegative. It follows in particular that
\[
\boxed{
\operatorname{Var}^+_I K
\le\frac{R(t_0)+2\mathfrak A_r(I)}{4a},
\qquad
K(t)\le K(t_0)+\frac{R(t_0)+2\mathfrak A_r([t_0,t])}{4a}.}
\]
Equivalently, every relative level crossing \(K(t_1)\ge(1+\eta)K(t_0)\) obeys the scale-invariant epsilon-cost bound
\[
\boxed{R(t_0)+2\mathfrak A_r([t_0,t_1])\ge4a\eta K(t_0).}
\]
Thus critical-norm escape forces \(\mathfrak A_r([0,T_*))=\infty\), with a linear scale-invariant cost for the **total** upward variation of \(K\). In particular, nonmonotone reset intervals cannot evade this charge.

### A forcing-level action that closes directly

The commutator action has a more concrete sufficient replacement. Since
\[
\Gamma_r=\langle\Lambda r,\Lambda^{-1}\mathcal L F\rangle,
\]
define the normal-forcing action
\[
\boxed{
\mathfrak N_r(I):=
\int_I E\,\|\Lambda^{-1}\mathcal L F\|_2^2dt.}
\]
It is scale invariant. (The zero mode causes no issue because the Euler forcing has zero spatial mean.) Young's inequality in the exact \(R\)-balance gives
\[
\boxed{
R(t_1)+\nu\int_I E\|\Lambda r\|_2^2dt
+2\nu\int_I Z\mathcal Ydt
\le R(t_0)+\nu^{-1}\mathfrak N_r(I).}
\]
Combining this with \(4a(K')_+\le2\nu Z\mathcal Y\) yields the direct no-reset estimate
\[
\boxed{
\operatorname{Var}^+_I K
\le\frac{R(t_0)+\nu^{-1}\mathfrak N_r(I)}{4a}.}
\]
Thus \(\mathfrak N_r([0,T_*))<\infty\) alone rules out critical-norm escape. It also implies \(\mathfrak A_r(I)\le R(t_0)/2+\mathfrak N_r(I)/\nu\).

This is the natural all-network target because it sees **actual** normal forcing rather than pair potential. In helical Fourier variables,
\[
\|\Lambda^{-1}\mathcal L F\|_2^2
=\sum_{k\ne0,\,\sigma}
\left|\frac{\ell_\sigma(k)}{|k|}\right|^2
|\widehat F_\sigma(k)|^2.
\]
At an exact two-shell profile, the on-shell multipliers vanish, so this is precisely the relative off-shell forcing cost. A valid cancellation/diamond theorem must bound this action; no such bound is proved here.

### A lower-time-integrability critical normal action

There is an independent endpoint that closes the critical norm directly, without first evolving \(r\). Self-adjointness gives
\[
\kappa=\langle\mathcal Lu,F\rangle
=\langle\Lambda u,\Lambda^{-1}\mathcal LF\rangle.
\]
Write
\[
b_r(t):=\|\Lambda^{-1}\mathcal LF(t)\|_2.
\]
All following identities are read on a component of \(\{K>0\}\); after removing a torus mean, \(K=0\) is the trivial non-escaping case.
Then \,\(|\kappa|\le Z^{1/2}b_r\), and \(Z^2\le KM_3\) in the exact critical balance yields
\[
K'
\le2Z^{1/2}b_r-\frac{2\nu}{K}Z^2.
\]
For \(K>0\), maximizing the right side over \(Z\ge0\) gives the sharp scalar estimate
\[
\boxed{
K'_+
\le\frac{3}{2^{5/3}}\nu^{-1/3}K^{1/3}b_r^{4/3}.}
\]
Consequently the critical normal-forcing action
\[
\boxed{
\mathfrak C_r(I):=\int_I
\|\Lambda^{-1}\mathcal LF\|_2^{4/3}dt}
\]
is scale invariant and obeys
\[
\boxed{
\bigl(K(t_1)^{2/3}-K(t_0)^{2/3}\bigr)_+
\le2^{-2/3}\nu^{-1/3}\mathfrak C_r(I).}
\]
In fact this is an exact three-defect identity. Set
\[
\Delta_K:=KM_3-Z^2\ge0.
\]
Define the scalar-optimization and forcing-alignment deficits by
\[
\mathcal S_r:=
\frac{3}{2^{5/3}}\nu^{-1/3}K^{1/3}b_r^{4/3}
-2Z^{1/2}b_r+\frac{2\nu Z^2}{K}\ge0,
\qquad
\mathcal A_r^{\rm al}:=Z^{1/2}b_r-\kappa\ge0.
\]
The first nonnegativity is precisely the scalar maximization above; the second is Cauchy--Schwarz. Splitting \(M_3=Z^2/K+\Delta_K/K\) in the exact \(K\)-balance gives
\[
\boxed{
\frac{3}{2^{5/3}}\nu^{-1/3}K^{1/3}b_r^{4/3}-K'
=\mathcal S_r+2\mathcal A_r^{\rm al}+\frac{2\nu}{K}\Delta_K.}
\]
After division by \(K^{1/3}\) and integration, this becomes the scale-invariant monotonicity identity
\[
\boxed{
2^{-2/3}\nu^{-1/3}\mathfrak C_r(I)
-\bigl(K(t_1)^{2/3}-K(t_0)^{2/3}\bigr)
=\frac23\int_I K^{-1/3}
\left(\mathcal S_r+2\mathcal A_r^{\rm al}+\frac{2\nu}{K}\Delta_K\right)dt
\ge0.}
\]
More sharply, no cost need be charged when \(K\) is decreasing. Define the growth-selected action
\[
\boxed{
\mathfrak C_r^\uparrow(I):=
\int_{I\cap\{K'>0\}}
\|\Lambda^{-1}\mathcal LF\|_2^{4/3}dt.}
\]
Restricting the same exact identity to \(\{K'>0\}\) gives
\[
\boxed{
2^{-2/3}\nu^{-1/3}\mathfrak C_r^\uparrow(I)
-\operatorname{Var}_I^+\!\bigl(K^{2/3}\bigr)
=\frac23\int_{I\cap\{K'>0\}}K^{-1/3}
\left(\mathcal S_r+2\mathcal A_r^{\rm al}+\frac{2\nu}{K}\Delta_K\right)dt
\ge0.}
\]
Thus any critical-norm escape forces
\(\mathfrak C_r^\uparrow([0,T_*))=\infty\), and this is the escape-adapted normal-forcing target for a cancellation/diamond theorem. It has the same \(4/3\) time exponent as the existing finite budget for \(\|\Lambda^{-1}F\|_2\), but it measures the symbol-filtered normal forcing \(\Lambda^{-1}\mathcal LF\). The missing estimate is exactly this one-spatial-derivative normal gain; it is not supplied by the energy budget or by static diamond incidence.

The endpoint has a rigid equality case. If \(d\mu(\rho)\) is the radial energy measure, then
\[
\Delta_K
=\frac12\iint \rho\eta(\rho-\eta)^2\,d\mu(\rho)d\mu(\eta).
\]
Hence, after removing the harmless torus mean, \(\Delta_K=0\) forces one radial shell. On that shell \(r=0\), hence \(\kappa=0\). Equality in the preceding \(\mathfrak C_r\)-growth bound is therefore impossible at an instant with \(K'>0\). An action-minimizing escape would have to approach this forbidden equality: one-shell radial concentration, forcing alignment \(\Lambda^{-1}\mathcal LF\parallel\Lambda u\), and the optimizing relation \(Z=(Kb_r/(4\nu))^{2/3}\). Turning this exact rigidity into a quantitative compactness--rigidity exclusion is the remaining step.

The exact equality case is already rigid. If all nonnegative defect terms in the monotonicity identity other than \(4a\operatorname{Var}^+_I K\) vanish, then \(\int_I E\|\Lambda r\|_2^2dt=0\). Thus \(r=0\) on \(\mathbb R^3\), and is at most a constant torus mode in the periodic case. In either case \(\kappa=\langle r,F\rangle=0\), since the Euler forcing has zero spatial mean, and \(K'=-2\nu M_3\le0\). Therefore no interval with positive upward variation can be an exact action minimizer. The remaining Perelman-style task is a compactness--rigidity theorem excluding an **asymptotically** saturating sequence; that theorem is not supplied here.

There is also an exact two-invariant shell-acceleration identity. At a nondegenerate instant with \(r=0\), let \(P_\perp\) be the orthogonal projection off \(\operatorname{span}\{u,\omega\}\). Differentiating the two normal equations for the minimizing \(\alpha,\beta\) gives
\[
r_t=P_\perp\mathcal L F.
\]
Indeed, \(\mathcal L\Lambda^2u=\Lambda^2\mathcal Lu=0\), so the viscous vector is tangent to the two-invariant shell manifold at that instant. Consequently,
\[
\boxed{
\mathcal Y'=0,
\qquad
\mathcal Y''=2\|P_\perp\mathcal L F\|_2^2\quad\text{when }r=0.}
\]
This has a direct Fourier leakage form. Put
\[
\ell_\sigma(k):=(1-\sigma\beta)|k|-\alpha,
\qquad
\mathcal S_{\alpha,\beta}:=\{(k,\sigma):\ell_\sigma(k)=0\}.
\]
At \(r=0\), \(u\) is supported on \(\mathcal S_{\alpha,\beta}\), whereas \(\operatorname{span}\{u,\omega\}\) has no off-shell component. Hence, on the torus (with the corresponding integral on \(\mathbb R^3\)),
\[
\boxed{
\mathcal Y''
\ge2\sum_{(k,\sigma)\notin\mathcal S_{\alpha,\beta}}
|\ell_\sigma(k)|^2|\widehat F_\sigma(k)|^2
\quad\text{when }r=0.}
\]
Thus the relevant leakage is not a cancelled sum output itself, but the symmetry-compatible **off-shell normal forcing**. This is the exact dynamic quantity a network rigidity theorem must charge.

This is not a closure: \(\Gamma_r\) is a two-invariant centered commutator, not automatically the same production as \(\Gamma_{\rm sp}\). It is, however, the cleanest entropy presently available: it removes both Euler-tangent directions before measuring escape, and needs no separate spin-mixing or reset term once its action is controlled.

### Spectral compactness datum for a minimal-action escape

The projection has an exact probability interpretation. Normalize Fourier energy to a probability measure, let \(X=|\xi|\), \(S=\sigma|\xi|\), and write \(m=\mathbb E X=K/E\), \(h=\mathbb E S=H/E\). The coefficients above are the least-squares regression of \(X\) on \(1,S\):
\[
\beta=\frac{\operatorname{Cov}(X,S)}{\operatorname{Var}(S)},
\qquad
\alpha=m-\beta h.
\]
Since \(X^2=S^2\), \(\operatorname{Var}(X)\le\operatorname{Var}(S)\); Cauchy--Schwarz and \(m\ge|h|\) therefore give
\[
\boxed{|\beta|\le1,\qquad 0\le\frac\alpha m\le2.}
\]
The Gram-degenerate case is the already rigid \(r=0\) case.

For \(y=|\xi|/m\), let \(\mu_\sigma\) be the energy-normalized radial spectral measure of \(u_\sigma\). The relative two-invariant defect has the exact form
\[
\boxed{
\frac{R}{K^2}
=\sum_{\sigma=\pm}\int
\left((1-\sigma\beta)y-\frac\alpha m\right)^2d\mu_\sigma(y).}
\]
Consequently, for every \(\varepsilon>0\),
\[
\sum_{\sigma=\pm}
\mu_\sigma\!\left\{
\left|(1-\sigma\beta)y-\frac\alpha m\right|>\varepsilon\right\}
\le\frac{R}{\varepsilon^2K^2}.
\]
Thus \(R/K^2\ll1\) concentrates the normalized spectrum near one affine shell constraint in each helicity. If \(1-\sigma\beta\) stays away from zero this is genuine two-shell radial concentration; the only degenerate branch is \(\beta\to\pm1\), the almost pure-helicity branch.

This is exactly the compactness input for a Perelman-style minimal-action argument. Indeed, if \(K(t_n)\to\infty\) while \(\mathfrak A_r([0,t_n])\le C K(t_n)\), then the \(R\)-balance gives \(R(t_n)\le R(0)+2CK(t_n)\), hence \(R(t_n)/K(t_n)^2\to0\). The normalized measures have first moment one and are therefore tight; after taking a subsequence, they have the two-shell (or degenerate pure-helicity) profile above. What is still missing is a symbol-aware phase/localization rigidity theorem excluding that limiting profile while it carries positive critical production.

The entropy retains an exact triadic symbol. For a helical triad with transfer rates \(T_i\), put
\[
\ell_i:=(1-\sigma_i\beta)|k_i|-\alpha.
\]
Its Euler contribution is exactly
\[
\boxed{2\Gamma_{r,\tau}=\sum_{i\in\tau}\ell_i^2T_i.}
\]
For a homochiral triad of sign \(\sigma\), energy and helicity cancel the constant and linear parts of \(\ell_i^2\), leaving
\[
\boxed{
2\Gamma_{r,\tau}
=(1-\sigma\beta)^2(p-k)(q-k)(p-q)J.}
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
