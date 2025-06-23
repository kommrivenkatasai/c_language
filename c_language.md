# 💡 Pointer Practice in C

A collection of beginner-friendly pointer problems in C to understand arrays, pointers, and memory manipulation.

---

## ✅ Problem 3: Print Elements of an Array Using a Pointer

**📝 Problem Statement:**  
Given an array of integers, use a pointer to print each element.

### 🔹 Array:
```c
int arr[] = {1, 2, 3, 4, 5};
```

### 🧠 Concept:
- `int *p = arr;` points to the first element
- Use `*(p + i)` or `p[i]` to access elements
- Loop through array using pointer arithmetic

### ✅ Solution:
```c
#include <stdio.h>

int main() {
    int arr[] = {1, 2, 3, 4, 5};
    int *p = arr;  // or &arr[0]

    for (int i = 0; i < 5; i++) {
        printf("%d ", *(p + i));
    }

    return 0;
}
```

---

## ✅ Problem 4: Find the Maximum Element Using a Pointer

**📝 Problem Statement:**  
Use a pointer to find the maximum number in an array.

### 🔹 Array:
```c
int arr[] = {15, 22, 7, 30, 18};
```

### 🧠 Plan:
- Use pointer `p = arr`
- Keep a `max` variable
- Compare `*p` with `max` during iteration

### ✅ Solution:
```c
#include <stdio.h>

int main() {
    int arr[] = {15, 22, 7, 30, 18};
    int *p = arr;
    int max = *p;

    for (int i = 1; i < 5; i++) {
        if (*(p + i) > max) {
            max = *(p + i);
        }
    }

    printf("Maximum element: %d\n", max);
    return 0;
}
```

---

## ✅ Problem 5: Reverse the Array Using Pointers

**📝 Problem Statement:**  
Reverse an array in-place using two pointers.

### 🔹 Input:
```c
int arr[] = {10, 20, 30, 40, 50};
```

### 🔹 Output:
```c
{50, 40, 30, 20, 10}
```

### 🧠 Plan:
- Use two pointers: `start` and `end`
- Swap values pointed by them
- Move `start++` and `end--` toward center

### ✅ Solution:
```c
#include <stdio.h>

int main() {
    int arr[] = {10, 20, 30, 40, 50};
    int *start = arr;
    int *end = arr + 4; // last element (5 - 1)

    while (start < end) {
        int temp = *start;
        *start = *end;
        *end = temp;

        start++;
        end--;
    }

    // Print the reversed array
    for (int i = 0; i < 5; i++) {
        printf("%d ", arr[i]);
    }

    return 0;
}
```

---
