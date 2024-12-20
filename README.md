# Implement_Some_Algorithms

## 1. Heap Sort Time Complexity Analysis

### `max_heapify`

- **Time Complexity**: `O(log n)` (worst case).


### `build_max_heap`
- Builds a max-heap from an unordered array.
- Calls `max_heapify` on all non-leaf nodes in reverse order.
- Total cost is the sum of costs across all levels of the heap:

  \[
  T(n) = \sum_{h=0}^{\lfloor \log n \rfloor} \frac{n}{2^{h+1}} \cdot h = O(n)
  \]

- **Time Complexity**: `O(n)`.



### `heap_sort`
- **Step 1**: Build a max-heap (time: `O(n)`).
- **Step 2**: Repeatedly extract the maximum element and call `max_heapify`:

  - `n-1` calls to `max_heapify`.
  - Each call takes `O(log n)` time.
  - Total cost: \((n-1) \cdot O(\log n) = O(n \log n)\).

- **Time Complexity**: `O(n \log n)`.



### Overall Time Complexity
The total time complexity of Heap Sort is:

\[
O(n) + O(n \log n) = O(n \log n)
\]

---

