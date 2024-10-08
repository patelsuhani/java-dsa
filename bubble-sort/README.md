# Bubble Sort Algorithm

**Bubble Sort** is a simple comparison-based sorting algorithm. It repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order. The pass through the list is repeated until the list is sorted.

### How Bubble Sort Works:

1. **Initial Pass:**
   - Start from the beginning of the array.
   - Compare the first two adjacent elements. If the first element is greater than the second, swap them.
   - Move to the next pair of adjacent elements (second and third) and repeat the comparison and swap if necessary.
   - Continue this process until you reach the end of the array. After the first pass, the largest element will be in its correct position (at the end of the array).

2. **Subsequent Passes:**
   - Repeat the process for the rest of the array, excluding the last sorted element.
   - After each pass, the next largest element will be placed in its correct position.
   - Continue until no swaps are needed, indicating that the array is sorted.

### Example:

Consider the following example with an array: `[5, 2, 9, 1, 5, 6]`.

- **Pass 1:**
  - Compare `5` and `2`: Swap → `[2, 5, 9, 1, 5, 6]`
  - Compare `5` and `9`: No swap → `[2, 5, 9, 1, 5, 6]`
  - Compare `9` and `1`: Swap → `[2, 5, 1, 9, 5, 6]`
  - Compare `9` and `5`: Swap → `[2, 5, 1, 5, 9, 6]`
  - Compare `9` and `6`: Swap → `[2, 5, 1, 5, 6, 9]`

  The largest element `9` is now at the end of the array.

- **Pass 2:**
  - Compare `2` and `5`: No swap → `[2, 5, 1, 5, 6, 9]`
  - Compare `5` and `1`: Swap → `[2, 1, 5, 5, 6, 9]`
  - Compare `5` and `5`: No swap → `[2, 1, 5, 5, 6, 9]`
  - Compare `5` and `6`: No swap → `[2, 1, 5, 5, 6, 9]`

  The second-largest element `6` is now in its correct position.

- **Pass 3:**
  - Compare `2` and `1`: Swap → `[1, 2, 5, 5, 6, 9]`
  - Compare `2` and `5`: No swap → `[1, 2, 5, 5, 6, 9]`
  - Compare `5` and `5`: No swap → `[1, 2, 5, 5, 6, 9]`

  The third-largest element `5` is now in its correct position.

- **Pass 4:**
  - Compare `1` and `2`: No swap → `[1, 2, 5, 5, 6, 9]`
  - Compare `2` and `5`: No swap → `[1, 2, 5, 5, 6, 9]`

  The fourth-largest element `5` is now in its correct position.

- **Pass 5:**
  - Compare `1` and `2`: No swap → `[1, 2, 5, 5, 6, 9]`

  The array is now fully sorted.

### Time Complexity

The time complexity of Bubble Sort depends on the number of comparisons and swaps made:

- **Best Case:** If the array is already sorted, Bubble Sort still makes one complete pass without any swaps. The best-case time complexity is `O(n)`.
- **Worst Case:** If the array is sorted in reverse order, Bubble Sort must perform the maximum number of comparisons and swaps. The worst-case time complexity is `O(n^2)`.
- **Average Case:** On average, Bubble Sort will perform \(\frac{n(n-1)}{2}\) comparisons, leading to an average time complexity of `O(n^2)`.

### Space Complexity

Bubble Sort is an in-place sorting algorithm, meaning it requires only a constant amount of extra space:

- **Space Complexity:** `O(1)` because it only requires a single additional variable for swapping, regardless of the size of the input array.
