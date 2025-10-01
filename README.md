Got it 👍 Here’s the **final README** in the exact format you asked, with your code’s algorithm and its Big O analysis inserted after the **Comparison Table** section:

---

# Algorithm Analysis using Big O Notation

**Aim:**
To study and understand **Algorithm Analysis** using **Big O Notation** for measuring the efficiency of algorithms.

---

## Theory

Algorithms are the backbone of computer science. To evaluate them, we need a way to measure their efficiency in terms of:

* **Time Complexity** → How the execution time of an algorithm grows as input size increases.
* **Space Complexity** → How much additional memory an algorithm requires as input size increases.

Since execution times vary across hardware and compilers, we use **Big O Notation** as a **mathematical model** to analyze algorithms independent of the machine.

---

## What is Big O Notation?

Big O Notation describes the **upper bound** of an algorithm’s growth rate. It tells us how the performance scales with input size (n), ignoring constant factors and less significant terms.

For example:

* If an algorithm takes `3n + 2` steps → Big O = **O(n)**
* If an algorithm takes `2n² + 5n + 7` steps → Big O = **O(n²)**

We only keep the **most dominant term**, since it has the greatest impact as `n` grows.

---

## General Syntax of Big O Notation

```
O(f(n))
```

Where:

* **O** = Order of growth
* **f(n)** = Function describing how runtime increases with input size `n`

---

## Common Time Complexities

### 1. O(1) – Constant Time

Execution time remains the same regardless of input size.

Example: Accessing an array element by index.

```cpp
int getFirst(int arr[]) {
    return arr[0];  // Always takes constant time
}
```

---

### 2. O(log n) – Logarithmic Time

Input size reduces by half at each step.

Example: Binary Search.

```cpp
int binarySearch(int arr[], int n, int target) {
    int low = 0, high = n-1;
    while(low <= high) {
        int mid = (low+high)/2;
        if(arr[mid] == target) return mid;
        else if(arr[mid] < target) low = mid+1;
        else high = mid-1;
    }
    return -1;
}
```

---

### 3. O(n) – Linear Time

Runtime grows directly with input size.

Example: Linear Search.

```cpp
int linearSearch(int arr[], int n, int target) {
    for(int i=0; i<n; i++) {
        if(arr[i] == target) return i;
    }
    return -1;
}
```

---

### 4. O(n log n) – Linearithmic Time

Common in efficient sorting algorithms.
Example: Merge Sort, Quick Sort.

---

### 5. O(n²) – Quadratic Time

Common with nested loops.

Example: Bubble Sort.

```cpp
void bubbleSort(int arr[], int n) {
    for(int i=0; i<n; i++) {
        for(int j=0; j<n-i-1; j++) {
            if(arr[j] > arr[j+1]) {
                swap(arr[j], arr[j+1]);
            }
        }
    }
}
```

---

### 6. O(2ⁿ) – Exponential Time

Runtime doubles with each new input size.
Example: Recursive Fibonacci without memoization.

---

### 7. O(n!) – Factorial Time

Extremely inefficient, grows faster than exponential.
Example: Brute force Travelling Salesman Problem.

---

## Space Complexity

Just like time, algorithms can also be analyzed for **memory usage**:

* **O(1):** Constant memory (in-place operations).
* **O(n):** Linear memory (storing extra arrays).
* **O(n²):** Memory grows quadratically (like 2D arrays).

---

## 📊 Big O Comparison Table

| Big O          | Name         | Example Algorithm           |
| -------------- | ------------ | --------------------------- |
| **O(1)**       | Constant     | Accessing array element     |
| **O(log n)**   | Logarithmic  | Binary Search               |
| **O(n)**       | Linear       | Linear Search               |
| **O(n log n)** | Linearithmic | Merge Sort, Quick Sort      |
| **O(n²)**      | Quadratic    | Bubble Sort, Insertion Sort |
| **O(2ⁿ)**      | Exponential  | Recursive Fibonacci         |
| **O(n!)**      | Factorial    | Travelling Salesman Problem |

---

## Example Program Analysis


**Algorithm of code:**

1. Start the program.
2. Define a function `printAllPairs(arr, n)`.
3. Use two nested loops:

   * Outer loop runs from `i = 0` to `n-1`.
   * Inner loop runs from `j = 0` to `n-1`.
   * Print the pair `(arr[i], arr[j])`.
4. In `main()`:

   * Initialize an array `{1, 2, 3}`.
   * Call the function with `n = 3`.
5. End program.

**Time Complexity Analysis:**

* Outer loop runs **n times**.
* Inner loop runs **n times** for each outer loop iteration.
* Total operations = **n × n = n²**.
* Hence, **Time Complexity = O(n²)** (Quadratic).

**Space Complexity Analysis:**

* Uses only a few variables (`i`, `j`, and array reference).
* No extra memory proportional to `n`.
* Hence, **Space Complexity = O(1)** (Constant).

**Sample Output:**

```
1, 1
1, 2
1, 3
2, 1
2, 2
2, 3
3, 1
3, 2
3, 3
```

---

## Why Big O Analysis Matters?

* **Predicts scalability:** Helps us understand if an algorithm will work efficiently for large inputs.
* **Compares algorithms:** Easier to choose the right approach.
* **Optimization:** Guides us toward improving performance.

---

## Key Learning Outcomes

* Understood the concept of **time and space complexity**.
* Learned how to express growth of algorithms using **Big O Notation**.
* Explored common complexities from **O(1) to O(n!)**.
* Learned why **efficiency analysis** is crucial in algorithm design.

---

👉 Would you also like me to add **diagrams/flowcharts** (like how nested loops expand step by step for O(n²)) to make the README even more explanatory?
