
Difficulty: **Easy**

## Two Pointers

The pointer is a very important concept in C/C++, as well as in algorithms. Applied to an algorithm, **the pointer can be used to represent the current element in a sequence (such as array or string).** **We can combine two pointers in different traversal ways** to express the complex algorithm logic.

The two pointers technique is widely used in many algorithm scenarios. According to mechanism and usage, they can roughly be classified into five categories:

1. Old and new state: **old, new = new, cur_result**
2. Slow and fast runner: **slow-> fast->->**
3. Left and right boundary: **|left-> ... <-right|**
4. Pointer-1 and pointer-2 from two sequences: **p1-> p2->**
5. Start and end of sliding window: **|start-> ... end->|**

### Slow & Fast Runner:

The first idea is to use two pointers as slow runner and fast runner. Each of them flags a key point during traversal. In general, fast runner grows each iteration and slow runner grows with some restrictions. By that, we can process logic based on these two runners.


```python
# slow & fast runner: slow-> fast->->
def slow_fast_runner(self, seq): 
	# initialize slow runner 
	slow = seq[0] # for index: slow = 0
	# fast-runner grows each iteration generally 
	for fast in range(seq): # for index: range(len(seq))
		#slow-runner grows with some restrictions 
		if self.slow_condition(slow):
			slow = slow.next # for index: slow += 1
		# process logic before or after pointers movement 
		self.process_logic(slow, fast)
```


The above technique works by using two pointers: *slow*, and *fast*. Usually, the *fast* pointer increments fast during the loop while the *slow* pointer moves more slowly; only incrementing if a certain condition is met.
 
#### Example:

```python
# [26] https://leetcode.com/problems/remove-duplicates-from-sorted-array/ 
def removeDuplicates(nums: 'List[int]') -> int: 
	if not nums: return 0 
	slow = 0 
	for fast in range(1, len(nums)): 
		# if current element is not duplicate, 
		# slow runner grows one step and copys the current value 
		if nums[slow] != nums[fast]: 
				slow += 1 
				nums[slow] = nums[fast] 
	return slow + 1
```

