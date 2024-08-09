


```cpp
// Function to swap two elements 
void swap(int &a, int &b) 
{ 
	int temp = a; 
	a = b;
	b = temp; 
}
```




```cpp
// Partition function
int partition(int arr[], int low, int high)
{
  int pivot = arr[high];
  int i = low - 1; // i = -1

  for (int j = low; j < high; j++)
  {
    if (arr[j] < pivot)
    {
      i++; // Tell us where/what index the smaller element is supposed to be                     placed at ('i' is now index 0).
      swap(arr[i], arr[j]) // Move the smaller element to the front so it can be                                 in ascending order.
    } 
  }
  // Then when all the smaller elements are sorted and to the left, place the           pivot after the last lower value
  swap(arr[i + 1], arr[high]); // Swap the pivot element with the element at i + 1
  return i + 1; // Return the partitioning index
}
```





```cpp
// QuickSort function
void quickSort(int arr[], int low, int high) {
    if (low < high) {
        int pi = partition(arr, low, high); // Partitioning index
        
        // Recursively sort the elements before and after partition
        quickSort(arr, low, pi - 1);
        quickSort(arr, pi + 1, high);
    }
}
```






```cpp
#include <iostream>
using namespace std;

// Main function
int main() {
    int arr[] = {10, 7, 8, 9, 1, 5};
    int n = sizeof(arr) / sizeof(arr[0]);
    
    cout << "Original array: ";
    printArray(arr, n);
    
    quickSort(arr, 0, n - 1);
    
    cout << "Sorted array: ";
    printArray(arr, n);
    return 0;
}

```





![[Quick Sort Demonstration.mkv]]
