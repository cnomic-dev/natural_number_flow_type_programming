# The Cosmological Constant in ln1 Notation

**Sorting 宇宙常數.txt — three exact identities, one structural location, one ill-posed number**

Cret, September 2026

---

## 0. What This Does

The Final Ledger placed "physical constants (`ħ`, `G`, `Λ`) expressed via `ln1`" in §3.4, **ill-posed**, on the grounds that dimensionful quantities have no unit-independent numerical value. That disposition stands. This document does three things it did not do:

1. sorts the source note `宇宙常數.txt` line by line, since it mixes objects of four different kinds under one heading;
2. gives the ill-posedness a quantitative form — the failure is not only dimensional, and the other two reasons hold independently of dimensions;
3. extracts the one line of the note that connects to an established result: `i^i` lands exactly on `τ = i` in the Tate-curve family.

Only (3) is new content. (1) is bookkeeping; (2) sharpens a verdict already reached.

---

## 1. Four Kinds of Object Under One Heading

The note contains:

```
自然常數 = e                                dimensionless, transcendental
({{e}({(∞!)^{n}}^{n})})^{n}                 not defined
f({x}) = f({ln x}/{x})                      under-specified; intent recoverable
e^{πi} + 1 = 0,   i^i = e^{−π/2}            exact identities
G_μν = 8πG T_μν + Λ g_μν                    field equation, sign convention off
```

`e` and `Λ` are not the same kind of constant, and the note's opening lines treat them as though a construction over the first could produce the second.

| | `e` | `Λ` |
|---|---|---|
| dimension | none | length⁻² |
| fixed by | definition | measurement |
| under unit change | invariant | changes |
| status | transcendental (Hermite, 1873) | ~1 significant figure known |

Everything in the note that `ln1` expresses exactly sits in the `e` column. `Λ` is the sole entry in the right column — and the only one the note actually set out to express.

---

## 2. The Two Lines That Are Not Claims

**`({{e}({(∞!)^{n}}^{n})})^{n}`.** `∞!` names no object. Factorial is defined on ℕ; the analytic extension `Γ(z+1)` diverges as `z → ∞`, so there is no limiting number to raise to a power. The regularised alternative, `∏_{n≥1} n "=" √(2π)` via `ζ′(0) = −½ ln 2π`, is a *choice of regulator*, not an evaluation — and `√(2π)` raised to `n^n` diverges anyway. Separately, `{e}` is a one-element set; `{e}^n` yields n-tuples, not a number. The expression has no value to compare with `Λ`, so this is not a false claim — it is **not yet a claim**, the same disposition as universal S1.

**`f({x}) = f({ln x}/{x})`.** As written this is a functional equation, not a definition: every constant function satisfies it, so it does not pick out `f`. The line immediately following recovers the intent — that derivation uses monotonicity — so the object meant is

```
g(x) = ln x / x
```

which is well-defined and does the work. Read that way, §3.3 below is correct as the note has it.

---

## 3. The Exact Part, in ln1 Form

Established (v0.9–v0.12): `ln1 = 2πiℤ`, the branch lattice.

### 3.1 Euler

```
ln(−1) = πi + ln1
ln(−1) / 2πi = 1/2 + ℤ
```

This is the first row of the note's `ζ` table, and it is right: `−1` is the primitive 2nd root of unity and its logarithm is a half-period of the lattice; likewise `ζ_n ↦ 1/n + ℤ`. The table's closing line — `1+2+3+⋯ = −1/12` "corresponding to `p = 13`" — is the claim already refuted in Ledger §3.1. The table itself is the disproof: `1/11` and `1/13` sit there on exactly the same footing as `1/12`.

### 3.2 `i^i` — the one line that connects

```
ln i = πi/2 + ln1
i^i = exp(i · ln i) = e^{−π/2} · exp(i · ln1)
```

and `i · ln1 = i · 2πiℤ = −2πℤ`, so

```
i^i ∈ e^{−π/2} · q^ℤ ,        q = e^{−2π}
```

Multiplying by `i` converts the branch lattice from a rotation group into a **scaling** group. And `q = e^{−2π} = e^{2πiτ}` at `τ = i` is exactly the nome of the Tate curve `ℂ*/q^ℤ`. Hence:

> `i^i` is infinitely many values in `ℂ*`, and **exactly one point** on the Tate curve at `τ = i`. The multivaluedness is quotiented away.

