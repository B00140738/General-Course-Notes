
Kadane's Algorithm is a way to find the **maximum sum of a contiguous subarray** within a larger array of numbers, which may include negative numbers.

### Think of it like this:

You're walking through an array, and at each step, you decide:

1. Should I keep extending the subarray I'm currently considering?
2. Or should I start fresh from this number because the previous subarray has dragged my total down too much?

### Simple Steps:

1. Start with two variables:
    
    - `max_current`: The maximum sum of the subarray ending at the current position.
    - `max_global`: The overall maximum sum found so far.
2. As you move through the array, for each number:
    
    - Update `max_current` to be either:
        - The current number itself (start fresh), or
        - The current number added to `max_current` (extend the subarray).
    - Update `max_global` to the maximum of `max_current` and itself.
3. At the end, `max_global` holds the maximum sum of any contiguous subarray.
    

### Example:

Array: `[-2, 1, -3, 4, -1, 2, 1, -5, 4]`

1. Start: `max_current = -2`, `max_global = -2`
2. Move to `1`: `max_current = max(1, -2+1) = 1`, `max_global = max(-2, 1) = 1`
3. Move to `-3`: `max_current = max(-3, 1-3) = -2`, `max_global = 1`
4. Move to `4`: `max_current = max(4, -2+4) = 4`, `max_global = 4`
5. Move to `-1`: `max_current = max(-1, 4-1) = 3`, `max_global = 4`
6. Continue...

Final result: Maximum sum is **6** (from subarray `[4, -1, 2, 1]`).

### Why Kadane’s Works:

It efficiently tracks the maximum without trying every possible subarray, making it super fast (time complexity: **O(n)**).