

```cpp
int* bubbleSort(int* list)
{
  int* result = list;
  // Get array size
  int size = getSize(result);

  for (int i = 0; i < size; i++)
  {
    for (int j = i + 1; j < size; j++)
    {
      
      // If there is a lower value than the subject, swap them.
      if (result[j] < result[i])
      {
        int temp = result[i];
        result[i] = result[j];
        result[j] = temp;
      }
    }
  }

  return result;
}
```