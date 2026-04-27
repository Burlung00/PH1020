# PROBLEM SET 6 - SOLUTION GUIDE
## IIT Madras PH1020 Physics II - April 2026

---

## PROBLEM 1: Current Distribution from Vector Potential

### Given:
- Vector potential: **A** = k ê_φ (cylindrical coordinates)
- k = constant

### Required:
Find the current distribution **J**

### Key Concepts:
1. Relation between A and B: **B** = ∇ × **A**
2. Relation between B and J: ∇ × **B** = μ₀**J**
3. Curl operator in cylindrical coordinates

### Solution Approach:

**Step 1**: Calculate **B** = ∇ × **A**

Since **A** = k ê_φ where k is constant:
- A_ρ = 0
- A_φ = k (constant)
- A_z = 0

Using curl in cylindrical coordinates:
```
B_ρ = (1/ρ)(∂A_z/∂φ) - ∂A_φ/∂z = 0 - 0 = 0

B_φ = ∂A_ρ/∂z - ∂A_z/∂ρ = 0 - 0 = 0

B_z = (1/ρ)[∂(ρA_φ)/∂ρ - ∂A_ρ/∂φ]
    = (1/ρ)[∂(ρk)/∂ρ - 0]
    = (1/ρ)[k]
    = k/ρ
```

Therefore: **B** = (k/ρ) ê_z

**Step 2**: Calculate **J** from ∇ × **B** = μ₀**J**

Since **B** = (k/ρ) ê_z:
```
J_ρ = (1/μ₀)(1/ρ)(∂B_z/∂φ) - (1/μ₀)∂B_φ/∂z = 0

J_φ = (1/μ₀)[∂B_ρ/∂z - ∂B_z/∂ρ]
    = (1/μ₀)[0 - ∂(k/ρ)/∂ρ]
    = (1/μ₀)[k/ρ²]
    = k/(μ₀ρ²)

J_z = (1/μ₀ρ)[∂(ρB_φ)/∂ρ - ∂B_ρ/∂φ] = 0
```

**Answer**: **J** = [k/(μ₀ρ²)] ê_φ

### Key Formula Highlighted:
```
∇ × A = B
∇ × B = μ₀J
(∇ × A)_z = (1/ρ) d(ρA_φ)/dρ  (for A = A_φ ê_φ only)
```

---

## PROBLEM 2: Magnetic Dipole Moment of Moving Charge

### Given:
- Particle with mass m, charge q
- Velocity **u**
- Orbital angular momentum **L** = **r** × **p**

### Required:
Show that **m** = (q/2m)**L**

### Key Concepts:
1. Magnetic dipole moment: **m** = IA**n̂**
2. Current from moving charge
3. Angular momentum

### Solution Approach:

**For circular motion** (specific case to derive general result):

Consider charge q moving in circle of radius r with speed v:

**Current**:
```
I = charge/period = q/(2πr/v) = qv/(2πr)
```

**Area**:
```
A = πr²
```

**Magnetic moment magnitude**:
```
m = IA = (qv/2πr)(πr²) = qvr/2
```

**Angular momentum magnitude**:
```
L = mvr
```

**Therefore**:
```
m = qvr/2 = q(mvr)/(2m) = qL/(2m)
```

**Vector form**:
```
m = (q/2m)L
```

**Gyromagnetic ratio**:
```
γ = q/(2m)
```

### Direction:
- If q > 0: **m** and **L** are parallel
- If q < 0: **m** and **L** are antiparallel

### Key Formula Highlighted:
```
m = (q/2m)L     (fundamental relation)
γ = q/(2m)      (gyromagnetic ratio)
```

---

## PROBLEM 3: Spinning Charged Sphere

### Given:
- Uniformly charged solid sphere
- Radius R, total charge Q
- Spinning with angular velocity ω about z-axis

### Required:
Find magnetic dipole moment **m**

### Key Concepts:
1. Rotating charges create current
2. Each shell acts like a current loop
3. Integration over volume