Cross-checks against results already established:

- height in the fundamental domain `= ln(p)/2π`; setting height `= 1` gives `p = e^{2π}`, the reciprocal nome here.
- `e^{2π}` is transcendental — Gelfond–Schneider via `(−1)^{−i} = e^{π}` — so this base is **not a prime**. That is the other face of the Ledger's obstructed entry "no CM for any prime curve `τ_p`, by Baker": the CM point is reachable only by leaving the prime family.
- `τ = i` has lattice `ℤ[i]`, `j = 1728`, extra automorphisms `μ₄`.
- The note's two remaining lines are the same number: `e^{π} = (i^i)^{−2}` on the principal branch.

What this does **not** do: it says nothing whatever about `Λ`. It is a worked instance belonging to *From ln1 to the Tate Curve*, and it turned up in this note only because `i^i` happened to be written next to a cosmology line.

### 3.3 `e^π > π^e`

```
g(x) = ln x / x ,        g′(x) = (1 − ln x)/x²
g(1) = ln1 ,   g(e) = 1/e  (unique maximum) ,   g(x) → ln1  as x → ∞
π > e  ⇒  g(π) < g(e)  ⇒  π ln e > e ln π  ⇒  e^π > π^e        (23.14 > 22.46)
```

This is the defensible version of "bridging 0 and ∞": `g` sends both `1` and `∞` to `ln1`, with a single maximum at `e` between them. On `x > 1` every value in `(0, 1/e)` is attained exactly twice, and each such pair `(x, y)` satisfies `x^y = y^x`; the only integer pair is `(2, 4)`. That two-to-one structure is real, and it is the entirety of what is there — no lattice, no group action, nothing that transfers.

---

## 4. What ln1 Can Say About Λ: Its Position

The note's field equation needs one correction. In the `(−+++)` convention:

```
G_μν + Λ g_μν = (8πG/c⁴) T_μν
```

The note moved `Λ g_μν` across the equality without changing sign, which flips the sign of `Λ`.

Now the part that holds. **Lovelock's theorem (1971):** in four dimensions the only symmetric, divergence-free rank-2 tensor built from the metric and its derivatives to second order, with those second derivatives entering linearly, is

```
a · G_μν + b · g_μν
```

Mapped onto the note's own order ladder:

| order | note's name | tensor | status |
|---|---|---|---|
| 0 | `ln1` | `g_μν` | the `Λ` term — no derivatives |
| 1 | slope | — | **provably empty** |
| 2 | curvature | `G_μν` | Einstein tensor |
| 3 | spin / torsion | `0` in GR | nonzero only in Einstein–Cartan |

Order 1 is empty for a reason, not by omission: normal coordinates set `∂g = 0` at any chosen point, so no tensor can be built from `g` and its first derivatives alone. This is why gravity's field equation starts at second order. Order 3 is a name-level correspondence only; nothing here derives it.

So the structural reading yields this much, and no more:

> The geometry **forces the order-0 slot to exist**. `Λ` is precisely the free coefficient `b` that Lovelock leaves undetermined. The position is derived; the number is not.

That is a genuine result about where `Λ` sits — and it is Lovelock's. The ladder re-labels it.

---

## 5. Why the Number Stays Ill-Posed — Three Independent Reasons

Measured: `Λ ≈ 1.1 × 10⁻⁵² m⁻²` (Planck 2018: `H₀ = 67.4 km/s/Mpc`, `Ω_Λ = 0.685`, `Λ = 3H₀²Ω_Λ/c²`). The only unit-free form is

```
Λ · ℓ_P² ≈ 2.8 × 10⁻¹²²
```

**(i) Dimensional.** Ledger §3.4. `Λ` in m⁻² and `Λ` in Planck units differ by ~70 orders of magnitude, and neither is "the" value. Any `ln1` expression for it would be expressing a choice of metre.

**(ii) Convention survives dimensionlessness.** Removing the dimensions does not fix the number. Using the *reduced* Planck length (defined with `8πG`), the same physical `Λ` gives `≈ 7 × 10⁻¹²¹` — a factor of `8π` away, with no principled ground for preferring either.

