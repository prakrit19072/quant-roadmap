# Green Book

## Problem 2.1: Problem Simplification

### Pirate Game
<details>
<summary><b>View Distribution Logic (2-5 Pirates)</b></summary>

| Pirates | Distribution | Logic |
| :--- | :--- | :--- |
| **2** | `(100, 0)` | Senior takes all; Junior has no leverage. |
| **3** | `(99, 0, 1)` | P3 gets 1 coin; better than the 0 they'd get with 2 pirates. |
| **4** | `(99, 0, 1, 0)` | P3 was getting 0 earlier; 1 coin secures their vote. |
| **5** | `(98, 0, 1, 0, 1)`| P3 and P5 are the cheapest votes to buy (both were at 0). |

</details>

### Tiger and Sheep
> [!TIP]
> **The Intuition:** It is a recursive fear check. If eating the sheep turns you into a sheep for the next tiger, you stay hungry.
* **Odd Tigers:** Sheep is eaten.
* **Even Tigers:** Sheep survives.

---

## Problem 2.2: Logical Reasoning

### River Crossing
**Goal:** 17 Minutes
* **Step 1:** C and D cross (2m), D returns (1m) -> **3m**
* **Step 2:** A and B cross (10m), C returns (2m) -> **12m**
* **Step 3:** C and D cross (2m) -> **2m**
* **Total:** $2 + 1 + 10 + 2 + 2 = 17$ min.

### Birthday Problem
<details>
<summary><b>Elimination Path</b></summary>

1. **Statement 1:** Eliminates June/December (Day must be unique if the month was known).
2. **Statement 2:** Eliminates March 5 and Sept 5.
3. **Statement 3:** Eliminates March entirely.
**Result:** **September 1**
</details>

### Card Game
> **Outcome:** $0.
> **Intuition:** Since it is a closed system of red/black cards being swapped, the number of misplaced reds must exactly equal the number of misplaced blacks to keep the pile sizes constant.

### Burning Ropes (45 Minutes)
1. **Rope 1:** Light **both** ends. (Burn time: 30m)
2. **Rope 2:** Light **one** end at the same time.
3. **Action:** When Rope 1 vanishes (30m mark), light the **other** end of Rope 2.
4. **Result:** The remaining 30m of Rope 2 burns in 15m. Total = 45m.

### Defective Ball (12 Balls)
<details>
<summary><b>The 3-Weighting Strategy</b></summary>

**Step 1:** Group into 4-4-4. Weigh `[1,2,3,4]` vs `[5,6,7,8]`.
* **If Balanced:** Faulty is in `[9,10,11,12]`. Compare three "good" balls against three "suspect" balls.
* **If Unbalanced:** Use the **Substitution Method**.
  * Swap one heavy for one light, and replace one light with a known good ball.
  * *Intuition:* If the scale tips the other way, the "swapped" balls contain the culprit. If it balances, the "removed" ball was the culprit.
</details>

### Horse Race
**The 7-Race Solution:**
1. **Races 1-5:** Find the top 3 of each group.
2. **Race 6:** Race the 5 winners. (Identifies the #1 overall Horse).
3. **Race 7:** The "Final Sprint." Race the 2nd and 3rd from the Winner's group, the 1st and 2nd from the 2nd place group, and the 1st from the 3rd place group.

---