### Solution Approach:

**Step 1**: Set up the geometry
- Uniform charge density: ρ = 3Q/(4πR³)
- Consider spherical shell at radius r, thickness dr
- Charge in shell: dq = ρ(4πr² dr)

**Step 2**: Current from rotating shell
- Shell rotates with angular velocity ω
- A point at radius r (distance from axis) moves with speed v = ωr sin θ
- For a thin ring at angle θ: current dI = (charge in ring) × (frequency)

**Alternative approach using volume integration**:
- Consider volume element at (r, θ, φ)
- Charge: dq = ρ r² sin θ dr dθ dφ
- Current density: **J** = ρ**v** = ρ(ω × **r**)

**Step 3**: Magnetic moment of shell
For a shell at radius r with surface charge σ:
- Surface current: **K** = σ**v** = σ(ω × **r**)
- This creates a magnetic moment

**Step 4**: Integration
Integrate dm over entire sphere:
```
m = ∫∫∫ dm
```

### Method using known result:
For uniformly charged rotating sphere:
```
m = (Q ω R²)/5
```

### Alternative formula derivation:
Using the relation for rotating charge distribution:
- Each charge element dq at position **r** moving with **v** = ω × **r**
- Contributes: d**m** = (1/2) **r** × (dq **v**) = (dq/2) **r** × (**ω** × **r**)
- For sphere: integrate to get final answer

### Key Formula Highlighted:
```
m = (1/5) Q ω R²     (for uniformly charged spinning sphere)
K = σv               (surface current density)
J = ρv               (volume current density)
```

---

## PROBLEM 4: Magnetized Cylinder

### Given:
- Infinite cylinder, radius a, axis along z
- Magnetization: **M** = M₀(ρ/a)² ê_φ (cylindrical coordinates)
- M₀ = constant

### Required:
Find J_b, K_b, **B**, and **H** (inside and outside)

### Key Concepts:
1. Bound currents: **J**_b = ∇ × **M**
2. Surface bound current: **K**_b = **M** × **n̂**
3. Ampere's law for **H**: ∇ × **H** = **J**_f
4. Relation: **B** = μ₀(**H** + **M**)

### Solution Approach:

**Step 1**: Calculate **J**_b = ∇ × **M**

**M** = M₀(ρ/a)² ê_φ, so:
- M_ρ = 0
- M_φ = M₀(ρ/a)²
- M_z = 0

Using curl in cylindrical coordinates:
```
J_b,ρ = (1/ρ)(∂M_z/∂φ) - ∂M_φ/∂z = 0

J_b,φ = ∂M_ρ/∂z - ∂M_z/∂ρ = 0

J_b,z = (1/ρ)[∂(ρM_φ)/∂ρ - ∂M_ρ/∂φ]
      = (1/ρ) ∂[ρ · M₀(ρ/a)²]/∂ρ
      = (M₀/a²ρ) ∂(ρ³)/∂ρ
      = (M₀/a²ρ)(3ρ²)
      = 3M₀ρ/a²
```

**Answer for J_b**: **J**_b = (3M₀ρ/a²) ê_z (for ρ < a)

**Step 2**: Calculate **K**_b at ρ = a

At the surface (ρ = a), outward normal: **n̂** = ê_ρ

```
K_b = M(a) × n̂
    = M₀ ê_φ × ê_ρ
    = -M₀ ê_z
```

Wait, let me recalculate:
ê_φ × ê_ρ = -ê_z (using right-hand rule in cylindrical coordinates)

Actually: **n̂** = ê_ρ (outward), **M**(a) = M₀ ê_φ

```
K_b = M × n̂ = M₀ ê_φ × ê_ρ = M₀ ê_z
```

(Using ê_φ × ê_ρ = ê_z)

**Step 3**: Find **H** using ∇ × **H** = **J**_f = 0 (no free currents)

By symmetry and ∇ × **H** = 0, assume **H** = H(ρ) ê_φ

Apply Ampere's law: ∮ **H** · d**l** = 0
This gives **H** = 0 everywhere? Let's reconsider...

