# CLP3

# Genetic Algorithm: Evolve List with Target Product

This project uses a **Genetic Algorithm (GA)** to find a list of `k` digits (from 0 to 9) such that their **product equals a target integer `T`**.

## 🔍 Problem Statement

Given:
- A target product `T`
- A fixed list length `k`
- Digits must be in the range `[0–9]`

Goal:
> Evolve a list of `k` integers where the **product of all numbers equals `T`**.

---

## 🧬 Approach: Genetic Algorithm

The solution applies standard GA components:

- **Population Initialization**: Random lists of `k` integers from 0 to 9.
- **Fitness Function**: Closeness of the list's product to `T`.
- **Selection**: Roulette wheel selection based on fitness.
- **Crossover**: One-point crossover to mix parents.
- **Mutation**: Randomly replace digits with a small probability.
- **Termination**: Stop when a solution is found or after max generations.

---

## ✅ Example Usage

```python
# Example test cases
result1 = evolve(12, 3)
result2 = evolve(18, 3)

print("Case#1 Output:", *result1 if result1 else ["No solution"])
print("Case#2 Output:", *result2 if result2 else ["No solution"])


Case#1 Output: 2 3 2
Case#2 Output: 3 3 2
