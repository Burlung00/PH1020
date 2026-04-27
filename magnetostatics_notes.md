# MAGNETOSTATICS - Comprehensive Notes for Exam Preparation
## Based on IIT Madras PH1020 Problem Set 6

---

## TABLE OF CONTENTS
1. Vector Potential
2. Magnetic Dipole Moment
3. Magnetization in Matter
4. Bound Currents
5. H Field and Constitutive Relations
6. Boundary Conditions
7. Magnetic Materials (LIH)
8. Standard Problems & Formulas

---

## 1. VECTOR POTENTIAL (A)

### Definition and Fundamental Relations

**Key Concept**: The vector potential **A** is defined such that:

```
∇ × A = B  (Magnetic field from vector potential)
```

**Why A exists**: Since ∇·B = 0 always (no magnetic monopoles), we can write B as the curl of some vector field A.

### Standard Formula: Current from Vector Potential

**Ampere's Law in free space**:
```
∇ × B = μ₀J
```

Substituting B = ∇ × A:
```
∇ × (∇ × A) = μ₀J
```

Using vector identity: ∇ × (∇ × A) = ∇(∇·A) - ∇²A

**In Coulomb Gauge** (∇·A = 0):
```
∇²A = -μ₀J
```

**To find J from A**:
```
J = (1/μ₀) ∇ × B = (1/μ₀) ∇ × (∇ × A)
```

### Cylindrical Coordinates

In cylindrical coordinates (ρ, φ, z):

**Curl in cylindrical coordinates**:
```
∇ × A = [(1/ρ)(∂A_z/∂φ) - ∂A_φ/∂z] ê_ρ 
       + [∂A_ρ/∂z - ∂A_z/∂ρ] ê_φ 
       + [(1/ρ)(∂(ρA_φ)/∂ρ) - (1/ρ)(∂A_ρ/∂φ)] ê_z
```

**For A = k ê_φ** (Problem 1):
- A_ρ = 0, A_φ = k, A_z = 0
- B_z = (1/ρ) d(ρk)/dρ = k/ρ + k = 2k/ρ... (needs careful calculation)

---

## 2. MAGNETIC DIPOLE MOMENT

### For a Current Loop

**Magnetic dipole moment**:
```
m = I A n̂
```
where:
- I = current
- A = area enclosed by loop
- n̂ = normal to the loop (right-hand rule)

### For a Moving Point Charge (Problem 2)

**Orbital magnetic moment**:
```
m = (q/2m) L
```
where:
- q = charge
- m = mass
- L = orbital angular momentum = r × p

**Derivation**:
For a charge q moving in a circle of radius r with velocity v:
- Current: I = q/(period) = qv/(2πr)
- Area: A = πr²
- m = IA = (qv/2πr)(πr²) = qvr/2
- But L = mvr (angular momentum)
- Therefore: m = (q/2m)L

**Gyromagnetic ratio**: γ = q/(2m)

### For Extended Charge Distributions (Problem 3)

**For a spinning charged sphere**:
- Consider shell at radius r, thickness dr
- Charge in shell: dq = ρ dV = ρ (4πr² dr)
- For uniform density: ρ = 3Q/(4πR³)
- Each shell rotates with ω, acts like current loop
- dm = (dq/2m_particle) L_shell

**Total moment** (to be calculated):
Integrate over all shells from 0 to R.

---

## 3. MAGNETIZATION (M)

### Definition

**Magnetization M**: Magnetic dipole moment per unit volume
```
M = dm/dV
```

For N dipoles per unit volume, each with moment m:
```
M = N m
```

**Units**: A/m (Amperes per meter)

### Physical Interpretation

- M represents the density of magnetic dipoles in matter
- Points in the direction of alignment of magnetic dipoles
- Zero in unmagnetized materials

---

## 4. BOUND CURRENTS

### Volume Bound Current (J_b)

**Fundamental Formula**:
```
J_b = ∇ × M
```

**Derivation**: The bound current arises from the circulation of magnetization.

**In cylindrical coordinates**:
```
∇ × M = [(1/ρ)(∂M_z/∂φ) - ∂M_φ/∂z] ê_ρ 
       + [∂M_ρ/∂z - ∂M_z/∂ρ] ê_φ 
       + [(1/ρ)(∂(ρM_φ)/∂ρ) - (1/ρ)(∂M_ρ/∂φ)] ê_z
```

### Surface Bound Current (K_b)

**Fundamental Formula**:
```
K_b = M × n̂
```
where n̂ is the outward normal to the surface.

**Units**: A/m (surface current density)

**Physical Meaning**: At the boundary of a magnetized material, the magnetization creates a surface current.

### Problem 4 Application

Given: M = M₀(ρ/a)² ê_φ in cylindrical coordinates

**Find J_b**:
```
J_b = ∇ × M
```

