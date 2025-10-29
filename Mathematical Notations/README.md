# 🧠 Theory of Computation – Mathematical Notations

## ⚙️ 1. SETS

**Definition:** A set is a collection of distinct objects or elements.

**Example:** `A = {1, 2, 3, 4}`

### Set Membership & Relations

| Symbol | Meaning | Example | Explanation |
|--------|---------|---------|-------------|
| `∈` | belongs to | `2 ∈ A` | 2 is an element of A |
| `∉` | does not belong to | `5 ∉ A` | 5 is not in A |
| `⊆` | subset | `{1,2} ⊆ A` | all elements are in A |
| `⊂` | proper subset | `{1,2} ⊂ A` | subset but not equal to A |
| `⊇` | superset | `A ⊇ {1,2}` | A contains all these elements |
| `\|A\|` | cardinality | `\|A\| = 4` | number of elements in A |

---

## 💡 2. SET OPERATIONS

| Operation | Symbol | Example | Result | Meaning |
|-----------|--------|---------|--------|---------|
| **Union** | `∪` | `{1,2} ∪ {2,3}` | `{1,2,3}` | Combine both sets |
| **Intersection** | `∩` | `{1,2} ∩ {2,3}` | `{2}` | Common elements only |
| **Difference** | `−` | `{1,2,3} − {2}` | `{1,3}` | Elements only in first set |
| **Complement** | `A′` or `Ā` | `U={1,2,3,4}, A={1,2}` | `A′={3,4}` | Elements not in A |

### Important Set Rules

```
✓ A ∪ ∅ = A                  (union with empty set)
✓ A ∩ ∅ = ∅                  (intersection with empty set)
✓ A ∪ A′ = U                 (union with complement = universe)
✓ A ∩ A′ = ∅                 (intersection with complement = empty)
✓ (A′)′ = A                  (complement of complement)
✓ A − B = A ∩ B′             (difference as intersection)
```

---

## 🔢 3. TUPLES / SEQUENCES

**Definition:** An ordered list of elements where **order matters**.

**Key Point:** `(a, b) ≠ (b, a)`

**Example in Automata:** `(q, a)` → represents state `q` with input symbol `a`

---

## 🔠 4. ALPHABET (Σ)

**Definition:** A finite set of symbols used to construct strings.

**Examples:**
- `Σ = {0, 1}` → Binary alphabet
- `Σ = {a, b, c}` → Simple alphabet
- `Σ = {a, b, ..., z}` → English lowercase letters

---

## 🔤 5. STRINGS

**Definition:** A finite sequence of symbols from an alphabet Σ.

### String Notation

| Notation | Meaning | Example |
|----------|---------|---------|
| `w` | A string | `w = 0101` |
| `\|w\|` | Length of string | `\|0101\| = 4` |
| `ε` | Empty string | `\|ε\| = 0` |
| `xy` | Concatenation | `x=01, y=10 → xy=0110` |

### String Operations

**Concatenation:** Joining strings in order
```
x = "01"
y = "10"
xy = "0110"
```

---

## 💥 6. POWERS OF STRINGS

| Notation | Meaning | Example (w = "ab") |
|----------|---------|-------------------|
| `w⁰` | Empty string | `ε` |
| `w¹` | String itself | `ab` |
| `w²` | String repeated twice | `abab` |
| `w³` | String repeated thrice | `ababab` |
| `wⁿ` | String repeated n times | `w⁵ = ababababab` |

---

## 🌌 7. KLEENE STAR & PLUS

Used to generate languages from alphabets.

| Symbol | Name | Meaning | Example (Σ = {0, 1}) |
|--------|------|---------|----------------------|
| `Σ*` | Kleene Star | All possible strings (including ε) | `{ε, 0, 1, 00, 01, 10, 11, 000, ...}` |
| `Σ⁺` | Kleene Plus | All non-empty strings | `{0, 1, 00, 01, 10, 11, 000, ...}` |

### Key Relationship
```
Σ* = Σ⁺ ∪ {ε}
```

**Example with Σ = {a}:**
- `Σ* = {ε, a, aa, aaa, aaaa, ...}`
- `Σ⁺ = {a, aa, aaa, aaaa, ...}`

---

## 📚 8. LANGUAGES (L)

**Definition:** A set of strings formed using alphabet Σ.

**Example:**
```
L = {w | w contains at least one '1'}
L = {1, 01, 10, 11, 101, 110, ...}
```

### Language Operations

