# leet-day11

# Add Binary Strings - LeetCode Problem

## Problem Description

Given two binary strings `a` and `b`, you need to return their sum as a binary string.

A binary string is a string consisting of only '0' and '1' characters.

## Examples

Example 1:

```
Input: a = "11", b = "1"
Output: "100"
```

Example 2:

```
Input: a = "1010", b = "1011"
Output: "10101"
```

## Constraints

- 1 <= a.length, b.length <= 10^4
- `a` and `b` consist only of '0' and '1' characters.
- Each string does not contain leading zeros except for the zero itself.

## Approach and Code

We can solve this problem by simulating the addition process of two binary strings. We iterate over the strings from right to left, adding the corresponding digits along with the carry. We keep track of the sum modulo 2 and the carry, and append the result to the result string. We handle cases where the two binary strings have different lengths and ensure that there are no leading zeros in the final result.


## Complexity Analysis

The time complexity of the `addBinary` function is O(max(n, m)), where n and m are the lengths of strings `a` and `b`, respectively. The space complexity is also O(max(n, m)) to store the result.

This solution passes all the test cases provided by LeetCode.