Since M only has φ-component and depends only on ρ:
```
J_b,z = (1/ρ) d(ρM_φ)/dρ
     = (1/ρ) d(ρ · M₀(ρ/a)² )/dρ
     = (M₀/a²) · (1/ρ) d(ρ³)/dρ
     = (M₀/a²) · 3ρ
```

**Find K_b**: At ρ = a (outer surface):
```
K_b = M × n̂ = M₀ ê_φ × ê_ρ = M₀ ê_z
```

---

## 5. H FIELD AND CONSTITUTIVE RELATIONS

### Definition of H

**Fundamental relation**:
```
H = (1/μ₀) B - M
```

Or equivalently:
```
B = μ₀(H + M)
```

**Why H is useful**: 
- ∇ × H = J_f (free currents only)
- Ampere's law becomes simpler in matter

### Ampere's Law for H

```
∇ × H = J_f
```

**Integral form**:
```
∮ H · dl = I_f,enc
```
where I_f,enc is the free current enclosed.

### Linear Magnetic Materials (LIH)

**Linear Isotropic Homogeneous (LIH) materials**:

**Constitutive relation**:
```
M = χ_m H
```
where χ_m is the magnetic susceptibility.

**Therefore**:
```
B = μ₀(H + M) = μ₀(H + χ_m H) = μ₀(1 + χ_m)H
```

**Define permeability**:
```
μ = μ₀(1 + χ_m) = μ₀ μ_r
```
where μ_r = 1 + χ_m is the relative permeability.

**Final relation**:
```
B = μH = μ₀μ_r H
```

### Classification of Materials

1. **Diamagnetic**: χ_m < 0 (slightly negative), μ_r < 1
   - Examples: Copper, gold, water
   
2. **Paramagnetic**: χ_m > 0 (small positive), μ_r > 1
   - Examples: Aluminum, platinum
   
3. **Ferromagnetic**: χ_m >> 1, μ_r >> 1
   - Examples: Iron, nickel, cobalt
   - Non-linear behavior (not strictly LIH)

---

## 6. BOUNDARY CONDITIONS

### Boundary Conditions for B

**Normal component**:
```
B₁ₙ = B₂ₙ
```
or
```
(B₁ - B₂) · n̂ = 0
```

**Tangential component** (no surface free current):
```
B₁ₜ/μ₁ = B₂ₜ/μ₂
```

### Boundary Conditions for H

**Normal component**:
```
μ₁H₁ₙ = μ₂H₂ₙ
```
or
```
(H₁ - H₂) · n̂ = (M₁ - M₂) · n̂
```

**Tangential component**:
```
H₁ₜ - H₂ₜ = K_f × n̂
```
where K_f is the free surface current density.

**If no free surface current** (K_f = 0):
```
H₁ₜ = H₂ₜ
```

### Boundary Conditions for M

**At the surface**:
```
K_b = M × n̂
```

This is the bound surface current density.

---

## 7. MAGNETIC CIRCUITS (Problem 5)

### Toroid with Gap

**Standard toroid** (no gap):
- ∮ H · dl = NI (N turns, current I)
- For uniform H: H(2πr) = NI
- H = NI/(2πr)

**Toroid with gap** (angle ψ):
- Path through material: length = 2πr - rψ
- Path through gap: length = rψ
- In material: H_mat
- In gap: H_gap = B_gap/μ₀

**Apply ∮ H · dl = NI**:
```
H_mat(2πr - rψ) + H_gap(rψ) = NI
```

**Continuity of B_normal**:
```
B_mat = B_gap = B
```

For LIH material:
```
B = μH_mat = μ₀(1 + χ_m)H_mat
```

In gap:
```
B = μ₀H_gap
```

Therefore:
```
H_gap = (1 + χ_m)H_mat
```

Substitute back:
```
H_mat(2πr - rψ) + (1 + χ_m)H_mat(rψ) = NI
H_mat[2πr - rψ + (1 + χ_m)rψ] = NI
H_mat[2πr + χ_m rψ] = NI
```

**Solution**:
```
H_mat = NI / [2πr + χ_m rψ]
     = NI / [r(2π + χ_m ψ)]
```

---

## 8. NON-UNIFORM PERMEABILITY (Problem 6)

### Key Concept

When permeability varies with position: μ = μ(r)

**Relation**:
```
B = μ(r)H
```

**No free currents**:
```
∇ × H = 0  ⟹  H is conservative (can be derived from potential)
```

**Divergence**:
```
∇ · B = ∇ · (μH) = 0
```

This gives:
```
∇ · (μH) = μ(∇ · H) + H · ∇μ = 0
```

### Magnetization Current

From B = μ₀(H + M):
```
M = B/μ₀ - H = (μ/μ₀ - 1)H = (μ_r - 1)H
```

