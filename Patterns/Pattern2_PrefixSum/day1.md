# 📘 Module 2: Prefix Sum

> **Status:** 🚀 In Progress  
> **Progress:** **65% Complete**  
> **Planned Duration:** 4 Days *(Updated)*  
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

| Day | Topics | Status |
|------|--------|--------|
| **Day 1** | Prefix Sum Theory + LC 1480 + LC 303 + LC 724 + LC 1732 + LC 2574 + LC 560 | ✅ Completed |
| **Day 2** | LC 523 + LC 525 + LC 930 | ⏳ |
| **Day 3** | LC 974 + LC 1248 + LC 1590 | ⏳ |
| **Day 4** | Revision + Re-solving Important Questions | ⏳ |

---

# 📚 Theory Checklist

## Prefix Sum Basics

- [x] What is Prefix Sum?
- [x] Why Prefix Sum?
- [x] Prefix Array Construction
- [x] In-place Prefix Sum
- [x] Range Sum Query
- [x] Prefix Sum Formula
- [x] Time Complexity
- [x] Space Complexity

---

## Prefix Sum + HashMap

- [x] Why HashMap is Required
- [x] Prefix Sum Frequency
- [x] Counting Subarrays
- [x] Running Prefix Sum
- [x] Handling Negative Numbers

---

# 🟢 Easy Problems

- [x] LC 1480 — Running Sum of 1D Array
- [x] LC 303 — Range Sum Query - Immutable
- [x] LC 724 — Find Pivot Index
- [x] LC 1732 — Find the Highest Altitude
- [x] LC 2574 — Left and Right Sum Differences

---

# 🟡 Medium Problems

- [x] LC 560 — Subarray Sum Equals K ⭐⭐⭐⭐⭐
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

✔ Prefix Array Construction

✔ In-place Prefix Sum

✔ Range Sum Query

✔ Left Sum & Right Sum Technique

✔ Prefix Sum without Prefix Array

✔ O(1) Range Query

---

## Prefix Sum + HashMap

✔ Running Prefix Sum

✔ Frequency Counting

✔ Prefix Sum Frequency

✔ Subarray Counting

✔ Prefix Difference

✔ Handling Negative Numbers

✔ Fast Lookup

✔ O(n) Optimization

---

# 🧠 Important Observations

- Prefix Sum stores cumulative information instead of recalculating sums.
- Range Sum Queries become **O(1)** after preprocessing.
- Prefix Sum alone solves many Easy problems.
- Prefix Sum + HashMap is one of the most common interview patterns.
- Many subarray problems become simple once Prefix Sum is recognized.
- Always think about cumulative information before using nested loops.
- **Current element is neither part of Left Sum nor Right Sum.**
- **PrefixSum - PreviousPrefixSum = K** is the key equation behind LC560.
- Store **Prefix Sum frequencies**, not indices.
- Always initialize:

```java
map.put(0,1);
```

- Always check the HashMap **before** inserting the current Prefix Sum.

---

# ⚠️ Common Mistakes

- [x] Included current element in Left Sum (Corrected)
- [x] Tried using `break` in LC560 (Incorrect)
- [ ] Forgetting the Range Sum Formula
- [ ] Forgetting `map.put(0,1)`
- [ ] Updating HashMap before checking
- [ ] Off-by-one errors
- [ ] Confusing Prefix Sum with Sliding Window

---

# 🔁 Revision Checklist

Without looking at previous solutions:

## Theory

- [x] Explain Prefix Sum.
- [x] Explain Range Sum Query.
- [x] Explain Prefix + HashMap.

---

## Coding

- [x] Build Prefix Array
- [x] LC 1480
- [x] LC 303
- [x] LC 724
- [x] LC 1732
- [x] LC 2574
- [x] LC 560
- [ ] LC 523
- [ ] LC 525
- [ ] LC 930
- [ ] LC 974

---

## Understanding

- [x] Can identify Prefix Sum problems quickly.
- [x] Know when Prefix Sum alone is enough.
- [x] Know when HashMap is required.
- [x] Can derive the Prefix + HashMap formula.

---

# 📝 Notes

## Pattern

**Prefix Sum**

---

## Core Idea

Store cumulative information to avoid repeated calculations.

---

## Prefix Array Formula

```text
prefix[i] = prefix[i-1] + arr[i]
```

---

## Running Prefix Sum

```text
sum += nums[i]
```

---

## Range Sum Formula

```text
If L == 0

sum = prefix[R]

Else

sum = prefix[R] - prefix[L-1]
```

---