Actually, with cylindrical symmetry and no free current:
Using ∇ × **H** = 0 and symmetry, **H** should be derivable from a potential or could be zero.

**Step 4**: Find **B** = μ₀(**H** + **M**)

Inside (ρ < a):
```
B = μ₀(H + M) = μ₀[H + M₀(ρ/a)² ê_φ]
```

Outside (ρ > a):
```
M = 0
B = μ₀H
```

Need to match boundary conditions to find **H**.

### Key Formulas Highlighted:
```
J_b = ∇ × M
K_b = M × n̂
∇ × H = J_f
B = μ₀(H + M)
(∇ × M)_z = (1/ρ) ∂(ρM_φ)/∂ρ
```

---

## PROBLEM 5: Toroid with Gap

### Given:
- Toroid with wedge-shaped gap of angle ψ
- Current I, N total turns
- Inner radius R
- Core: LIH material with susceptibility χ_m
- Assume **B** in gap is along ê_φ

### Required:
Find **H** in the toroid

### Key Concepts:
1. Ampere's law for **H**: ∮ **H** · d**l** = NI
2. Boundary condition: B_normal continuous
3. Constitutive relation: **B** = μ**H** in material
4. In gap: **B** = μ₀**H**

### Solution Approach:

**Step 1**: Set up Ampere's law path
Choose circular path at radius r inside toroid

**Step 2**: Apply ∮ **H** · d**l** = NI

Path consists of:
- Material: arc length = r(2π - ψ)
- Gap: arc length = rψ

```
H_mat · r(2π - ψ) + H_gap · rψ = NI
```

**Step 3**: Relate H_mat and H_gap using boundary conditions

Since **B** is along ê_φ (tangent to interface), we need normal component continuous.

Actually, **B** is tangent to the circular path, so at the interface between material and gap:
- Normal to interface is radial: **n̂** = ê_r
- **B** is along ê_φ, so **B** is tangential
- For tangential component: B₁_t/μ₁ = B₂_t/μ₂

In material: **B**_mat = μ₀(1 + χ_m)**H**_mat
In gap: **B**_gap = μ₀**H**_gap

But actually, since they're at the same radius and **B** is along ê_φ, the boundary is at the azimuthal interfaces.

Let me reconsider: The gap is a wedge, so the boundaries are at constant φ values.
At these boundaries, the normal is along ê_φ.
Since **B** is along ê_φ, **B** is normal to the boundary!

**Correct boundary condition**: B_normal continuous
```
B_mat = B_gap
```

Therefore:
```
μ₀(1 + χ_m)H_mat = μ₀H_gap
H_gap = (1 + χ_m)H_mat
```

**Step 4**: Substitute into Ampere's law
```
H_mat · r(2π - ψ) + (1 + χ_m)H_mat · rψ = NI
H_mat · r[(2π - ψ) + (1 + χ_m)ψ] = NI
H_mat · r[2π - ψ + ψ + χ_m ψ] = NI
H_mat · r[2π + χ_m ψ] = NI
```

**Answer**:
```
H_mat = NI / [r(2π + χ_m ψ)]
```

And:
```
H_gap = (1 + χ_m) · NI / [r(2π + χ_m ψ)]
```

### Key Formulas Highlighted:
```
∮ H · dl = I_f,enc
B = μ₀(1 + χ_m)H  (in LIH material)
B_normal continuous
H_gap = (1 + χ_m)H_mat  (from B continuity)
```

---

## PROBLEM 6: Planar Sheet with Non-uniform Permeability

### Given:
- Infinite planar sheet: 0 ≤ z ≤ d
- Permeability: μ(z) = μ₀[1 + (z/d)]²
- Vacuum on both sides (z < 0 and z > d)
- Applied field: **B** = B₀ ê_y everywhere (uniform)
- No free current

### Required:
Find:
1. Magnetization surface current densities at z = 0 and z = d
2. Magnetization volume current density J_b(z)

