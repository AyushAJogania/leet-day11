# leet-day11

# Peak Index in a Mountain Array

You are given an array `arr` that represents a mountain array. A mountain array is defined as an array where there exists an index `i` such that `arr[0] < arr[1] < ... < arr[i - 1] < arr[i] > arr[i + 1] > ... > arr[arr.length - 1]`.

You need to find the peak index `i`, where the array is strictly increasing up to index `i` and strictly decreasing from index `i` onwards.

## Example

### Input
```cpp
arr = [0, 2, 1, 0]
```

### Output
```cpp
1
```

### Explanation
The peak index in the mountain array is 1 since `arr[1]` is the peak element, and `arr[0] < arr[1] > arr[2] > arr[3]`.

## Constraints

- `3 <= arr.length <= 10^5`
- `0 <= arr[i] <= 10^6`
- The array `arr` is guaranteed to be a mountain array.

## Approach and Complexity

We can use a binary search-based approach to find the peak index in the mountain array. The binary search algorithm looks at the middle element (`mid`) of the array and compares it with its right neighbor (`arr[mid + 1]`). If `arr[mid]` is less than `arr[mid + 1]`, it means the peak is on the right side, so we update the left pointer `low = mid + 1`. Otherwise, the peak is on the left side or is the element `mid` itself, so we update the right pointer `high = mid`.

We continue this process until `low` and `high` pointers are not equal. When the loop ends, both `low` and `high` will point to the peak index, and we can return either `low` or `high`.

The time complexity of this approach is O(log n), where n is the length of the input array `arr`. The binary search algorithm reduces the search space by half in each iteration, making it very efficient. The space complexity is O(1) as we are using only a constant amount of extra space.
