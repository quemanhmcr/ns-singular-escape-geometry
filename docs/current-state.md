# Current State of the Argument

Snapshot date: 2026-08-15.

## 1. Navier–Stokes in rotational/Leray form

For smooth divergence-free \(u\) on \(\mathbb R^3\) (or a periodic domain, with the corresponding Fourier interpretation),

\[
u_t+(u\cdot\nabla)u=-\nabla p+\nu\Delta u,
\qquad \nabla\cdot u=0.
\]

Using \((u\cdot\nabla)u=\nabla(|u|^2/2)-u\times\omega\), \(\omega=\nabla\times u\), and the Leray projector \(P\), define

\[
F:=P(u\times\omega).
\]

Then

\[
u_t=F-\nu\Lambda^2u,
\qquad \Lambda=(-\Delta)^{1/2},
\]

and

\[
\langle u,F\rangle=0.
\]

Hence the nonlinear Euler direction is tangent to the \(L^2\) energy shell.

## 2. Basic moments and energy confinement

Define

\[
E=\|u\|_2^2,
\qquad
K=\langle u,\Lambda u\rangle=\|\Lambda^{1/2}u\|_2^2,
\qquad
Z=\|\Lambda u\|_2^2,
\]

\[
M_3=\|\Lambda^{3/2}u\|_2^2,
\qquad
M_4=\|\Lambda^2u\|_2^2.
\]

Then

\[
E'=-2\nu Z\le 0.
\]

The energy remains bounded, so any hypothetical blow-up must escape in a stronger topology, naturally interpreted as motion toward high frequency while remaining inside an energy ball.

## 3. Canonical centered spectral direction

Set

\[
m=\frac KE,
\qquad
s=(\Lambda-m)u.
\]

Then

\[
\langle u,s\rangle=0,
\]

and exactly

\[
\|s\|_2^2
=Z-\frac{K^2}{E}
=\frac{EZ-K^2}{E}.
\]

Define

\[
D:=EZ-K^2\ge 0,
\qquad
\delta:=\frac{D}{EZ}=1-\frac{K^2}{EZ}.
\]

In Fourier variables, \(m\) is the energy-weighted mean radial frequency and \(D/E^2\) is the corresponding radial-frequency variance.

## 4. Exact escape coupling

Define

\[
\kappa:=\langle s,F\rangle.
\]

Because \(\langle u,F\rangle=0\),

\[
\kappa=\langle \Lambda u,F\rangle.
\]

Because \(s\) is divergence-free,

\[
\kappa
=\langle s,u\times\omega\rangle
=\langle \omega,s\times u\rangle.
\]

Thus the unnormalized escape action is

\[
A_{\rm escape}=|\kappa|^2
=|\langle \omega,s\times u\rangle|^2.
\]

This detects a genuinely three-dimensional alignment between vorticity, velocity, and the centered spectral direction.

## 5. Exact critical-norm balance and Euler viscosity

Differentiate \(K\):

\[
K'=2\langle \Lambda u,F\rangle-2\nu\langle\Lambda u,\Lambda^2u\rangle.
\]

Therefore

\[
K'=2\kappa-2\nu M_3.
\]

Define

\[
\nu_E:=\frac{\kappa}{M_3}.
\]

Then

