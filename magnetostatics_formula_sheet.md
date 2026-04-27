# MAGNETOSTATICS - FORMULA SHEET (Quick Reference)

## FUNDAMENTAL EQUATIONS

### Maxwell's Equations (Magnetostatics)
| Equation | Differential Form | Integral Form |
|----------|-------------------|---------------|
| **Ampere's Law** | ∇ × B = μ₀J | ∮ B · dl = μ₀I_enc |
| **No Monopoles** | ∇ · B = 0 | ∫ B · dA = 0 |
| **Ampere for H** | ∇ × H = J_f | ∮ H · dl = I_f,enc |

### Vector Potential
```
B = ∇ × A
∇²A = -μ₀J     (Coulomb gauge: ∇·A = 0)
```

---

## FIELDS IN MAGNETIC MATERIALS

### Core Relations
```
B = μ₀(H + M)           H = B/μ₀ - M
M = χ_m H               (Linear materials)
B = μH = μ₀μ_r H        μ = μ₀(1 + χ_m)
```

### Bound Currents
```
J_b = ∇ × M             (Volume bound current)
K_b = M × n̂             (Surface bound current)
```

---

## MAGNETIC DIPOLE MOMENTS

```
m = IA n̂                      (Current loop: I = current, A = area)
m = (q/2m)L                   (Moving charge: L = r × p)
M = dm/dV = Nm                (Magnetization: N dipoles/volume)
```

---

## BOUNDARY CONDITIONS

### At Interface Between Media 1 and 2

**Normal components:**
```
B₁ₙ = B₂ₙ                     (B_⊥ continuous)
μ₁H₁ₙ = μ₂H₂ₙ
```

**Tangential components:**
```
H₁ₜ - H₂ₜ = K_f × n̂          (K_f = free surface current)
B₁ₜ/μ₁ = B₂ₜ/μ₂              (no free surface current)
```

**If K_f = 0:**
```
H₁ₜ = H₂ₜ                     (H_∥ continuous)
```

---

## CURL IN CYLINDRICAL COORDINATES (ρ, φ, z)

### For A = A_ρ ê_ρ + A_φ ê_φ + A_z ê_z

```
(∇ × A)_ρ = (1/ρ)(∂A_z/∂φ) - ∂A_φ/∂z

(∇ × A)_φ = ∂A_ρ/∂z - ∂A_z/∂ρ

(∇ × A)_z = (1/ρ)[∂(ρA_φ)/∂ρ - ∂A_ρ/∂φ]
```

### Special Case: A = A_φ(ρ) ê_φ only
```
(∇ × A)_z = (1/ρ) d(ρA_φ)/dρ
```

---

## MATERIAL PROPERTIES

| Type | χ_m | μ_r | Example |
|------|-----|-----|---------|
| **Diamagnetic** | < 0 (small) | < 1 | Cu, Au, H₂O |
| **Paramagnetic** | > 0 (small) | > 1 | Al, Pt |
| **Ferromagnetic** | >> 1 | >> 1 | Fe, Ni, Co |

---

## STANDARD CONFIGURATIONS

### 1. Infinite Straight Wire
```
B = (μ₀I)/(2πr) ê_φ          (r = distance from wire)
```

### 2. Solenoid (infinite, n turns/length)
```
B = μ₀nI ê_z                 (inside)
B = 0                        (outside)
```

### 3. Toroid (N total turns, radius r)
```
H = NI/(2πr) ê_φ             (inside)
H = 0                        (outside)
```

### 4. Toroid with Gap (gap angle ψ, susceptibility χ_m)
```
H_material = NI/[r(2π + χ_m ψ)]
H_gap = (1 + χ_m)H_material
```

---

## PROBLEM-SPECIFIC FORMULAS

### Spinning Charged Sphere (radius R, charge Q, angular velocity ω)
Setup for calculation:
- Volume charge density: ρ = 3Q/(4πR³)
- Shell at radius r: dq = ρ(4πr²)dr
- Surface velocity: v = ωr
- Current element: dI = (dq)ω/(2π)
- Need to integrate: m = ∫ dm