## Left & Right Sum Formula

```text
rightSum = totalSum - leftSum - nums[i]
```

---

## Prefix + HashMap Formula

```text
CurrentPrefix - PreviousPrefix = K

PreviousPrefix = CurrentPrefix - K
```

---

## HashMap Stores

```text
Prefix Sum → Frequency
```

Example

```text
0 → 1
1 → 2
3 → 1
7 → 1
```

---

## Why map.put(0,1)?

Because the empty Prefix Sum exists before the array starts.

This allows subarrays beginning from index **0** to be counted.

---

## Why answer += map.get(sum-k)?

Multiple previous Prefix Sums may satisfy the condition.

Each occurrence forms a different valid subarray.

---

## Why check before inserting?

The HashMap should only contain Prefix Sums that occurred **before** the current index.

Otherwise, we may incorrectly count the current Prefix Sum itself.

---

## When to Use Prefix Sum

- Range Sum Query
- Running Sum
- Left vs Right Sum
- Prefix + HashMap
- Frequency Counting
- Subarray Problems

---

# ⏱ Time Complexity

| Operation | Complexity |
|------------|------------|
| Build Prefix Array | O(n) |
| Range Query | O(1) |
| Prefix + HashMap | O(n) |

---

# 💾 Space Complexity

| Method | Complexity |
|----------|------------|
| Prefix Array | O(n) |
| In-place Prefix | O(1) |
| Prefix + HashMap | O(n) |

---

# 🏁 Module Completion Criteria

- [x] Understand Prefix Sum.
- [x] Understand Prefix + HashMap.
- [x] Complete all Easy Problems.
- [x] Solve LC560 without hints.
- [ ] Complete all Medium Problems.
- [ ] Complete Revision Day.
- [ ] Ready for Two Pointers.

---

# 📊 Progress

```text
█████████████░░░░░░░ 65%

Completed
────────────
✅ Prefix Sum Basics
✅ All Easy Problems
✅ Prefix Sum + HashMap
✅ LC560

Remaining
────────────
⬜ LC523
⬜ LC525
⬜ LC930
⬜ LC974
⬜ LC1248
⬜ LC1590
⬜ Revision
```

---

# 📅 Session Log

## ✅ Day 1

### Theory Covered

- Prefix Sum Fundamentals
- Prefix Array
- Running Prefix Sum
- In-place Prefix Sum
- Range Sum Query
- Left & Right Sum Technique
- Prefix Sum + HashMap

---

### Problems Solved

- ✅ LC1480 — Running Sum
- ✅ LC303 — Range Sum Query
- ✅ LC724 — Pivot Index
- ✅ LC1732 — Highest Altitude
- ✅ LC2574 — Left & Right Sum Difference
- ✅ LC560 — Subarray Sum Equals K

---

### Biggest Learnings

- Prefix Sum is a **pattern**, not just an array.
- Current element never belongs to Left Sum or Right Sum.
- `PrefixSum - PreviousPrefixSum = K` is the heart of LC560.
- HashMap stores Prefix Sum **frequencies**, not indices.
- Always check the map before inserting the current Prefix Sum.
- Brute Force helps derive the optimal solution.

---

### Mistakes Corrected

- ❌ Included current element in Left Sum.
- ❌ Tried using `break` in LC560.
- ✅ Understood why frequencies are stored instead of indices.
- ✅ Understood why `map.put(0,1)` is required.

---

### Confidence

⭐⭐⭐⭐☆ (4.5/5)

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

# 🚀 Final Takeaway

> **"Prefix Sum is not about storing sums—it's about recognizing cumulative information. Once you see `Current Prefix - Previous Prefix`, many O(n²) subarray problems collapse into elegant O(n) solutions."**




## 📅 Session Log (Continuation)

### ✅ LC523 — Continuous Subarray Sum

#### New Pattern Learned

- Prefix Sum + Modulo (Remainder)
- Equal Remainders imply a divisible subarray.
- HashMap stores **Remainder → First Occurrence Index**.
- Initialize with `map.put(0, -1)` to handle subarrays starting from index `0`.
- Store only the first occurrence of each remainder.

#### Brute Force Progression

O(n³)
→ Prefix Sum O(n²)
→ Prefix Sum + HashMap O(n)

#### Biggest Learning

The real optimization was **not** computing sums faster—it was avoiding checking every possible subarray.

#### Confidence

⭐⭐⭐⭐☆ (4/5)

> "This was the toughest Prefix Sum problem so far. I now understand *why* equal remainders work instead of simply memorizing the solution."