\[
\boxed{K'=2M_3(\nu_E-\nu)}.
\]

Interpretation: \(\nu_E\) is the nonlinear production coefficient expressed in viscosity units. The sign of \(K'\) is controlled by \(\nu_E-\nu\).

## 6. Critical spectral-defect barrier

From

\[
|\kappa|\le \|s\|_2\,\|u\|_6\,\|\omega\|_3,
\]

Sobolev estimates give

\[
|\kappa|
\le C_*\sqrt{\frac DE}\,Z^{1/2}M_3^{1/2}.
\]

Using

\[
Z^2\le KM_3,
\]

we obtain

\[
\boxed{
|\nu_E|
\le C_*\sqrt{K\left(1-\frac{K^2}{EZ}\right)}
=C_*\sqrt{\frac{KD}{K^2+D}}.
}
\]

Hence, if \(K'>0\), then necessarily \(\nu_E>\nu\), so with \(a:=\nu^2/C_*^2\),

\[
\frac{KD}{K^2+D}>a.
\]

For \(K>a\), this forces

\[
\boxed{
D>\frac{aK^2}{K-a}.
}
\]

Thus large critical-norm growth cannot occur without a minimum amount of centered spectral defect.

## 7. Finite lifetime budget

Since \(EZ=K^2+D\),

\[
(E^2)'=2EE'=-4\nu EZ=-4\nu(K^2+D).
\]

Therefore, for every smooth interval \([0,T]\),

\[
\boxed{
\int_0^T (K^2+D)\,dt
\le \frac{E(0)^2}{4\nu}.
}
\]

Any blow-up scenario must therefore form increasingly intense, increasingly short bursts while respecting a finite global budget.

## 8. Evolution of the spectral defect

Differentiate \(D=EZ-K^2\). Define

\[
\Gamma:=\langle(\Lambda-m)^2u,F\rangle.
\]

Then

\[
D'
=2E\Gamma
-2\nu\left(EM_4+Z^2-2KM_3\right).
\]

The dissipative bracket has the exact decomposition

\[
EM_4+Z^2-2KM_3
=E\|\Lambda s\|_2^2+\frac ZE D.
\]

Hence

\[
\boxed{
D'
=2E\Gamma
-2\nu E\|\Lambda s\|_2^2
-2\nu\frac ZE D.
}
\]

## 9. Commutator collapse of the second-centered Euler term

Let \(Q=\Lambda-m\), so \(s=Qu\). Using \(F=-P(u\cdot\nabla u)\), self-adjointness, and incompressibility,

\[
\Gamma
=-\langle Q^2u,u\cdot\nabla u\rangle
=-\langle s,Q(u\cdot\nabla u)\rangle.
\]

Since

\[
Q(u\cdot\nabla u)
=u\cdot\nabla s+[\Lambda,u\cdot\nabla]u,
\]

and

\[
\langle s,u\cdot\nabla s\rangle=0,
\]

one gets the exact identity

\[
\boxed{
\Gamma=-\langle s,[\Lambda,u\cdot\nabla]u\rangle.
}
\]

Thus the next escape level does not introduce an arbitrary new nonlinear object: it is the first centered spectral defect paired with a genuine Navier–Stokes commutator.

The Fourier symbol is

\[
\widehat{[\Lambda,u\cdot\nabla]u}(k)
=i\int_{p+q=k} (|k|-|q|)(q\cdot\hat u(p))\hat u(q)\,dp.
\]

Therefore \(\Gamma\) carries two radial spectral differences: roughly

\[
(|k|-m)(|k|-|q|).
\]

## 10. Shell acceleration

At an exact spectral shell \(s=0\),

\[
D=0,
\qquad D'=0,
\qquad \kappa=0.
\]

However the Euler term may open spectral width at second order. At such an instant,

\[
\boxed{
D''=2E\|(\Lambda-m)F\|_2^2\ge0.
}
\]

Hence a proof cannot rely on the false principle that a narrow packet is automatically invariant or instantaneously self-narrowing. The relevant competition involves escape acceleration versus viscous dissipation.

## 11. Helical decomposition and the heterochiral obstruction

Let

\[
R=\Lambda^{-1}\operatorname{curl},
\qquad
u=u_++u_-,
\qquad
Ru_\pm=\pm u_\pm.
\]

Define \(s_\pm=(\Lambda-m)u_\pm\). Then the determinant coupling expands to

\[
\boxed{
\kappa
=2m\langle u_+,s\times u_-\rangle
+2\langle s_+,s_-\times u\rangle.
}
\]

Consequences:

- \(s=0\Rightarrow\kappa=0\);
- a pure-helicity state (one spin absent) has \(\kappa=0\) at that instant;
- genuine positive critical-norm production requires centered spectral defect **and** heterochiral interaction.

This isolates the dangerous class to coherent narrow-band heterochiral triads.

## 12. Current frontier

The proof is not closed. The remaining target is a quantitative **heterochiral cascade barrier** strong enough to exclude an infinite sequence of states satisfying simultaneously

\[
K\to\infty,
\qquad
D\gtrsim \frac{aK^2}{K-a},
\qquad
\kappa>\nu M_3,
\]

while respecting

\[
\int_0^T(K^2+D)\,dt<\infty.
\]

The key unresolved object is the true triadic/commutator geometry of

\[
\Gamma=-\langle s,[\Lambda,u\cdot\nabla]u\rangle
\]

restricted to coherent heterochiral interactions.