### Magnetized Cylinder (M = M₀(ρ/a)² ê_φ)
```
J_b,z = (1/ρ) d(ρM_φ)/dρ     (Volume current)
K_b = M(a) × ê_ρ              (Surface current at ρ = a)
```

### Non-uniform Permeability
If μ = μ(r) and B is known:
```
H = B/μ(r)
M = (μ/μ₀ - 1)H = (μ_r - 1)H
J_b = ∇ × M
K_b = (M_inside - M_outside) × n̂
```

---

## VECTOR IDENTITIES (Useful)

```
∇ × (∇ × A) = ∇(∇·A) - ∇²A
∇ · (∇ × A) = 0
∇ × (∇φ) = 0
∇ · (φA) = φ(∇·A) + A·∇φ
∇ × (φA) = φ(∇×A) + (∇φ)×A
```

---

## UNITS (SI)

| Quantity | Symbol | Unit | Alternative |
|----------|--------|------|-------------|
| **Magnetic field** | B | Tesla (T) | Wb/m² = kg/(A·s²) |
| **Auxiliary field** | H | A/m | - |
| **Magnetization** | M | A/m | - |
| **Vector potential** | A | T·m | Wb/m |
| **Magnetic flux** | Φ | Weber (Wb) | T·m² |
| **Permeability** | μ | H/m | T·m/A |
| **Susceptibility** | χ_m | - | dimensionless |
| **Current density** | J | A/m² | - |
| **Surface current** | K | A/m | - |

**Constants:**
```
μ₀ = 4π × 10⁻⁷ H/m ≈ 1.257 × 10⁻⁶ H/m
```

---

## QUICK PROBLEM-SOLVING CHECKLIST

### For "Find J from A" problems:
- [ ] Calculate B = ∇ × A (use correct coordinates)
- [ ] Calculate ∇ × B
- [ ] Use J = (∇ × B)/μ₀

### For "Find bound currents" problems:
- [ ] Calculate J_b = ∇ × M (volume current)
- [ ] Calculate K_b = M × n̂ at each boundary (surface current)
- [ ] Check direction using right-hand rule

### For "Find B and H" problems:
- [ ] Identify free currents J_f
- [ ] Apply ∇ × H = J_f or ∮ H · dl = I_f,enc
- [ ] Use constitutive relation: B = μH (in LIH materials)
- [ ] Apply boundary conditions at interfaces

### For magnetic circuit problems:
- [ ] Draw equivalent circuit if helpful
- [ ] Apply ∮ H · dl = NI around closed path
- [ ] Use B_normal continuous at boundaries
- [ ] Express H in terms of B using H = B/μ
- [ ] Solve for unknowns

---

## COMMON EXAM QUESTIONS

1. **Derive the relation m = (q/2m)L**
2. **Show that J_b = ∇ × M**
3. **Prove boundary conditions for B and H**
4. **Calculate magnetic moment of spinning sphere**
5. **Find H in toroid with gap**
6. **Determine bound currents from given M**
7. **Apply Ampere's law in different geometries**

---

## CONCEPTUAL POINTS

1. **B vs H**: 
   - B is the total magnetic field
   - H is the field due to free currents only
   - In vacuum: B = μ₀H (since M = 0)

2. **Physical meaning of M**:
   - Magnetic dipole moment per unit volume
   - Represents alignment of atomic dipoles
   - M = 0 in unmagnetized materials

3. **Why bound currents?**:
   - Magnetization creates effective currents
   - J_b from circulation of M (like ∇ × M)
   - K_b from discontinuity of M at surface

4. **Linear materials**:
   - M proportional to H
   - Constant χ_m and μ
   - Simplifies calculations significantly

5. **Boundary conditions**:
   - Follow from Maxwell equations
   - Normal B continuous (∇·B = 0)
   - Tangential H has jump if K_f ≠ 0 (∇×H = J_f)

---

## FINAL TIPS FOR EXAM

✓ **Always specify coordinate system**
✓ **Check dimensions of your answer**
✓ **Draw diagrams for clarity**
✓ **Use symmetry to simplify**
✓ **State boundary conditions explicitly**
✓ **Verify direction using right-hand rule**
✓ **Remember: B is solenoidal (∇·B = 0)**
✓ **Remember: H depends only on free currents**

---
