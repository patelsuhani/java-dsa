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

### Example

Let's walk through an example to illustrate how Insertion Sort works.

**Given array:** `[12, 11, 13, 5, 6]`

**Initial state:**
- Sorted Subarray: `[12]`
- Unsorted Subarray: `[11, 13, 5, 6]`

**Detailed steps:**

#### **Pass 1:** (Current Element = 11)

- **Initial array:** `[12, 11, 13, 5, 6]`
- Compare `11` with `12`:
  - Since `11` < `12`, shift `12` to the right.
- **Array after shifting:** `[12, 12, 13, 5, 6]`
- Insert `11` at position 0.
- **Array after insertion:** `[11, 12, 13, 5, 6]`

**Result after Pass 1:** `[11, 12, 13, 5, 6]`

#### **Pass 2:** (Current Element = 13)

- **Initial array:** `[11, 12, 13, 5, 6]`
- Compare `13` with `12`:
  - Since `13` >= `12`, no shifting is needed.
- Insert `13` at its current position.
- **Array remains unchanged:** `[11, 12, 13, 5, 6]`

**Result after Pass 2:** `[11, 12, 13, 5, 6]`

#### **Pass 3:** (Current Element = 5)

- **Initial array:** `[11, 12, 13, 5, 6]`
- Compare `5` with `13`:
  - Since `5` < `13`, shift `13` to the right.
- **Array after shifting:** `[11, 12, 13, 13, 6]`
- Compare `5` with `12`:
  - Since `5` < `12`, shift `12` to the right.
- **Array after shifting:** `[11, 12, 12, 13, 6]`
- Compare `5` with `11`:
  - Since `5` < `11`, shift `11` to the right.
- **Array after shifting:** `[11, 11, 12, 13, 6]`
- Insert `5` at position 0.
- **Array after insertion:** `[5, 11, 12, 13, 6]`

**Result after Pass 3:** `[5, 11, 12, 13, 6]`

#### **Pass 4:** (Current Element = 6)

- **Initial array:** `[5, 11, 12, 13, 6]`
- Compare `6` with `13`:
  - Since `6` < `13`, shift `13` to the right.
- **Array after shifting:** `[5, 11, 12, 13, 13]`
- Compare `6` with `12`:
  - Since `6` < `12`, shift `12` to the right.
- **Array after shifting:** `[5, 11, 12, 12, 13]`
- Compare `6` with `11`:
  - Since `6` < `11`, shift `11` to the right.
- **Array after shifting:** `[5, 11, 11, 12, 13]`
- Compare `6` with `5`:
  - Since `6` >= `5`, insert `6` at position 1.
- **Array after insertion:** `[5, 6, 11, 12, 13]`

**Result after Pass 4:** `[5, 6, 11, 12, 13]`

**Final sorted array:** `[5, 6, 11, 12, 13]`