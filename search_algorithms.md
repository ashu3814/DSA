
## 1. Linear Search (O(n))

### Basic Implementation
```javascript
function linearSearch(arr, target) {
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] === target) return i;
    }
    return -1;
}
```

### Key Points:
- Simplest search algorithm
- Works on any array (sorted/unsorted)
- Checks every element sequentially
- Worst-case: Target is last element or not present

### Example:
```javascript
console.log(linearSearch([5, 2, 9, 1], 9)); // 2
console.log(linearSearch([5, 2, 9, 1], 3)); // -1
```

---

## 2. Binary Search (O(log n))

### Prerequisite: Sorted Array
```javascript
function binarySearch(arr, target) {
    let left = 0;
    let right = arr.length - 1;

    while (left <= right) {
        const mid = Math.floor((left + right) / 2);
        
        if (arr[mid] === target) return mid;
        if (arr[mid] < target) left = mid + 1;
        else right = mid - 1;
    }
    return -1;
}
```

### Key Points:
- Requires sorted array
- Divide-and-conquer approach
- Eliminates half the remaining elements each step
- Much faster than linear for large datasets

### Example:
```javascript
const sorted = [1, 3, 5, 7, 9];
console.log(binarySearch(sorted, 5)); // 2
console.log(binarySearch(sorted, 2)); // -1
```

### Visualization:
```
[1, 3, 5, 7, 9] → mid=5 (match)
[1, 3] → mid=1 (too small)
[3] → mid=3 (not found)
```

---

## 3. Recursive Binary Search (O(log n))

### Implementation
```javascript
function recursiveBinarySearch(arr, target, left=0, right=arr.length-1) {
    if (left > right) return -1;
    
    const mid = Math.floor((left + right) / 2);
    
    if (arr[mid] === target) return mid;
    if (arr[mid] < target) {
        return recursiveBinarySearch(arr, target, mid + 1, right);
    } else {
        return recursiveBinarySearch(arr, target, left, mid - 1);
    }
}
```

### Key Points:
- Same logic as iterative binary search
- Uses call stack instead of loop
- More elegant but has stack size limitations
- Default parameters handle initial bounds

### Example:
```javascript
console.log(recursiveBinarySearch(sorted, 7)); // 3
console.log(recursiveBinarySearch(sorted, 0)); // -1
```

---

## Comparison Table

| Algorithm          | Time     | Space    | Requires Sorted? | Best For          |
|--------------------|----------|----------|------------------|-------------------|
| Linear Search      | O(n)     | O(1)     | No               | Small/unsorted data |
| Binary Search      | O(log n) | O(1)     | Yes              | Large sorted data |
| Recursive Binary   | O(log n) | O(log n) | Yes              | Code readability |

## When to Use Which:
1. **Unsorted data** → Linear Search
2. **Large sorted data** → Binary Search
3. **Readability preferred** → Recursive Binary
4. **Memory constrained** → Iterative Binary

## Edge Cases:
```javascript
// Empty array
console.log(linearSearch([], 1)); // -1

// Duplicate values
console.log(binarySearch([1, 2, 2, 3], 2)); // 1 or 2

// Single element
console.log(recursiveBinarySearch([5], 5)); // 0
```

## Practice Variations:
1. Find first/last occurrence in duplicates
2. Search in rotated sorted array
3. Find closest number to target
4. Implement for custom objects
``` 

Key Takeaways:
- Linear: Simple but slow for big data
- Binary: Fast but needs sorted input
- Recursive: Elegant but uses more memory
