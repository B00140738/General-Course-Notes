
### Getting the size of an Array

Unlike other languages such as Java, C/C++ does not have a `.size()` method. If you're working with raw Arrays, you need to pass the size separately or create another method to obtain a size/length value. 

   > [!NOTE]
>If you're using `std::vector`, you can use `.size()`.

#### Code Example:

```cpp
int getSize(int* list)
{
  // Set start value
  int len = 0;
  // While there are values left, add 1 to the total size/number of elements.
  while (list[len] != -1)
  {
    len++;
  }
  return len;
}

```