# CFD_SOLVER_DEVELOPMENT 
# CFD From Scratch: 1D Advection, Diffusion & Advection-Diffusion Solvers

A learning-focused repository for developing numerical PDE solvers from first principles using Python.

The goal is to understand every component of a CFD solver:

- Grid generation
- Spatial discretization
- Temporal discretization
- Boundary conditions
- Ghost cells
- Matrix formation
- Explicit methods
- Implicit methods
- Verification and validation

---

# Learning Philosophy

This repository does not rely on CFD libraries.

Every solver is developed from the governing equation to the final implementation.

For each solver:

1. Write PDE
2. Discretize time
3. Discretize space
4. Rearrange discrete equation
5. Create grid
6. Define boundary conditions
7. Compute CFL/Fourier number
8. March in time
9. Verify solution
10. Compare implementations

---

# Solver Development Roadmap

## Phase 1: FTCS Solvers

### Advection Equation

\[
\frac{\partial u}{\partial t}
+
c\frac{\partial u}{\partial x}
=
0
\]

### Periodic Boundary Conditions

#### With Ghost Nodes

- [x] Loop Implementation
- [ ] Vectorized Implementation

#### Without Ghost Nodes

- [x] Interior + Boundary Update
- [ ] Modulo Indexing
- [ ] np.roll() Implementation

### Dirichlet Boundary Conditions

#### Both Sides Dirichlet

- [ ] Loop Implementation
- [ ] Vectorized Implementation

### Neumann Boundary Conditions

#### Zero Gradient

- [x] Loop Implementation
- [ ] Vectorized Implementation

#### Specified Gradient

- [ ] Loop Implementation
- [ ] Vectorized Implementation

---

## Diffusion Equation

\[
\frac{\partial u}{\partial t}
=
\alpha
\frac{\partial^2 u}{\partial x^2}
\]

### FTCS

#### Periodic BC

- [ ] With Ghost Nodes
- [ ] Without Ghost Nodes

#### Dirichlet BC

- [ ] Both Sides

#### Neumann BC

- [ ] Both Sides

---

## Advection-Diffusion Equation

\[
\frac{\partial u}{\partial t}
+
c\frac{\partial u}{\partial x}
=
\alpha
\frac{\partial^2 u}{\partial x^2}
\]

### FTCS

#### Periodic BC

- [ ] With Ghost Nodes
- [ ] Without Ghost Nodes

#### Dirichlet BC

- [ ] Both Sides

#### Neumann BC

- [ ] Both Sides

---

# Phase 2: Explicit Stable Schemes

## Advection

### FTBS (Upwind)

- [ ] Periodic
- [ ] Dirichlet
- [ ] Neumann

### Lax-Friedrichs

- [ ] Periodic
- [ ] Dirichlet
- [ ] Neumann

### Lax-Wendroff

- [ ] Periodic
- [ ] Dirichlet
- [ ] Neumann

### MacCormack

- [ ] Periodic
- [ ] Dirichlet
- [ ] Neumann

---

# Phase 3: Implicit Solvers

## BTCS

### Diffusion

- [ ] Matrix Formation
- [ ] Dirichlet BC
- [ ] Neumann BC
- [ ] Periodic BC

---

## Crank-Nicolson

### Diffusion

- [ ] Matrix Formation
- [ ] Dirichlet BC
- [ ] Neumann BC
- [ ] Periodic BC

---

# Phase 4: Matrix-Based CFD

## Understanding Linear Systems

### Topics

- [ ] Tridiagonal Matrices
- [ ] Sparse Matrices
- [ ] Boundary Row Modification
- [ ] Thomas Algorithm
- [ ] Matrix Assembly

---

# Phase 5: Verification Studies

## Grid Convergence

- [ ] Coarse Mesh
- [ ] Medium Mesh
- [ ] Fine Mesh

### Error Analysis

- [ ] L1 Norm
- [ ] L2 Norm
- [ ] L∞ Norm

### Observed Order of Accuracy

- [ ] First Order
- [ ] Second Order

---

# Phase 6: Vectorization

## Replace Loops Using NumPy

### Methods

- [ ] Array Slicing
- [ ] np.roll()
- [ ] Broadcasting

Performance comparisons:

- [ ] Loop Solver
- [ ] Vector Solver

---

# Phase 7: Toward Real CFD

## 2D Solvers

### Advection

- [ ] FTCS
- [ ] Upwind

### Diffusion

- [ ] FTCS
- [ ] BTCS
- [ ] Crank-Nicolson

### Advection-Diffusion

- [ ] Explicit
- [ ] Implicit

---

# Repository Structure
