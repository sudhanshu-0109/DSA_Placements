# 📅 Day 4 — Prefix Sum (Final Learning Day)

> **Status:** ✅ Completed
> **Duration:** ~1 Session
> **Focus:** LC1590 + Completing the Prefix Sum Pattern

---

# 🎯 Goal

Complete the Prefix Sum module by solving its final and most challenging pattern problem.

---

# ✅ Problem Completed

- ✅ LC1590 — Make Sum Divisible by P

---

# 🧠 Concepts Learned

## Problem Understanding

Given an array `nums` and an integer `p`, remove the **smallest** subarray such that the remaining array sum becomes divisible by `p`.

---

## Step 1

Calculate the total sum.

```java
total = sum(nums)
```

Compute

```java
rem = total % p
```

If

```java
rem == 0
```

return

```java
0
```

because the array is already divisible by `p`.

---

## Step 2

Suppose the removed subarray has sum `x`.

The remaining sum becomes

```
total - x
```

We require

```
(total - x) % p == 0
```

which means

```
x % p == total % p
```

Therefore, we need a subarray whose remainder equals

```
rem
```

---

## Step 3 — Prefix Sum

Maintain

```java
prefix = (prefix + nums[i]) % p;
```

instead of the actual prefix sum.

This avoids overflow and directly gives the remainder.

---

## Step 4 — Mathematical Derivation

Subarray Sum

```
CurrentPrefix - PreviousPrefix
```

Need

```
(CurrentPrefix - PreviousPrefix) % p == rem
```

Rearranging,

```
PreviousPrefix = (CurrentPrefix - rem + p) % p
```

This gives

```java
long target = (prefix - rem + p) % p;
```

which becomes the lookup key inside the HashMap.

---

## Step 5 — HashMap

Store

```
Prefix Remainder → Latest Index
```

Reason:

We need the **minimum** removable subarray.

Keeping the latest occurrence minimizes

```
currentIndex - previousIndex
```

---

# 💡 Biggest Realizations

### Prefix Sum is not always the actual sum.

Sometimes it stores

- Running Sum
- Running Odd Count
- Prefix Modulo

depending on the problem.

---

### The HashMap value depends entirely on the question.

| Requirement | Store |
|-------------|-------|
| Count | Frequency |
| Existence | First Index |
| Longest | First Index |
| Minimum Length | Latest Index |

---

### Every Prefix Sum problem follows the same workflow.

```
Brute Force

↓

Prefix Sum

↓

Observation

↓

HashMap

↓

Optimal Solution
```

---

# 📚 Prefix Sum Pattern Summary

## LC560

```
Prefix Sum → Frequency
```

Need

```
CurrentPrefix - PreviousPrefix = K
```

---

## LC523

```
Remainder → First Index
```

Need

```
CurrentRemainder == PreviousRemainder
```

---

## LC974

```
Remainder → Frequency
```

Need

```
CurrentRemainder == PreviousRemainder
```

---

## LC1248

```
Odd Count → Frequency
```

Need

```
CurrentOddCount - PreviousOddCount = K
```

---

## LC1590

```
Remainder → Latest Index
```

Need

```
(CurrentPrefix - PreviousPrefix) % p = rem
```

Lookup

```
(CurrentPrefix - rem + p) % p
```

---

# ⚠️ Mistakes Avoided

- ✅ Remembered to return `0` when `total % p == 0`.
- ✅ Used modulo prefix instead of storing the full prefix sum.
- ✅ Understood why `+p` is required before taking `% p`.
- ✅ Learned why the latest index is stored instead of the first.
- ✅ Recognized that Sliding Window cannot solve this problem because modulo does not behave monotonically.

---

# 📝 Final Accepted Solution

```java
class Solution {
    public int minSubarray(int[] nums, int p) {

        long total = 0;

        for (int n : nums)
            total += n;

        long rem = total % p;

        if (rem == 0)
            return 0;

        long prefix = 0;

        Map<Long, Integer> map = new HashMap<>();
        map.put(0L, -1);

        int ans = nums.length;

        for (int i = 0; i < nums.length; i++) {

            prefix = (prefix + nums[i]) % p;

            long target = (prefix - rem + p) % p;

            if (map.containsKey(target))
                ans = Math.min(ans, i - map.get(target));

            map.put(prefix, i);
        }

        return ans == nums.length ? -1 : ans;
    }
}
```

---

# 📈 Prefix Sum Module Status

```
████████████████████ 100%
```

## Problems Solved

### Easy

- ✅ LC1480
- ✅ LC303
- ✅ LC724
- ✅ LC1732
- ✅ LC2574

### Medium

- ✅ LC560
- ✅ LC523
- ✅ LC974
- ✅ LC1248
- ✅ LC1590

---

# 🎯 Next Two Days

No new pattern.

Focus only on strengthening the first two modules.

### Revision Plan

#### Day 5

- Blind solve Traversal questions.
- Blind solve Prefix Sum questions.
- Complete `Traversals.md`.
- Complete `PrefixSum.md`.

#### Day 6

Mixed Pattern Practice.

Goal:

Before writing any code, identify

- Pattern
- Reason
- Data Structure
- Time Complexity

Only then start coding.

---

# 💬 Mentor's Remarks

This was one of the most satisfying modules to teach.

At the beginning of Prefix Sum, you were learning **what** Prefix Sum is.

By the end, you were asking a completely different question:

> "Can I transform this problem into a pattern I've already solved?"

That shift is exactly what experienced problem solvers do.

The biggest moment for me wasn't when you solved LC1590—it was when you independently recognized that LC1248 was simply LC560 after changing the meaning of the Prefix Sum. That showed you were no longer memorizing solutions; you were identifying reusable patterns.

Even in LC1590, you didn't wait for the formula. You derived:

```
(CurrentPrefix - rem + p) % p
```

on your own after understanding the mathematics. That's a significant step forward.

Over these four days, you didn't just complete a module—you built a framework for approaching problems.

Moving into Two Pointers after two days of revision is the right decision. A strong foundation in Traversals and Prefix Sum will make every upcoming pattern easier to recognize and connect.

Keep this mindset:

> **Don't collect problems. Collect patterns.**

That's how great DSA preparation is built.

---

# 🏁 Day 4 Takeaway

> "A Prefix Sum is not just a running sum—it is accumulated information. Once I understand what information needs to be accumulated and what the HashMap should store, the algorithm almost derives itself."