# System Stability 

## 1. Find the poles
- Express the transfer function as:

  \[
  G(s) = \frac{N(s)}{D(s)}
  \]

  where \(N(s)\) is the numerator polynomial and \(D(s)\) is the denominator (the characteristic polynomial).
- The roots of \(D(s) = 0\) are the **poles** of the system.


## 2. Check pole locations in the complex \(s\)-plane
- **Stable system (BIBO stable)**
  - All poles have **strictly negative real parts** (open left-half plane).
  - \(\Re(s_i) < 0 \quad \forall i\)

- **Unstable system**
  - At least one pole has a **positive real part**.
  - \(\exists \; s_i \; \text{with} \; \Re(s_i) > 0\)

- **Marginally stable system**
  - No poles in the right-half plane,
  - At least one pole lies **on the imaginary axis** (\(\Re(s_i) = 0\)),
  - Those poles must be **simple** (multiplicity 1).
    - Example: a single pole at \(s = j\omega\) or \(s = 0\) → sustained oscillations or constant output.
    - Repeated poles on the imaginary axis → **unstable**.


## 3. Special cases
- **Pole at the origin (\(s=0\))**
  - Single pole → marginally stable (integrator).
  - Repeated pole → unstable.

- **Imaginary axis poles (\(\pm j\omega\))**
  - Single pair → marginally stable (sustained oscillations).
  - Multiple/repeated pair → unstable.


## Quick rule of thumb
- **All poles in left-half plane** → Stable  
- **Any pole in right-half plane** → Unstable  
- **Simple poles on imaginary axis only** → Marginally stable  