| Operation | Symbol | Example | Meaning |
|-----------|--------|---------|---------|
| **Union** | `L₁ ∪ L₂` | `{a,b} ∪ {b,c} = {a,b,c}` | Strings in either language |
| **Intersection** | `L₁ ∩ L₂` | `{ab,ba} ∩ {ab,cd} = {ab}` | Strings in both languages |
| **Concatenation** | `L₁L₂` | `{a}{b} = {ab}` | All combinations joined |
| **Kleene Star** | `L*` | `{a}* = {ε,a,aa,aaa,...}` | Repeat any number of times |
| **Complement** | `L′` or `L̄` | `Σ* − L` | Strings not in L |

### Concatenation Example
```
L₁ = {a, ab}
L₂ = {c, cd}
L₁L₂ = {ac, acd, abc, abcd}
```

---

## ⚡ 9. RELATIONS & FUNCTIONS

### Relations

**Definition:** A connection between elements of two sets.

**Notation:** `R ⊆ A × B`

**Example:**
```
A = {a, b}
B = {1, 2}
R = {(a,1), (b,2), (b,1)}
```

### Functions

**Definition:** A special relation where each input maps to **exactly one** output.

**Notation:** `f: A → B`

**Example:**
```
f(a) = 1
f(b) = 2
```

### Key Rule
```
✓ Every function is a relation
✗ Not every relation is a function
```

---

## 🧩 10. CARTESIAN PRODUCT

**Definition:** All possible ordered pairs between two sets.

**Notation:** `A × B`

**Example:**
```
A = {1, 2}
B = {x, y}

A × B = {(1,x), (1,y), (2,x), (2,y)}
```

### Size Formula
```
|A × B| = |A| × |B|
```

If `|A| = 2` and `|B| = 3`, then `|A × B| = 6`

---

## 🌀 11. POWER SET

**Definition:** The set of all possible subsets of a set.

**Notation:** `P(A)` or `2^A`

**Example:**
```
A = {1, 2}
P(A) = {∅, {1}, {2}, {1,2}}
```

### Size Formula
```
If |A| = n, then |P(A)| = 2ⁿ
```

**Example:**
- `A = {a, b, c}` where `|A| = 3`
- `|P(A)| = 2³ = 8` subsets

```
P(A) = {
  ∅, 
  {a}, {b}, {c}, 
  {a,b}, {a,c}, {b,c}, 
  {a,b,c}
}
```

---

## 🧮 12. LOGICAL OPERATORS

### Basic Operators

| Symbol | Name | Example | Meaning |
|--------|------|---------|---------|
| `¬` | NOT | `¬p` | Negation of p |
| `∧` | AND | `p ∧ q` | Both must be true |
| `∨` | OR | `p ∨ q` | At least one is true |
| `→` | IMPLIES | `p → q` | If p then q |
| `↔` | IFF | `p ↔ q` | If and only if (both ways) |

### Truth Table Quick Reference

| p | q | p∧q | p∨q | p→q | p↔q |
|---|---|-----|-----|-----|-----|
| T | T | T   | T   | T   | T   |
| T | F | F   | T   | F   | F   |
| F | T | F   | T   | T   | F   |
| F | F | F   | F   | T   | T   |

### Important Logical Laws

**Commutative Laws:**
```
p ∨ q = q ∨ p
p ∧ q = q ∧ p
```

**De Morgan's Laws:**
```
¬(p ∨ q) = ¬p ∧ ¬q
¬(p ∧ q) = ¬p ∨ ¬q
```

**Implication:**
```
p → q = ¬p ∨ q
```

**Double Negation:**
```
¬(¬p) = p
```

---

## 🧠 13. QUANTIFIERS

Used in formal logic and proofs.

| Symbol | Name | Example | Meaning |
|--------|------|---------|---------|
| `∀` | Universal | `∀x (x² ≥ 0)` | For all x, x squared is non-negative |
| `∃` | Existential | `∃x (x = 2)` | There exists an x such that x equals 2 |

### Examples in Context

**Universal Quantifier:**
```
∀x ∈ N (x ≥ 0)
"For all x in natural numbers, x is greater than or equal to 0"
```

**Existential Quantifier:**
```
∃x ∈ R (x² = 4)
"There exists an x in real numbers such that x squared equals 4"
```

### Negation Rules
```
¬(∀x P(x)) = ∃x ¬P(x)
¬(∃x P(x)) = ∀x ¬P(x)
```

---

## 📝 Quick Reference Summary

### Most Common Symbols

| Category | Symbols |
|----------|---------|
| **Sets** | `∈, ∉, ⊆, ⊂, ∪, ∩, −, ′` |
| **Strings** | `Σ, ε, *, ⁺, \|w\|` |
| **Logic** | `¬, ∧, ∨, →, ↔, ∀, ∃` |
| **Relations** | `×, ⊆, →` |

---
