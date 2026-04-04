# **Shiftless & Carryless Collatz Models** 
## **A New Visualization Framework for the $3n+1$ Problem via $\text{GF}(2)$ Algebraic Analysis × Fractal Geometry × Information Theory**
Hiroshi Harada - April 4, 2026

---

## 🧭 **Overview**

This repository is a collection of research code for analyzing the unsolved **Collatz conjecture ($3n+1$ problem)** from a new perspective: **information flow, fractal structures, and $\text{GF}(2)$ algebra**.

In the traditional Collatz map, observing the internal structure of the trajectory is hindered by:

- Information loss due to **right shifts (÷2)** in even steps.
- Structural destruction caused by carries (carry propagation) during the **$3n+1$** odd steps.

To solve this problem, this repository introduces the following three models.

---

### ✔ Shiftless Model

Constructs a **Collatz map that discards zero information** by eliminating right shifts and preserving the weight of the LSB.

Update rule:
$$n_{k+1} = 3n_k + \text{LSB}(n_k)$$

---

### ✔ Redundant Binary (RB) Representation

Fully records the Shiftless trajectory by retaining carries during addition as **polynomial coefficients** instead of processing them immediately.

Evaluating the RB polynomial at $x=2$ perfectly matches the Shiftless integer value.

---

### ✔ Carryless Model

Extracts the **pure fractal skeleton (Rule 90)** by projecting the coefficients of the RB polynomial onto **$\text{GF}(2)$** (mod 2), completely eliminating carries.

---

## 🔥 **Cellular Automaton (Rule 90) and the Emergence of Chaos**

The analysis in this project clarifies that the complexity of the Collatz trajectory can be explained by the interference of three elements: **Order × Noise × Carry**.

---

### 🟦 1. Order: $3n$ without carries is equivalent to Rule 90

As a $\text{GF}(2)$ polynomial, the carryless $3n$ becomes:
$$(x+1)P(x)$$
which perfectly matches the 1D cellular automaton **Rule 90**.

→ **A pure Sierpiński gasket emerges.**

---

### 🟧 2. Noise: LSB injection disrupts the fractal

In the Shiftless model, at each step, **LSB noise** is injected:
$$x^{L_k}$$

→ It enters the "holes" of the fractal, causing local disturbances.

---

### 🔴 3. Chaos: Carry avalanches destroy the structure

In the standard Collatz ($3n+1$), LSB noise triggers carries, resulting in **global structural destruction (carry avalanches)**.

→ The collision of **Order × Noise × Carry** generates the "chaos" of the Collatz trajectory.

---

## 📂 **Included Scripts**

This repository includes the following analysis code.

| File Name | Description |
|-----------|-------------|
| `code_01_equivalence_shiftless.py` | Verifies equivalence between Shiftless and standard Collatz (odd sequence) |
| `code_02_equivalence_rb.py` | Verifies perfect match between RB polynomials and Shiftless |
| `code_03_3n.py` | Visualizes fractal destruction with and without $3n$ carries |
| `code_04_carryless.py` | Compares Shiftless (noise + carry) and Carryless (noise only) |

---

## 🛠 **Requirements**

- Python 3.8+
- NumPy
- Matplotlib

```bash
pip install numpy matplotlib
```

---

## ▶️ **Usage**

Each script can be run independently.

Example:

```bash
python code_03_3n_carry_vs_carryless.py
```

The generated figures allow you to visually compare the differences between:

- Fractal structures
- Noise injection
- Carry avalanches

---

## 📜 **License**

- Python Source Code: **MIT License** - Research Documents / Theory: **CC BY 4.0** - Copyright (c) 2026 Hiroshi Harada

---

## 🌌 **About This Project**

This repository is designed as a **"new platform to play with Collatz."**

- Fractals
- Cellular Automata
- $\text{GF}(2)$
- Information Theory
- Number Theory

It is created as a "playground" where these fields intersect, allowing researchers, math enthusiasts, and programmers to explore freely.

