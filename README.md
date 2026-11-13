# CE101 Homework - LeetCode 121: Best Time to Buy and Sell Stock

**Course:** CE101 - Algorithms and Computer Programming I  
**Student:** Beril Su Güneş (260170117)  
**Problem Link:** [LeetCode 121 - Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)

## Problem Description
Given an array `prices` where `prices[i]` is the price of a stock on day `i`, the goal is to find the maximum profit we can achieve by buying on one day and selling on a later day. We cannot sell a stock before buying it. If no profitable transaction is possible, the function returns `0`.

## Compilation and Execution (GCC / C99)
All C programs in this repository are compiled using GCC in C99 mode. You can compile and run them from the terminal using the commands below:

```bash
# Compile and run the original starter code
gcc -std=c99 -Wall -Wextra original.c -o original
./original

# Compile and run the time-optimized code
gcc -std=c99 -Wall -Wextra optimized_time.c -o optimized_time
./optimized_time

# Compile and run the space-optimized code
gcc -std=c99 -Wall -Wextra optimized_space.c -o optimized_space
./optimized_space
```
*(Note: On Windows terminals, run `original.exe`, `optimized_time.exe`, or `optimized_space.exe` instead of `./`)*

## Test Cases Used
Each program is tested with the two starter arrays and two additional test cases (including a single-element edge case):

1. `prices1 = {7, 1, 5, 3, 6, 4}` → **Expected & Actual Output:** `5` (Buy at `1`, sell at `6`)
2. `prices2 = {7, 6, 4, 3, 1}` → **Expected & Actual Output:** `0` (Prices decrease every day, no profit)
3. `prices3 = {5}` *(Edge Case)* → **Expected & Actual Output:** `0` (Only one day, cannot buy and sell)
4. `prices4 = {1, 2, 3, 4, 5}` → **Expected & Actual Output:** `4` (Buy at `1`, sell at `5`)

## Repository File Inventory
* `original.c` — Starter baseline solution using nested loops ($O(n^2)$ time) and an auxiliary array ($O(n)$ space).
* `optimized_time.c` — Improved single-pass solution tracking the running minimum price ($O(n)$ time, $O(1)$ auxiliary space).
* `optimized_space.c` — Space-optimized solution removing the extra `bestForBuy` array ($O(n)$ time, $O(1)$ auxiliary space; identical implementation to `optimized_time.c`).
* `report.pdf` — Written report answering Questions 1–5, including trace tables, complexity comparisons, and AI-use disclosure.
* `screenshots/` — Terminal screenshots showing compilation and test outputs (`test_original.png` and `extra_tests.png`).
* `README.md` — Overview of the repository, build instructions, and test summary.