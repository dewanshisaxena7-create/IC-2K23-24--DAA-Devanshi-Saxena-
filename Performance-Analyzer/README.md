# DAA Algorithm Performance Analyzer

## 1. Problem Statement

Develop an Algorithm Performance Analyzer to compare the theoretical and experimental performance of Iterative and Recursive Binary Search algorithms.

The objective is to measure the execution time of both implementations for different input sizes, store the experimental results, and visualize their performance using graphs.

---

## 2. Algorithms Implemented

The following algorithms are implemented and analyzed:

### Iterative Binary Search

Iterative Binary Search repeatedly divides a sorted array into two halves using a loop until the target element is found or the search range becomes empty.

### Recursive Binary Search

Recursive Binary Search performs the same search operation by recursively dividing the search range into two halves until the target is found or the search range becomes empty.

---

## 3. Pseudocode / Flowchart

### Iterative Binary Search Pseudocode

```text
BINARY_SEARCH_ITERATIVE(array, target)

    low = 0
    high = length(array) - 1

    WHILE low <= high

        mid = (low + high) // 2

        IF array[mid] == target
            RETURN mid

        ELSE IF array[mid] < target
            low = mid + 1

        ELSE
            high = mid - 1

    RETURN -1
```

### Recursive Binary Search Pseudocode

```text
BINARY_SEARCH_RECURSIVE(array, target, low, high)

    IF low > high
        RETURN -1

    mid = (low + high) // 2

    IF array[mid] == target
        RETURN mid

    ELSE IF array[mid] < target
        RETURN BINARY_SEARCH_RECURSIVE(array, target, mid + 1, high)

    ELSE
        RETURN BINARY_SEARCH_RECURSIVE(array, target, low, mid - 1)
```

### Flowchart

Flowcharts for both Iterative and Recursive Binary Search are included in the `PerformanceAnalyzer.ipynb` notebook.

---

## 4. Time & Space Complexity Analysis

| Algorithm | Best Case | Average Case | Worst Case | Space Complexity |
|---|---|---|---|---|
| Iterative Binary Search | O(1) | O(log n) | O(log n) | O(1) |
| Recursive Binary Search | O(1) | O(log n) | O(log n) | O(log n) |

Both algorithms have logarithmic time complexity because the search space is reduced by half during every step.

The recursive implementation requires additional stack space because of recursive function calls, while the iterative implementation uses constant auxiliary space.

---

## 5. Sample Input / Output

### Sample Input

```text
Sorted Array:
10 20 30 40 50 60 70

Target:
40
```

### Sample Output

```text
Element found at index: 3
```

If the target is not present:

```text
Target not found
```

---

## 6. Experimental Analysis

The performance of Iterative and Recursive Binary Search was experimentally analyzed by measuring their execution time for different input sizes.

The following input sizes were used:

```text
100
500
1000
5000
10000
50000
100000
500000
1000000
```

The algorithms were tested on sorted arrays, and a randomly selected existing element was used as the target.

Multiple timing trials were performed for each input size to obtain reliable execution-time measurements.

---

## 7. Experimental Results

The experimental results were stored in:

```text
results.csv
```

The CSV file contains:

```text
input_size
iterative_time_sec
recursive_time_sec
```

### Observed Results

| Input Size | Iterative Time (µs) | Recursive Time (µs) |
|---:|---:|---:|
| 100 | 0.821 | 0.889 |
| 500 | 1.103 | 1.393 |
| 1000 | 1.455 | 1.772 |
| 5000 | 1.513 | 1.812 |
| 10000 | 1.889 | 2.340 |
| 50000 | 2.318 | 2.852 |
| 100000 | 2.464 | 3.042 |
| 500000 | 2.494 | 3.056 |
| 1000000 | 2.608 | 3.269 |

The results show that the execution time increases slowly as the input size increases, which is consistent with the logarithmic time complexity of Binary Search.

The iterative implementation was slightly faster than the recursive implementation in this experiment because the recursive version has additional function-call overhead.

---

## 8. Screenshots / Graphs

The performance graph generated from the experiment is available in:

```text
performance_graph (1).png
```

The graph compares the execution time of:

- Iterative Binary Search
- Recursive Binary Search

for different input sizes.

The flowcharts and experimental analysis are also available in:

```text
PerformanceAnalyzer (1).ipynb
```

---

## 9. Learning Outcomes

Through this experiment, the following concepts were studied:

- Implementation of Iterative Binary Search.
- Implementation of Recursive Binary Search.
- Comparison between iterative and recursive approaches.
- Analysis of best, average, and worst-case complexity.
- Analysis of time and space complexity.
- Measurement of execution time for different input sizes.
- Storage of experimental results in CSV format.
- Generation of performance graphs.
- Comparison of theoretical and experimental complexity.
- Understanding the effect of input size on algorithm performance.

---

## 10. Conclusion

The Algorithm Performance Analyzer demonstrates the theoretical and experimental performance of Iterative and Recursive Binary Search.

Both algorithms have a time complexity of O(log n) in the average and worst cases. The experimental results show that both algorithms remain efficient for large input sizes.

The iterative implementation performed slightly faster in the experiment, while the recursive implementation required additional stack space due to recursive function calls.

This experiment provides a practical understanding of how theoretical complexity relates to actual algorithm performance.
