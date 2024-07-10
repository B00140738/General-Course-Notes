The find() function is used to **find/return the first occurrence of a specified string, prefix, substring or character in a string.** If no results are found, [[npos]] is returned instead. This can be used to find a certain combination of letters/pattern that is present in multiple words/an Array of strings/chars.

Additionally this can also be used conditionally in both WHILE and FOR loops. For example, if we wanted to keep looping until we have exhausted all possible present/located prefixes, we can just do the following:

#### FOR Loop:

```cpp
#include <string>
using namespace std;

// Example string
std::string example = "this";

while (example.find("is") != 0)
{
	// Do Something...
}
```