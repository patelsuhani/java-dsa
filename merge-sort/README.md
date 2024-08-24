# Merge Sort Algorithm

**Merge Sort** is a divide-and-conquer algorithm that was invented by John von Neumann in 1945. It works by recursively splitting the array into smaller subarrays until each subarray contains a single element (which is inherently sorted). Then, these subarrays are merged back together in sorted order.

### How Merge Sort Works:

1. **Divide:**
   - The array is recursively divided into two halves until each subarray contains only one element.
   - This division continues until the base case is reached, where the subarray has a length of 1.

2. **Conquer:**
   - Once the array is divided into individual elements, the algorithm begins merging these elements back together.
   - During the merge process, the elements from the two halves are compared, and the smaller element is added to the merged array.
   - This process continues until all elements from both halves are merged back into a single sorted array.

### Example:

Consider the following example with an array: `[38, 27, 43, 3, 9, 82, 10]`.

- **Step 1: Divide**
  - Split the array into two halves: `[38, 27, 43]` and `[3, 9, 82, 10]`.
  - Continue dividing each half:
    - `[38, 27, 43]` → `[38]` and `[27, 43]` → `[27]` and `[43]`
    - `[3, 9, 82, 10]` → `[3, 9]` and `[82, 10]` → `[3]` and `[9]`, `[82]` and `[10]`

- **Step 2: Conquer (Merge)**
  - Merge the individual elements back together:
    - Merge `[27]` and `[43]` → `[27, 43]`
    - Merge `[38]` and `[27, 43]` → `[27, 38, 43]`
    - Merge `[3]` and `[9]` → `[3, 9]`
    - Merge `[82]` and `[10]` → `[10, 82]`
    - Merge `[3, 9]` and `[10, 82]` → `[3, 9, 10, 82]`
  - Finally, merge the two sorted halves `[27, 38, 43]` and `[3, 9, 10, 82]`:
    - `[27, 38, 43]` and `[3, 9, 10, 82]` → `[3, 9, 10, 27, 38, 43, 82]`

The array is now fully sorted: `[3, 9, 10, 27, 38, 43, 82]`.