**Volume magnetization current**:
```
J_b = ∇ × M
```

**Surface magnetization current** (at interface):
```
K_b = M × n̂
```

### Problem 6 Specifics

Given: μ(z) = μ₀[1 + (z/d)]², B = B₀ ê_y everywhere

**Since ∇ × H = 0 and B is uniform**:
```
H = B/μ(z) = B₀/μ₀[1 + (z/d)]² ê_y
```

**Magnetization**:
```
M = B/μ₀ - H = B₀/μ₀ ê_y - B₀/μ₀[1 + (z/d)]² ê_y
  = (B₀/μ₀)[1 - 1/[1 + (z/d)]²] ê_y
```

**Volume current**:
```
J_b = ∇ × M
```

**Surface currents**: Calculate M × n̂ at z = 0 and z = d

---

## STANDARD FORMULAS - QUICK REFERENCE

### Fundamental Relations
```
∇ × A = B                          (Vector potential)
∇ × B = μ₀J + μ₀ε₀(∂E/∂t)        (Ampere-Maxwell law)
∇ × B = μ₀J                        (Magnetostatics)
∇ · B = 0                          (No magnetic monopoles)
```

### Fields in Matter
```
B = μ₀(H + M)                      (Fundamental relation)
H = B/μ₀ - M                       (Alternative form)
∇ × H = J_f                        (Ampere's law for H)
J_b = ∇ × M                        (Bound volume current)
K_b = M × n̂                        (Bound surface current)
```

### Linear Materials
```
M = χ_m H                          (Susceptibility)
B = μH                             (Permeability)
μ = μ₀μ_r = μ₀(1 + χ_m)           (Permeability relation)
```

### Boundary Conditions
```
B₁ₙ = B₂ₙ                         (Normal B continuous)
H₁ₜ - H₂ₜ = K_f × n̂               (Tangential H)
(B₁ - B₂) · n̂ = 0                 (Alternative form)
```

### Magnetic Dipole
```
m = IA n̂                          (Current loop)
m = (q/2m)L                        (Moving charge)
M = dm/dV                          (Magnetization)
```

### Integral Forms
```
∮ B · dl = μ₀I_enc                (Ampere's law)
∮ H · dl = I_f,enc                (Ampere's law for H)
∫ B · dA = 0                      (Gauss's law for B)
```

### Cylindrical Coordinates
```
∇ × A|_z = (1/ρ)[∂(ρA_φ)/∂ρ - ∂A_ρ/∂φ]
∇ × A|_φ = ∂A_ρ/∂z - ∂A_z/∂ρ
∇ × A|_ρ = (1/ρ)[∂A_z/∂φ - ∂(ρA_φ)/∂z]
```

---

## PROBLEM-SOLVING STRATEGIES

### Problem Type 1: Finding Current from Vector Potential
1. Calculate B = ∇ × A
2. Calculate ∇ × B
3. Use J = (∇ × B)/μ₀

### Problem Type 2: Magnetic Dipole Moment
1. For current loops: m = IA
2. For moving charges: m = (q/2m)L
3. For extended distributions: integrate dm

### Problem Type 3: Magnetization Problems
1. Calculate bound currents: J_b = ∇ × M, K_b = M × n̂
2. Find H using ∇ × H = J_f
3. Find B = μ₀(H + M)

### Problem Type 4: Magnetic Circuits
1. Identify path for ∮ H · dl
2. Apply boundary conditions at interfaces
3. Use B_normal continuous
4. Solve for H in each region

### Problem Type 5: Boundary Value Problems
1. Apply boundary conditions for B and H
2. Use symmetry to simplify
3. Match normal and tangential components

---

## COMMON MISTAKES TO AVOID

1. **Confusing B and H**: Remember B = μ₀(H + M) in matter
2. **Forgetting bound currents**: Always calculate J_b and K_b
3. **Wrong curl in cylindrical coordinates**: Use correct formula
4. **Boundary conditions**: Normal B continuous, tangential H continuous (no free current)
5. **Units**: M and H have same units (A/m), B has different units (T)

---

## EXAM-WORTHY DERIVATIONS

1. **Derive m = (q/2m)L for a charged particle**
2. **Derive J_b = ∇ × M from first principles**
3. **Derive boundary conditions for B and H**
4. **Derive H field in toroid with and without gap**
5. **Show ∇ · B = 0 implies B = ∇ × A**

---

## KEY CONCEPTS TO REMEMBER

1. **Vector potential** A is not unique (gauge freedom)
2. **H field** eliminates bound currents from Ampere's law
3. **Magnetization** M is dipole moment per unit volume
4. **Bound currents** arise from ∇ × M and M × n̂
5. **LIH materials**: M = χ_m H, B = μH
6. **Boundary conditions** follow from ∇ · B = 0 and ∇ × H = J_f

---

## END OF NOTES
