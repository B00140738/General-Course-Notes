


### Fixed Sliding Window:

```cpp
#include <iostream>
#include <algorithm>  // For std::max

int maxSumSubarray(int arr[], int n, int k) 
{
    int maxSum = 0;
    int windowSum = 0;
    
    // Calculate the sum of the first k elements
    for (int i = 0; i < k; ++i) 
    {
        windowSum += arr[i];
    }
    
    maxSum = windowSum;
    
    // Slide the window from start to end (n = total size of array (arr))
    for (int i = k; i < n; ++i) 
    {
        windowSum += arr[i] - arr[i - k];
        maxSum = std::max(maxSum, windowSum);
    }
    
    return maxSum;
}

```



### Dynamic Sliding Window:

```cpp
#include <iostream>
#include <climits>  // For INT_MAX

int minSubarrayLen(int arr[], int n, int target) 
{
    int minLength = INT_MAX;
    int windowSum = 0;
    int start = 0;
    
    for (int end = 0; end < n; ++end) 
    {
        windowSum += arr[end];
        
        while (windowSum >= target) 
        {
            minLength = std::min(minLength, end - start + 1);
            windowSum -= arr[start];
            ++start;
        }
    }

    return (minLength == INT_MAX) ? 0 : minLength;
}

```



###  Caterpillar Method:

```cpp
#include <iostream>

int countSubarrays(int arr[], int n, int target) 
{
    int count = 0;
    int windowSum = 0;
    int start = 0;
    
    for (int end = 0; end < n; ++end) 
    {
        windowSum += arr[end];
        
        // Shrink the window as long as the sum is greater than the target
        while (windowSum > target) 
        {
            windowSum -= arr[start];
            ++start;
        }
        
        // If the window sum matches the target, increase the count
        if (windowSum == target) 
        {
            ++count;
        }
    }
    
    return count;
}

```



### Expanding/Shrinking Sliding Window:

```cpp
#include <iostream>
#include <unordered_set>
#include <string>

int lengthOfLongestSubstring(const std::string& s) 
{
    std::unordered_set<char> charSet;
    int maxLength = 0;
    int start = 0;
    
    for (int end = 0; end < s.length(); ++end) 
    {
        // Shrink the window until there are no duplicate characters
        while (charSet.find(s[end]) != charSet.end()) 
        {
            charSet.erase(s[start]);
            ++start;
        }
        
        // Add the current character to the set
        charSet.insert(s[end]);
        
        // Update the maximum length found so far
        maxLength = std::max(maxLength, end - start + 1);
    }
    
    return maxLength;
}

```



### Examples:

#### **Exact Subarray Count Pattern**:

The idea is to calculate the number of subarrays with at most k elements that satisfy the condition, and then subtract the number of subarrays with at most k−1 elements to find the exact number of subarrays with exactly k elements that satisfy the condition.

Here's a general outline of this approach:

**Define a Function for Answer(≤k)**: Implement a function to find the number of subarrays (or subsequences) where the condition is satisfied with at most kkk elements. This typically involves a sliding window or two-pointer approach.  
Calculate Answer(k):

**Answer(k)=Answer(≤k) − Answer(≤k−1)**

By subtracting the result for k−1 from the result for k, you obtain the number of subarrays with exactly k elements that meet the condition:


```cpp
#include <iostream>
#include <unordered_map>

int atMostKDistinct(int arr[], int n, int k) 
{
    std::unordered_map<int, int> count;
    int left = 0;
    int result = 0;
    
    for (int right = 0; right < n; ++right) 
    {
        count[arr[right]]++;
        
        // If we have more than k distinct integers, move the left pointer
        while (count.size() > k) 
        {
            count[arr[left]]--;
            if (count[arr[left]] == 0) 
            {
                count.erase(arr[left]);
            }
            ++left;
        }
        
        // Count the number of valid subarrays ending at `right`
        result += right - left + 1;
    }
    return result;
}

int subarraysWithKDistinct(int arr[], int n, int k) 
{
    return atMostKDistinct(arr, n, k) - atMostKDistinct(arr, n, k - 1);
}

```

This solution covers the following problems:

- Subarrays with Exactly k Distinct Integers:
- Subarrays with Exactly k Odd Numbers:
- Subarrays with Exactly k Even Numbers:
- Subarrays with Exactly k Elements Greater Than a Threshold
- Subarrays with Exactly k Distinct Characters:
- Subarrays with Exactly k Maximum Values:
- Subarrays with Exactly k Minimum Values:
- Subarrays with Exactly k Prime Numbers:
- Subarrays with Exactly k Divisible by a Number:
- Subarrays with Exactly k Increasing or Decreasing Elements

### Summary:

**Fixed Sliding Window:**

- Maximum Sum of K Consecutive Elements
- First Negative Integer in Every Window of Size K
- Average of Subarrays of Size K

**Dynamic Sliding Window:**

- Smallest Subarray with a Given Sum
- Longest Substring with K Distinct Characters
- Fruits into Baskets

**Caterpillar Method:**

- Number of Subarrays with Sum Equals K
- Longest Subarray with Sum Less than or Equal to K
- Subarray Product Less than K

**Expanding/Shrinking Sliding Window:**

- Longest Substring Without Repeating Characters
- Longest Substring with At Most Two Distinct Characters
- Permutation in String
- Minimum Window Substring
- Longest Repeating Character Replacement
- Find All Anagrams in a String