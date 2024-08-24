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
