# Helical triad factorization and within-spin spectral defect

Research note — current proof state. This note records identities/reductions obtained after the initial snapshot. It is **not** a claim of a completed Navier–Stokes regularity proof.

## 1. Exact triad constraints

For one helical triad with radii `k,p,q`, helicity signs `sigma_k,sigma_p,sigma_q in {+1,-1}`, and nonlinear energy-transfer rates `T_k,T_p,T_q`, Euler conservation gives

```text
T_k + T_p + T_q = 0,
sigma_k k T_k + sigma_p p T_p + sigma_q q T_q = 0.
```

Hence the transfer vector is one-dimensional and can be parameterized as

```text
T_k = J (sigma_p p - sigma_q q),
T_p = J (sigma_q q - sigma_k k),
T_q = J (sigma_k k - sigma_p p),
```

where `J` contains the phase/geometric triad amplitude.

For the critical quantity `K = sum |k| |u_k|^2`, the triad production is

```text
dot K_triangle = k T_k + p T_p + q T_q.
```

### Homochiral cancellation

If all three helicity signs agree, then

```text
dot K_triangle = 0
```

exactly.

### Heterochiral factorization

If `k,p` have the same helicity sign and `q` the opposite sign, then

```text
dot K_triangle = 2 sigma_k q (k-p) J.
```

Thus a heterochiral interaction can produce `K` only if the two same-helicity modes have different radii. Opposite helicity alone is insufficient.

## 2. Within-spin centered variables

Decompose

```text
u = u_+ + u_-,
curl u_± = ± Lambda u_±.
```

For each sign define

```text
E_± = ||u_±||_2^2,
K_± = <u_±, Lambda u_±>,
m_± = K_± / E_±,
s_± = (Lambda - m_±) u_±,
W_± = ||s_±||_2^2.
```

Then

```text
<u_±, s_±> = 0,
W_± = Z_± - K_±^2 / E_±.
```

`W_±` is the spectral variance inside each helicity sector. The triad factorization above suggests that these are the natural defects controlling production of the critical norm.

## 3. Global collapse of kappa

Let

```text
F = P(u x omega),
F_± = P_± F,
A_± = <Lambda u_±, F_±>,
B_± = <u_±, F_±>.
```

Euler energy and helicity conservation imply

```text
B_+ + B_- = 0,
A_+ - A_- = 0.
```

Since

```text
kappa = <Lambda u,F> = A_+ + A_-,
```

we have `A_+ = A_- = kappa/2`.

Define

```text
c_± = <s_±,F_±>.
```

Using `c_± = A_± - m_± B_±` and the two conservation relations gives

```text
kappa = 2 (m_- c_+ + m_+ c_-) / (m_+ + m_-).
```

This is the global counterpart of the heterochiral triad factorization: the monochromatic core of each helicity sector does not contribute to `K` production; only the within-spin centered defects do.

## 4. Refined nonlinear bound

Let

```text
S = (m_- ||s_+||_2 + m_+ ||s_-||_2) / (m_+ + m_-).
```

Using

```text
|c_±| <= C ||s_±||_2 ||u||_6 ||omega||_3,
||u||_6 <= C Z^(1/2),
||omega||_3 <= C M_3^(1/2),
```

one obtains

```text
|kappa| <= 2 C S Z^(1/2) M_3^(1/2).
```

Together with

```text
K' = 2 kappa - 2 nu M_3,
Z^2 <= K M_3,
```

and Young's inequality, this yields a conditional differential estimate of the form

```text
K' <= C0 nu^(-3) S^4 K.
```

Therefore

```text
integral_0^T S(t)^4 dt < infinity
```

is sufficient to keep `K` bounded up to `T`.

## 5. Viscous Riccati damping of within-spin width

Let

```text
Q_± = Lambda - m_±,
Gamma_± = <Q_±^2 u_±, F_±>,
H_± = ||Lambda s_±||_2^2.
```

Differentiating `W_± = ||s_±||_2^2` gives the exact balance

```text
W_±' = 2 Gamma_± - 2 nu H_±.
```

