# Network-closure audit: the missing lemma is genuinely dynamical

**Date:** 2026-08-16
**Claim level:** exact obstruction checks. This note does not prove Navier–Stokes regularity.

The proposed closing step would turn repeated sum-output cancellation and diamond propagation into a finite spacetime cost, ideally
\((\Gamma_{\rm sp})_+\in L^1_t\). The finite-triad identities do not yet give such a theorem. The checks below isolate why a static all-network argument cannot do so.

## 1. The raw \(\Gamma_{\rm sp}\) action is scale covariant, not invariant

Set \(m_\sigma=K_\sigma/E_\sigma\), \(W_\sigma=\|(\Lambda-m_\sigma)u_\sigma\|_2^2\), and
\[
\Gamma_{\rm sp}=\sum_{\sigma=\pm}
\langle(\Lambda-m_\sigma)^2u_\sigma,F_\sigma\rangle.
\]
Under \(u_\lambda(x,t)=\lambda u(\lambda x,\lambda^2t)\),
\[
m_{\sigma,\lambda}=\lambda m_\sigma,
\qquad W_{\sigma,\lambda}=\lambda W_\sigma,
\qquad \Gamma_{{\rm sp},\lambda}=\lambda^3\Gamma_{\rm sp}.
\]
Consequently
\[
\boxed{
\int_{I_\lambda}(\Gamma_{{\rm sp},\lambda})_+\,dt
=\lambda\int_I(\Gamma_{\rm sp})_+\,dt.}
\]
Finiteness of this integral is preserved by scaling, but its value is not. Thus a scale-invariant network lemma cannot be a uniform bound for the raw action in terms of scale-invariant data alone. It must either produce a scale-covariant estimate with dimensionful data, or first control a normalized action; for example, where \(m=K/E>0\),
\[
\int_I\frac{(\Gamma_{\rm sp})_+}{E m^2}\,dt
\]
is scale invariant. No implication from this normalized quantity to the required raw \(L^1_t\) action is presently proved.

## 2. An exact finite Fourier state defeats instantaneous coercivity

Work on \(\mathbb T^3\), and for a nonzero \(k=(a,b,0)\) use the helical frame
\[
h_s(k)=\frac1{\sqrt2}
\left(\frac{(-b,a,0)}{|k|}+is e_3\right),
\qquad i k\times h_s(k)=s|k|h_s(k).
\]
Let
\[
\begin{aligned}
K_1&=(1,1,0),& Q_1&=(3,-1,0),& P_1&=(2,-2,0),\\
K_2&=(1,-1,0),& Q_2&=(3,1,0),& P_2&=(2,2,0),
\end{aligned}
\qquad M=(4,0,0),
\]
so \(Q_i=K_i+P_i\) and \(M=K_i+Q_i\). Define a real finite Fourier field by
\[
\widehat u(K_i)=h_+(K_i),\quad
\widehat u(Q_i)=h_+(Q_i),\quad
\widehat u(P_1)=i h_-(P_1),\quad
\widehat u(P_2)=-i h_-(P_2),
\]
with \(\widehat u(-k)=\overline{\widehat u(k)}\) and all other coefficients zero.

The two same-spin pair contributions to the sum output are exactly opposite:
\[
F_M^{(K_1,Q_1)}=
\left(0,\frac{2\sqrt5}{5}i,-\sqrt2+\frac{\sqrt{10}}5\right)
=-F_M^{(K_2,Q_2)}.
\]
The remaining possible pair, \((P_1,P_2)\), is equal-radius homochiral and has zero coefficient. Hence
\[
\boxed{F_M=0.}
\]
For \(T_\ell=2\operatorname{Re}(\overline{\widehat u(\ell)}\cdot F_\ell)\) at either positive representative \(i=1,2\), the exact transfer table is
\[
\begin{array}{c|ccc}
\ell & K_i & Q_i & P_i\\ \hline
T_\ell & -1-\frac{3\sqrt5}{5} & 3-\frac{3\sqrt5}{5} & -2+\frac{6\sqrt5}{5}.
\end{array}
\]
In particular, the two catalyst currents have
\[
T_{P_i}=-2+\frac{6\sqrt5}{5}>0,
\]
so both handoffs have positive critical production. Directly,
\[
\kappa=\frac{48\sqrt{10}}5-16\sqrt2>0.
\]
On the other hand,
\[
E_+=8,\quad E_-=4,\quad
m_+=\frac{\sqrt2+\sqrt{10}}2,\quad m_-=2\sqrt2,
\]
and the exact within-spin production is
\[
\boxed{\Gamma_{\rm sp}=24-\frac{56\sqrt5}{5}<0.}
\]
Equivalently, in the positive-handoff formula of the critical note, its bracket is
\[
kq-\left(\frac{k+q}{2}\right)^2
=-\frac{(q-k)^2}{4}<0,
\]
because both catalysts have radius \(p=m_-\).