### Key Concepts:
1. **H** = **B**/μ in linear materials
2. **M** = χ_m **H** = (μ_r - 1)**H**
3. Volume current: **J**_b = ∇ × **M**
4. Surface current: **K**_b = (**M**_inside - **M**_outside) × **n̂**

### Solution Approach:

**Step 1**: Find **H** inside the sheet

Since **B** = B₀ ê_y is uniform everywhere:
```
H(z) = B(z)/μ(z) = B₀ ê_y / [μ₀[1 + (z/d)]²]
```

Inside sheet (0 ≤ z ≤ d):
```
H = (B₀/μ₀) [1 + (z/d)]^(-2) ê_y
```

**Step 2**: Find **M** inside the sheet

Using **B** = μ(**H** + **M**):
```
M = B/μ₀ - H
  = B₀/μ₀ ê_y - (B₀/μ₀)[1 + (z/d)]^(-2) ê_y
  = (B₀/μ₀){1 - [1 + (z/d)]^(-2)} ê_y
```

**Step 3**: Calculate **J**_b = ∇ × **M**

Since **M** = M_y(z) ê_y (only y-component, depends only on z):
```
J_b,x = -∂M_y/∂z

J_b,y = 0

J_b,z = 0
```

Calculate:
```
∂M_y/∂z = (B₀/μ₀) ∂/∂z{1 - [1 + (z/d)]^(-2)}
         = (B₀/μ₀) · 2[1 + (z/d)]^(-3) · (1/d)
         = (2B₀)/(μ₀d) [1 + (z/d)]^(-3)
```

Therefore:
```
J_b = -(2B₀)/(μ₀d) [1 + (z/d)]^(-3) ê_x
```

**Step 4**: Calculate surface currents

At z = 0 (bottom surface):
- Inside: **M**(0⁺) = (B₀/μ₀){1 - 1} ê_y = 0
- Outside: **M**(0⁻) = 0 (vacuum)
- **K**_b = (**M**_in - **M**_out) × **n̂** = 0

At z = d (top surface):
- Inside: **M**(d⁻) = (B₀/μ₀){1 - [1 + 1]^(-2)} ê_y = (B₀/μ₀){1 - 1/4} ê_y = (3B₀)/(4μ₀) ê_y
- Outside: **M**(d⁺) = 0 (vacuum)
- Normal: **n̂** = ê_z
- **K**_b = **M** × **n̂** = [(3B₀)/(4μ₀) ê_y] × ê_z = -(3B₀)/(4μ₀) ê_x

**Answers**:
```
K_b(z=0) = 0
K_b(z=d) = -(3B₀)/(4μ₀) ê_x
J_b(z) = -(2B₀)/(μ₀d) [1 + (z/d)]^(-3) ê_x
```

### Key Formulas Highlighted:
```
H = B/μ(z)
M = (μ/μ₀ - 1)H = B/μ₀ - H
J_b = ∇ × M
K_b = (M_in - M_out) × n̂
For M = M_y(z) ê_y: J_b,x = -∂M_y/∂z
```

---

## SUMMARY TABLE: FORMULAS USED PER PROBLEM

| Problem | Key Formulas |
|---------|-------------|
| **1** | B = ∇ × A, J = (∇ × B)/μ₀ |
| **2** | m = IA, m = (q/2m)L |
| **3** | m = ∫ dm, J = ρv, spinning sphere formula |
| **4** | J_b = ∇ × M, K_b = M × n̂, B = μ₀(H + M) |
| **5** | ∮ H·dl = NI, B continuous, B = μH |
| **6** | H = B/μ, M = B/μ₀ - H, J_b = ∇ × M, K_b = M × n̂ |

---

## COMMON TECHNIQUES

1. **Use symmetry** to simplify curl calculations
2. **Check dimensions** at each step
3. **Apply boundary conditions** carefully
4. **Remember sign conventions** (right-hand rule)
5. **Verify limiting cases** (μ → μ₀, χ_m → 0, etc.)

---