Because

```text
W_± = <u_±, Lambda s_±>,
```

Cauchy-Schwarz yields

```text
W_±^2 <= E_± H_±,
```

hence

```text
W_±' <= 2 Gamma_± - 2 nu W_±^2 / E_±.
```

With

```text
W = W_+ + W_-,
Gamma_sp = Gamma_+ + Gamma_-,
```

one obtains

```text
W' <= 2 Gamma_sp - 2 nu W^2/E,
```

and `S^2 <= W`. Thus a sufficient remaining target is

```text
(Gamma_sp)_+ in L^1_t,
```

because then `W in L^2_t`, hence `S in L^4_t`, and the preceding Gronwall estimate controls `K`.

## 6. Further triad-level cancellation

For a homochiral triad, the production of a quadratic radial variance contains the Vandermonde factor

```text
k^2 T_k + p^2 T_p + q^2 T_q
  = (p-k)(q-k)(p-q) J.
```

Thus homochiral recharge of within-spin spectral width carries three radial differences and is strongly depleted for a narrow packet.

## 7. Current proof target

The present reduction is:

```text
finite-time singular escape
=> unbounded critical K
=> failure of S in L^4_t
=> failure of W in L^2_t
=> infinite positive action of Gamma_sp.
```

The next task is therefore to exploit the **exact Navier–Stokes helical triad coefficients** to control

```text
Gamma_sp = sum_{sigma=±} <(Lambda-m_sigma)^2 u_sigma,
                         P_sigma(u x omega)>.
```

The key advantage to preserve is that `Gamma_sp` is not treated as a generic bilinear term: it retains energy/helicity conservation, helicity signs, radial differences, phase geometry, and the exact Lamb-vector structure.

## 8. Exact spin-mixing remainder in the total defect

The within-spin action is not identical to the total centered-defect action. This difference has an exact and useful form. Set

```text
m = (K_+ + K_-) / (E_+ + E_-),
Delta_m = m_+ - m_-,
B = <u_+,F_+> = -<u_-,F_->,
Gamma_tot = sum_sigma <(Lambda-m)^2 u_sigma,F_sigma>.
```

The energy and helicity identities give

```text
<Lambda u_+,F_+> = <Lambda u_-,F_-> = kappa/2.
```

Since

```text
m_+ - m = (E_-/E) Delta_m,
m_- - m = -(E_+/E) Delta_m,
```

and `<(Lambda-m_+)u_+,F_+> = kappa/2-m_+B`,
`<(Lambda-m_-)u_-,F_-> = kappa/2+m_-B`, expanding
`Lambda-m = (Lambda-m_sigma)+(m_sigma-m)` in `Gamma_tot` yields the exact decomposition

```text
Gamma_tot
= Gamma_sp
  + ((E_- - E_+) / E) Delta_m kappa
  - (m_+^2 - m_-^2) B.
```

The remainder is the Euler production of the variance between the two helicity means. Indeed, define

```text
V = E_+ E_- (m_+ - m_-)^2.
```

Then the total defect splits as

```text
D = E (W_+ + W_-) + V,
```

For the Euler part alone,

```text
(d/dt) E_+ =  2B,     (d/dt) E_- = -2B,
(d/dt) K_+ = (d/dt) K_- = kappa.
```

Substitution into `V` gives

```text
(d/dt)_Euler V = 2 E (Gamma_tot - Gamma_sp).
```

Thus define the two nonnegative scale-invariant actions

```text
A_sp(I)  = integral_I E (Gamma_sp)_+ dt,
A_mix(I) = integral_I E (Gamma_tot-Gamma_sp)_+ dt.
```

Pointwise positivity gives `A_D(I) <= A_sp(I)+A_mix(I)`. The first is implied by the originally desired raw `(Gamma_sp)_+ in L^1_t`, because energy is bounded. The second is a genuine **spin-mixing action**, not a harmless error term. In particular, a network argument that only charges within-spin variance recharge cannot yet control the direct total-defect route; it must also charge Euler growth of `V`.
