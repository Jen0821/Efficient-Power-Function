# ⚡ Haskell Power Function Implementation and Efficiency Comparison

## Overview

This project implements the mathematical **power function ($n^k$)** for non-negative integer exponents ($k \ge 0$) using **three distinct algorithmic approaches** in **Haskell**. The primary goal is to compare the implementation methodologies—from basic recursion to highly efficient recursive structures—highlighting expertise in functional programming principles and algorithmic efficiency analysis.

## Key Implementations

The core of the project involves defining the power function in three ways:

| Function | Description | Core Concept |
| :--- | :--- | :--- |
| `power n k` | The **standard recursive** definition: $n^k = n \cdot n^{k-1}$. | Demonstrates fundamental recursion and base cases. |
| `power1 n k` | Utilizes Haskell's List Prelude functions (`replicate`, `product`) to generate a list and compute its product. | Showcases the use of higher-order functions for concise solutions. |
| `power2 n k` | An **efficient, optimised recursive** implementation. It uses the property $n^k = (n \cdot n)^{k/2}$ when $k$ is even to significantly reduce the number of multiplications (Divide and Conquer). | Focuses on **algorithmic time complexity** and optimisation. |

## Verification and Testing

To ensure correctness, the project includes automated comparison functions:

* `comparePower1 n k`: Compares the result of `power n k` with `power1 n k`.
* `comparePower2 n k`: Compares the result of `power n k` with `power2 n k`.
* `comparisonList ns ks`: Generates a list of test results for the **Cartesian product** of input lists of $n$ and $k$ values, providing a robust test suite outcome.

## Compilation and Usage

This project uses the standard Haskell ecosystem managed by **Cabal**.

### 🛠 Dependencies
* GHC (Glasgow Haskell Compiler)
* Cabal Build Tool

### 🚀 Build and Test

```bash
# Update package list (if necessary)
cabal update

# Build the project and its test executables
cabal build

# Run the test suite to verify all implementations
cabal test

# Load the module in GHCi for interactive use
cabal repl
