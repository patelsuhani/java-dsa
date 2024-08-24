## Insertion Sort Algorithm

**Insertion Sort** is a simple and efficient comparison-based sorting algorithm suitable for small datasets and nearly sorted data. It builds the final sorted array one element at a time by repeatedly inserting the next element into the correct position within the sorted portion of the array.

### How Insertion Sort Works

The algorithm divides the input array into two parts:
- **Sorted Subarray:** Initially contains the first element of the array.
- **Unsorted Subarray:** Contains the rest of the elements.

The algorithm proceeds by picking each element from the unsorted subarray and inserting it into the correct position in the sorted subarray.

**Step-by-step process:**
1. **Start with the second element** (index 1) of the array; consider the first element (index 0) as already sorted.
2. **Compare the current element** with the elements in the sorted subarray:
   - Shift all elements in the sorted subarray that are greater than the current element to the right by one position.
3. **Insert the current element** into its correct position within the sorted subarray.
4. **Move to the next element** in the unsorted subarray and repeat the process until the entire array is sorted.