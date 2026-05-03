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



## Problem 2.3: Thinking outside the Box


### Box Packing
We will take 2x2x2 boxes of black and white each. We got this 2 from gcd(4,6)
total boxes = 27. 14 red and 13 blue. Total blue cells = 13*8 
each brick will use 2 red and 2 blue cells
max bricks possible = 13*8/2 = 52. 53 impossible


### Calender Cubes

die1 0 1 2 3 4 5
die2 0 1 2 6 7 8

(6 can be used as a 9 crazy)

### Door to offer
I couldnt think of this one this was pretty hard
ask "will the other guard say that you are guarding the offer door"

### Light Switches
The bulb hot cold and just 1 try is a crazy stratergy

### Quant Salary
Cool to add a random number and then subtract. This wont work for 2 people though 


## Problem 2.4: Symmetry
### Coin piles
Choos 20 and flip them!

### Mislabeled Bags
1 fruit from the mixed bag. if it is apple, then the orange one has to be mixed, and the apple one is orange

### Wise men
so basically, we need that only 1 person should be the one who says the answer

so, 49 others will flip the first time they see the glass straight, otherwise not.

the last one will flip when he sees glass upside down

after 49 flips of the last one, he can say that yes all others have come atleast once


## Problem 2.5: Series Summation

### Clock Pieces

Sum of each piece = (12*13)/(2*3) = 26

11,12,1,2 = could be one piece
5,6,7,8  =  could be one piece
3,4,9,10 = could be one piece (this is not continous but a piece)

### Counterfeit coins I

I first understood the problem that the scammy bag can have 11 AND 9 coins both, which would make this problem a bit more difficult

So, I choose the stratergy to choose odd number of coins from each 

1, 3, 5, 7, 9, 11, 13, 15, 17, 19

and then depending on the sum form a linear diophantine equation to calculate 9s and 11s

### Glass Balls 
Binary Search? == Not really too many drops there
we want that all our cases should be the same, because if theyre not then the adversarial will always choose the worst case

toh we will try our ball from a floor
if it breaks then we will throw from 1 to floor-1

if it works then we will go to 2*floor-1 and do the same

we will fic the number of throws that we will make


## Problem 2.6: PigeonHole

### Handshakes

26 people, and a person can do max 25 handshakes
There must be 2 with same number

### Have we met before?

6 people
all strangers = second true
2 met each other = second true
3 met each other and above = first true

atleast 3 people met each other before
or atleast 3 people were strangers before 

all cases fixed!

### Counterfeit coins II

2x1 + 3x2 + 13x3 + 7x4 + 17x5 == thinking of something like this

So I got the weighing part since we can easily solve a diophantine equation we would need just 1 weighing

but now we also need the number of coins from each bag needed

9,10,11

9/10/11 bag 1

9/10/11 bag 2

we can convert to base 3

3^0, 3^1, 3^2, 3^3, 3^4 as coefficients can be used

This is because this will always lead to unique combinations, just like using base 10 and all that

We are using a base-3 bitmask, hence the coefficients are 3^0, 3^1, 3^2 ,3^3 and 3^4

think of it in this way, what is the max number we can reach with 1 coin = 2

next coin sum we need = 3

hence, the next multipler adder that we need from second coin = 3

like this. max that can we make = 3*2 + 2 = 8

next needed = 9. Next multiplier = 9


## Problem 2.7: Modular Artithmatic


### Prisoner Problem

Red or blue hat
hats assigned = cant communicate
guess color of his hat

55, 44 ===== (56, 44) or (55, 45) initially both possible

red, blue === 1st     prisoner

initially = both odd or both even



odd, odd = odd even
even , even = odd , evemn 

odd red, even blue ===== maybe he says red



Solution = he will announce odd number of hats color. The others who see the saeme odd one willl get to know their color as same as him, and those who dont will get to know thier color opposite of him


### Chameleon colors

I did this with a mathematical proof and arrived at a contradiction

## Problem 2.7: Math Induction

### Coin split
simple induction n(n-1)/2 ans

### Chocolate bar
Simple induction n*m-1

### Race track one
induction. combine the point having gas more than the distance to the next point with the enxt point, and it becomes an n problem !!!

### Rainbow Hats

The sum of colors of each prsioner % 7 has to be one of 0,1,2,3,4,5,6

So, each prisoner will try to guess the sum between 0 to 6, atleast one of them will match. He will give the guess so that his guess + other numbers sum mod 7 becomes i

koi na koi ek toh sahi hoga hi



