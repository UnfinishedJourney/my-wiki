# Complexity of Data Structures and Iterator Invalidations in C++

## Complexity Comparison

| Data Structure     | Insert (Average) | Insert (Worst) | Access (Average) | Access (Worst) | Delete (Average) | Delete (Worst) | Space Complexity |
|--------------------|------------------|----------------|------------------|----------------|------------------|----------------|------------------|
| `std::vector`      | O(1) amortized   | O(n)           | O(1)             | O(1)           | O(n)             | O(n)           | O(n)             |
| `std::deque`       | O(1) amortized   | O(n)           | O(1)             | O(1)           | O(n)             | O(n)           | O(n)             |
| `std::list`        | O(1)             | O(1)           | O(n)             | O(n)           | O(1)             | O(1)           | O(n)             |
| `std::forward_list`| O(1)             | O(1)           | O(n)             | O(n)           | O(1)             | O(1)           | O(n)             |
| `std::set`         | O(log n)         | O(log n)       | O(log n)         | O(log n)       | O(log n)         | O(log n)       | O(n)             |
| `std::unordered_set`| O(1)            | O(n)           | O(1)             | O(n)           | O(1)             | O(n)           | O(n)             |
| `std::map`         | O(log n)         | O(log n)       | O(log n)         | O(log n)       | O(log n)         | O(log n)       | O(n)             |
| `std::unordered_map`| O(1)            | O(n)           | O(1)             | O(n)           | O(1)             | O(n)           | O(n)             |

## Iterator Invalidations

| Data Structure     | Insert                   | Delete                   | Access |
|--------------------|--------------------------|--------------------------|--------|
| `std::vector`      | All after insertion point| All after deletion point | Stable |
| `std::deque`       | All after insertion point| All after deletion point | Stable |
| `std::list`        | Only the inserted element| Only the deleted element | Stable |
| `std::forward_list`| Only the inserted element| Only the deleted element | Stable |
| `std::set`         | Stable                   | Stable                   | Stable |
| `std::unordered_set`| Stable                  | Stable                   | Stable |
| `std::map`         | Stable                   | Stable                   | Stable |
| `std::unordered_map`| Stable                  | Stable                   | Stable |