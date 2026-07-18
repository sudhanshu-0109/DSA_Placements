# 📘 Module 2: Prefix Sum

> **Status:** 🚀 In Progress  
> **Planned Duration:** 6 Days  
> **Difficulty:** ⭐⭐☆☆☆ → ⭐⭐⭐⭐☆

---

# 🎯 Module Objective

The Prefix Sum module teaches you how to preprocess cumulative information to answer range-based queries efficiently.

By completing this module, you should be able to:

- Build Prefix Sum arrays from scratch.
- Solve range sum problems in O(1).
- Identify Prefix Sum patterns quickly.
- Combine Prefix Sum with HashMap.
- Solve subarray-related interview questions.

---

# 📅 Module Plan

| Day | Topics |
|-----|--------|
| **Day 1** | Prefix Sum Theory + LC 1480 + LC 303 |
| **Day 2** | LC 724 + LC 1732 + LC 2574 |
| **Day 3** | Prefix Sum + HashMap + LC 560 |
| **Day 4** | LC 523 + LC 525 + LC 930 |
| **Day 5** | LC 974 + LC 1248 + LC 1590 |
| **Day 6** | Revision + Re-solving Important Questions |

---

# 📚 Theory Checklist

## Prefix Sum Basics

- [ ] What is Prefix Sum?
- [ ] Why Prefix Sum?
- [ ] Prefix Array Construction
- [ ] In-place Prefix Sum
- [ ] Range Sum Query
- [ ] Prefix Sum Formula
- [ ] Time Complexity
- [ ] Space Complexity

---

## Prefix Sum + HashMap

- [ ] Why HashMap is Required
- [ ] Prefix Sum Frequency
- [ ] Counting Subarrays
- [ ] Running Prefix Sum
- [ ] Handling Negative Numbers

---

# 🟢 Easy Problems

- [ ] LC 1480 — Running Sum of 1D Array
- [ ] LC 303 — Range Sum Query - Immutable
- [ ] LC 724 — Find Pivot Index
- [ ] LC 1732 — Find the Highest Altitude
- [ ] LC 2574 — Left and Right Sum Differences

---

# 🟡 Medium Problems

- [ ] LC 560 — Subarray Sum Equals K ⭐⭐⭐⭐⭐
- [ ] LC 523 — Continuous Subarray Sum
- [ ] LC 525 — Contiguous Array
- [ ] LC 930 — Binary Subarrays With Sum
- [ ] LC 974 — Subarray Sums Divisible by K
- [ ] LC 1248 — Count Number of Nice Subarrays
- [ ] LC 1590 — Make Sum Divisible by P

---

# 🔴 Advanced (Optional)

- [ ] LC 1074 — Number of Submatrices That Sum to Target
- [ ] 2D Prefix Sum
- [ ] Prefix XOR
- [ ] Difference Array
- [ ] Coordinate Compression + Prefix Sum

---

# 💡 Key Concepts Learned

## Prefix Sum

✔ Cumulative Sum

✔ Running Sum

✔ Range Sum Query

✔ O(1) Query Time

✔ Prefix Array Construction

---

## Prefix Sum + HashMap

✔ Frequency Counting

✔ Subarray Counting

✔ Prefix Difference

✔ Handling Negative Numbers

✔ Fast Lookup

---

# 🧠 Important Observations

- Prefix Sum stores cumulative information instead of recalculating sums.
- Range Sum Queries become O(1) after preprocessing.
- Prefix Sum alone solves many easy problems.
- Prefix Sum + HashMap is one of the most common interview patterns.
- Many subarray problems become simple once Prefix Sum is recognized.
- Always think about cumulative information before using nested loops.

---

# ⚠️ Common Mistakes

- [ ] Forgetting the Range Sum formula.
- [ ] Incorrect Prefix Array construction.
- [ ] Forgetting `map.put(0,1)` in LC 560.
- [ ] Updating HashMap before checking the answer.
- [ ] Off-by-one errors.
- [ ] Confusing Prefix Sum with Sliding Window.

---

# 🔁 Revision Checklist

Without looking at previous solutions:

## Theory

- [ ] Explain Prefix Sum.
- [ ] Explain Range Sum Query.
- [ ] Explain Prefix + HashMap.

---

## Coding

- [ ] Build Prefix Array
- [ ] LC 1480
- [ ] LC 303
- [ ] LC 724
- [ ] LC 560
- [ ] LC 523
- [ ] LC 525

---

## Understanding

- [ ] Can identify Prefix Sum problems quickly.
- [ ] Know when Prefix Sum alone is enough.
- [ ] Know when HashMap is required.

---

# 📝 Notes

## Pattern

Prefix Sum

---

## Core Idea

Store cumulative information to avoid repeated calculations.

---

## Formula

```text
prefix[i] = prefix[i-1] + arr[i]
```

---

### Range Sum Formula

```text
If L == 0

sum = prefix[R]

Else

sum = prefix[R] - prefix[L-1]
```

---

## When to Use

- Range Sum Query
- Running Sum
- Left vs Right Sum
- Subarray Problems
- Prefix + HashMap
- Frequency Counting

---

## Time Complexity

| Operation | Complexity |
|-----------|------------|
| Build Prefix Array | O(n) |
| Range Query | O(1) |
| Prefix + HashMap | O(n) |

---

## Space Complexity

| Method | Complexity |
|---------|------------|
| Prefix Array | O(n) |
| In-place Prefix | O(1) |
| Prefix + HashMap | O(n) |

---

# 🏁 Module Completion Criteria

- [ ] Understand Prefix Sum.
- [ ] Understand Prefix + HashMap.
- [ ] Complete all Easy Problems.
- [ ] Complete all Medium Problems.
- [ ] Solve LC 560 without hints.
- [ ] Complete Revision Day.
- [ ] Ready for Two Pointers.

---

# 📊 Progress

```text
░░░░░░░░░░░░░░░░░░░░ 0%

Module 2 Started 🚀
```

*(Update as you progress!)*

```text
██████░░░░░░░░░░░░░░ 30%

████████████░░░░░░░░ 60%

████████████████████ 100%
```

---

# 🎯 What This Module Prepares Me For

After completing Prefix Sum, I will be comfortable with:

- Efficient Range Queries
- Running Sum Problems
- Prefix + HashMap Pattern
- Subarray Problems
- Frequency-based Problems

Next Module:

➡️ **Module 3 — Two Pointers**

---

## 🚀 Final Takeaway

> **"Prefix Sum teaches you to preprocess once and answer many times. The real skill is recognizing when cumulative information can replace repeated work."**