The diamond conclusion still occurs: the cross outputs satisfy
\[
|F_{(4,2,0)}|^2=|F_{(4,-2,0)}|^2
=\frac{19-5\sqrt5}{25}>0.
\]
Thus this is not a counterexample to diamond propagation. It proves the sharper fact that positive escape plus exact sum-output cancellation cannot yield a **pointwise** positive lower bound for \(\Gamma_{\rm sp}\). A closing lemma must charge the subsequent dynamics of the cross outputs.

### The cancellation can be symmetry-protected for all smooth time

This example is not merely an instantaneous phase accident. On the \(2\pi\)-periodic torus, let
\[
S=\operatorname{diag}(1,-1,-1),\qquad a=(\pi,0,0),
\qquad (\mathcal Gu)(x)=S u(Sx+a).
\]
The displayed initial field satisfies
\[
\widehat u(k)=(-1)^{k_1}S\widehat u(Sk),
\qquad\text{equivalently}\qquad \mathcal Gu=u.
\]
The Navier–Stokes vector field commutes with \(\mathcal G\); smooth uniqueness therefore preserves this relation. At \(M=(4,0,0)\), it gives
\[
\widehat u(M,t)=S\widehat u(M,t),\qquad
\widehat F(M,t)=S\widehat F(M,t).
\]
Both coefficients are divergence-free and perpendicular to \(M\), while \(S\) acts as \(-1\) on that plane. Hence
\[
\boxed{\widehat u(M,t)=\widehat F(M,t)=0}
\]
throughout every interval of smooth existence. In particular, a universal transversality estimate based on \(\partial_tF_M\) is false; the cost, if any, must be read from symmetry-compatible cross outputs or another dynamical quantity.

## 3. Diamond topology alone has no uniform forcing coercivity

For \(L\ge1\), consider the scalar convolution data on \(\mathbb Z\)
\[
a=(1,-1),\qquad b=(\underbrace{1,\ldots,1}_{L+1\ \mathrm{terms}}),
\qquad g=a*b.
\]
Every interior output is a two-pair cancellation,
\[
g_n=a_0b_n+a_1b_{n-1}=1-1=0,
\qquad 1\le n\le L,
\]
and these relations form a chain of additive diamonds. Yet
\[
\sum_n|g_n|^2=2,
\qquad
\mathcal P:=\sum_{i,j}|a_i b_j|^2=2(L+1),
\qquad
\boxed{\frac{\|g\|_{\ell^2}^2}{\mathcal P}=\frac1{L+1}.}
\]
There is therefore no graph-theoretic constant converting pair potential to actual forcing after arbitrarily many diamond steps.

The same algebra survives nonzero weighted coefficients: if an interior output is
\[
C_{0,n}a_0b_n+C_{1,n-1}a_1b_{n-1},
\]
then the recurrence
\[
b_n=-\frac{C_{1,n-1}a_1}{C_{0,n}a_0}\,b_{n-1}
\]
cancels it exactly. Controlling the resulting weights is a new analytic problem; it cannot follow from additive-diamond incidence alone.

## 4. The corrected closing target

A viable all-network lemma must add information absent from the current static reductions:

1. a fixed, scale-consistent packet/localization framework rather than bare mode multiplicities;
2. a symbol-aware estimate that controls weighted cancellation ladders, not only their incidence graph;
3. a time-dependent estimate that charges symmetry-compatible cross-output evolution, without assuming transversality of the cancelled output; and
4. a bridge from the resulting normalized action to the raw \((\Gamma_{\rm sp})_+\in L^1_t\) needed by the Riccati argument.

Until all four are supplied, the desired full-network lemma remains unproved. The finite calculations above prevent treating its conclusion as a consequence of the present cancellation/diamond identities.
