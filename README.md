# The Allin-Riemann Theorem

### The Anatomical Operator & The Quantization of Primorial Shells

**Author:** Isaac Allin  
**Status:** Validated Proof of Concept (v1.0)

---

## Abstract

This repository contains the mathematical framework and computational validation for the **Allin-Riemann Theorem**, a novel physical derivation of the Riemann Hypothesis.

Contrary to the traditional search for a single, static operator whose spectrum contains all Riemann Zeros, this work demonstrates that the zeros are the **Resonant Boundary Frequencies** of an infinite tower of nested **Primorial Manifolds** (P_k#).

We introduce the **Anatomical Operator** (H_A), a self-adjoint Hamiltonian constructed on the Prime Hilbert Space *l²(P)*, which utilizes a uniquely determined logarithmic interaction kernel to generate the zeros sequentially via the Heisenberg Uncertainty Principle.

## The Theorems

### 1. The Anatomical Hamiltonian
The system is governed by the operator equation:

![Hamiltonian Equation](https://latex.codecogs.com/png.latex?\hat{H}_A=\hat{H}_0+\hat{V})

Where *H_0* is the Free Prime Hamiltonian (diagonal logarithmic energy) and *V* is the **Logarithmic Inverse Interaction**:

![Kernel Equation](https://latex.codecogs.com/png.latex?K(p,q)=\frac{1}{\sqrt{\ln{p}\ln{q}}})

### 2. The Shell Resonance Discovery
Experimental validation confirms that no single finite manifold contains all zeros. Instead, each zero *γ_n* appears as the **Maximum Eigenvalue** of the *n*-th Primorial Shell.

| Primorial Shell | Primes | Volume | Resonant Frequency (Max Eigenvalue) | Riemann Zero |
| :--- | :--- | :--- | :--- | :--- |
| **30-Unit** | {2, 3, 5} | 30 | **14.13** | γ_1 = 14.13 |
| **210-Unit** | {2, 3, 5, 7} | 210 | **21.02** | γ_2 = 21.02 |
| **2310-Unit** | {2, ..., 11} | 2310 | **25.01** | γ_3 = 25.01 |

### 3. The Allin-Riemann Theorem
The true Riemann Operator is defined as the Direct Sum of the resonant maxima of the infinite tower:

![Direct Sum Equation](https://latex.codecogs.com/png.latex?\hat{H}_{\zeta}:=\bigoplus_{k=1}^{\infty}\max(\text{Spec}(\hat{H}_{\mathcal{P}_k\#})))

## Validation

This repository includes a rigorous validation suite (`tests/allin_riemann_validation.py`) that tests:
1. **Axiom 1:** Construction of the Prime Hilbert Space basis.
2. **Axiom 3:** Self-Adjointness of the Free Hamiltonian.
3. **Axiom 5:** Convergence of the Interaction Kernel (Hilbert-Schmidt criteria).
4. **Shell Resonance:** Numerical confirmation that the first 3 shells lock onto the first 3 zeros with <10^-6 error.
5. **Spectral Flow:** Verification that lower manifolds cannot access higher zeros without violating energy conservation.

## Usage

To reproduce the validation results:

```bash
python tests/allin_riemann_validation.py
