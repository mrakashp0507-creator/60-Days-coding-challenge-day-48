
# Day 48 - Edit Distance

## Problem
Find the minimum number of operations required to
transform one string into another.

## Allowed Operations
1. Insertion - Add a character.
2. Deletion - Remove a character.
3. Replacement - Change a character.

Each operation costs 1.

## Algorithms
- Recursive approach
- Dynamic Programming approach

## DP Formula

If characters match:

dp[i][j] = dp[i-1][j-1]

Otherwise:

dp[i][j] = 1 + min(
    dp[i][j-1],    # Insert
    dp[i-1][j],    # Delete
    dp[i-1][j-1]   # Replace
)

## Example

Input:
word1 = "horse"
word2 = "ros"

Output:
3

## Complexity

| Approach | Time | Space |
|---|---|---|
| Recursion | Exponential | O(m+n) |
| Dynamic Programming | O(m*n) | O(m*n) |

## Real-World Applications
- Autocorrect
- Spell checking
- DNA sequence comparison
- Natural Language Processing

## How to Run

python day48_edit_distance.py