**(iii) Density defeats fitting — fatal on its own.** The notation generates all of `ℚ⁺` from `(ln1)^(ln1) = 1` by the note's own sum-and-ratio rules, and `ℚ` is dense in `ℝ`. The target has roughly one reliable significant figure: `H₀` is disputed between ≈67 and ≈73, and since `Λ ∝ H₀²` that alone is a ~17% spread. The interval to be hit is therefore wide and contains infinitely many `ln1` expressions. A fit is **guaranteed to exist**, so producing one carries zero information.

Reason (iii) is the one to keep. It never mentions dimensions, so it applies unchanged to dimensionless constants — `α⁻¹ ≈ 137.036` included. The "分子分母完美表達" programme presupposes that an exact value exists and only its notation is missing. For a measured quantity that presupposition fails: **there is no exact value to write down.**

**And the open question is magnitude, not notation.** The problem is why the value is `10⁻¹²²` rather than `O(1)`, which is what a naive Planck-cutoff vacuum-energy estimate gives. A framework earns standing here by *deriving* that exponent. Transcribing it into new symbols does not touch it.

**`Λ` may not be constant.** DESI DR2 (2025) combined with CMB reports a `3.1σ` preference for evolving dark energy (`w₀ = −0.42 ± 0.21`, `w_a = −1.75 ± 0.58`), rising toward `4σ` with some supernova compilations. The significance is contested: critical analyses note that DR1 full-shape results are consistent with ΛCDM, and that BAO+CMB under relaxed priors does not by itself confirm late-time acceleration. If `w` evolves, "the cosmological constant" is not a constant, and there is no such quantity of this kind to express. Status as of writing; recheck before relying on it.

---

## 6. Disposition

Following the Final Ledger's categories.

### Established
- `ln(−1) = πi + ln1`, and the `ζ`-table reading `ln ζ_n / 2πi = 1/n + ℤ` — known
- `i^i ∈ e^{−π/2} · q^ℤ` with `q = e^{−2π}`, single-valued on `ℂ*/q^ℤ` at `τ = i` — known in itself, but **new here**: it is the v0.12 Tate family evaluated at a CM point, with the transcendence of `e^{2π}` explaining why no prime base reaches it
- `g(x) = ln x/x` monotone structure ⇒ `e^π > π^e`, two-to-one on `(0, 1/e)`, sole integer pair `(2,4)` — known
- `Λ` occupies the order-0 slot of a ladder whose order-1 rung is provably empty — Lovelock's result, re-labelled

### Refuted
- `1+2+3+⋯ = −1/12` as singling out `p = 13` — already closed; the note's own table gives `1/11` and `1/13` equal standing

### Ill-posed
- `Λ` via `ln1`: three independent reasons, (iii) sufficient alone
- `({{e}({(∞!)^{n}}^{n})})^{n}` — `∞!` names no object

### Underdetermined
- `f({x}) = f({ln x}/{x})` as written; determinate under the intended reading `g(x) = ln x/x`

---

## 7. On the Figure

The accompanying construction labels four axes `(ln1)(±1)`, `(ln1)(±i)` with bidirectional rotation, and nests circles in what reads as 4-fold and 6-fold arrangements. Those symmetries are `μ₄` and `μ₆` — the automorphism groups of the two CM points `τ = i` (`j = 1728`) and `τ = ρ = e^{2πi/3}` (`j = 0`), the same two points §3.2 reaches analytically.

That is a correspondence of **names**, and the project's own standing lesson applies: a shared symmetry label does not carry theorems with it into a new domain. The figure illustrates; it does not evidence. It would become evidence only if the nesting ratios were computed and matched a predicted quantity — and the obvious candidate, `e^{−2π} ≈ 0.00187`, is not a ratio the drawing visibly realises.

---

## 8. Where This Leaves the Note

**Keep:** §3.2. `i^i` at `τ = i` is a clean worked instance of the one result this project genuinely owns. It belongs in *From ln1 to the Tate Curve* as an **example**, not as an application.

**Keep as bookkeeping:** §4. The order ladder is a readable index into Lovelock, useful for stating where `Λ` sits — provided it is never presented as deriving anything.

**Retire:** the cosmological-constant expression itself, in every form — dimensionful, dimensionless, and factorial-over-`e`. It joins the `ħ`/`G`/`Λ` entry already in §3.4, now with the fitting-density argument attached, which is the version that generalises to dimensionless constants as well.

---

*The Cosmological Constant in ln1 Notation — Cret, September 2026*

*The geometry fixes where the constant goes. It does not fix what it is — and a notation that can express every rational number cannot be the thing that finds out.*
