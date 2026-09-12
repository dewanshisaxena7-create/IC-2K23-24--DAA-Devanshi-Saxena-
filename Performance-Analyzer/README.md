# DAA Algorithm Performance Analyzer

## 1. Problem Statement

Develop an Algorithm Performance Analyzer to compare the theoretical and experimental performance of Iterative and Recursive Binary Search algorithms.

The objective of this project is to measure the execution time of both implementations for different input sizes, store the experimental results, and visualize their performance using graphs.

---

## 2. Algorithms Implemented

The following algorithms are implemented and analyzed:

### Iterative Binary Search

Iterative Binary Search repeatedly divides a sorted array into two halves using a loop until the target element is found or the search range becomes empty.

### Recursive Binary Search

Recursive Binary Search performs the same search operation by recursively dividing the search range into two halves.

---

## 3. Theoretical Complexity Analysis

| Algorithm | Best Case | Average Case | Worst Case | Space Complexity |
|-----------|-----------|--------------|------------|------------------|
| Iterative Binary Search | O(1) | O(log n) | O(log n) | O(1) |
| Recursive Binary Search | O(1) | O(log n) | O(log n) | O(log n) |

Both algorithms have logarithmic time complexity because the search space is reduced by half during each step.

---

## 4. Experimental Analysis

The performance of Iterative and Recursive Binary Search was experimentally analyzed by measuring their execution time for different input sizes.

The experimental results were recorded and stored in a CSV file.

### Experimental Results File

```text
results.csv
