# 📅 Day 3 — Prefix Sum

> **Status:** ✅ Completed
> **Duration:** ~1 Session
> **Focus:** Prefix Sum + HashMap Pattern Recognition

---

# 🎯 Goal

Understand how different problems can be solved using the same Prefix Sum + HashMap pattern by changing what the Prefix Sum represents.

---

# ✅ Problems Completed

- ✅ LC523 — Continuous Subarray Sum
- ✅ LC974 — Subarray Sums Divisible by K
- ✅ LC1248 — Count Number of Nice Subarrays

---

# 🧠 Concepts Learned

## LC523

### Pattern

Prefix Sum + Modulo

### HashMap Stores

```
Remainder → First Occurrence Index
```

### Key Observation

If two Prefix Sums have the same remainder,

```
(Prefix2 - Prefix1) % k == 0
```

then the subarray between them is divisible by `k`.

### Important Points

- Store only the first occurrence.
- `map.put(0,-1)` represents the empty prefix.
- Check subarray length:

```java
i - previousIndex >= 2
```

---

## LC974

### Pattern

Prefix Sum + Modulo

### HashMap Stores

```
Remainder → Frequency
```

### Key Observation

Instead of asking

> "Does a previous remainder exist?"

we ask

> "How many previous remainders exist?"

Hence

```java
count += map.get(rem);
```

---

## LC1248

### Pattern

Transform + Prefix Sum + HashMap

### Transformation

```
Odd  → 1
Even → 0
```

Instead of actually converting the array, maintain

```java
oddCount
```

which behaves exactly like a Prefix Sum.

### HashMap Stores

```
Odd Prefix Count → Frequency
```

### Key Observation

This problem is essentially **LC560** after transforming the meaning of the Prefix Sum.

---

# 💡 Biggest Realizations

### Prefix Sum is not always the sum of elements.

It can represent:

- Running Sum
- Number of Odd Elements
- Prefix Modulo
- Frequency Information

---

### The Prefix Sum algorithm remains almost identical.

Only the meaning of the Prefix changes.

---

### Choosing the HashMap value depends on the question.

| Requirement | HashMap Stores |
|-------------|----------------|
| Count | Frequency |
| Existence | First Index |
| Longest | First Index |
| Exact Sum | Prefix Sum |

---

# 📚 Pattern Revision

## LC560

```
Prefix Sum → Frequency
```

Equation

```
CurrentPrefix - PreviousPrefix = K
```

---

## LC523

```
Remainder → First Index
```

Equation

```
CurrentRemainder == PreviousRemainder
```

---

## LC974

```
Remainder → Frequency
```

Equation

```
CurrentRemainder == PreviousRemainder
```

---

## LC1248

```
Odd Prefix Count → Frequency
```

Equation

```
CurrentOddCount - PreviousOddCount = K
```

---

# ⚠️ Mistakes Corrected

- ✅ Mixed up Frequency and First Index in LC523.
- ✅ Understood why `map.put(0,-1)` is required.
- ✅ Learned not to overwrite the first occurrence.
- ✅ Understood the minimum subarray length condition.
- ✅ Realized LC1248 is simply LC560 after transformation.

---

# ⭐ Confidence

⭐⭐⭐⭐⭐ (5/5)

---

# 🚀 Progress

```text
████████████████████░ 90%

Completed
────────────
✅ Prefix Sum Basics
✅ LC1480
✅ LC303
✅ LC724
✅ LC1732
✅ LC2574
✅ LC560
✅ LC523
✅ LC974
✅ LC1248

Remaining
────────────
⬜ LC1590
⬜ Revision
```

---

# 🎯 Next Session

- LC1590 — Make Sum Divisible by P
- Full Prefix Sum Revision
- Blind Re-solving of important questions

---

# 🏁 Day 3 Takeaway

> "Today I stopped thinking about individual problems and started recognizing reusable patterns. Prefix Sum isn't just about cumulative sums—it can represent anything that accumulates over a traversal. The real skill is choosing what to accumulate and what information the HashMap should store."