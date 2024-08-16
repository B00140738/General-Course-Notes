
A _reference_ is an alias or an alternative name for an object. All operations applied to a reference act on the object to which the reference refers. The address of a reference is the address of the aliased object.

Because arguments of a function are passed by value, a function call does not modify the actual values ​​of the arguments. If a function needs to modify the actual value of an argument or needs to return more than one value, the argument must be _passed by reference_ (as opposed to being _passed by value_ ). 

Passing arguments by reference can be done using either references or pointers. Unlike C, C++ does not force you to use pointers if you want to pass arguments by reference. The syntax of using a reference is somewhat simpler than that of using a pointer. Passing an object by reference enables the function to change the object being referred to without creating a copy of the object within the scope of the function. Only the address of the actual original object is put on the stack, not the entire object.

   > [!IMPORTANT]
> The following types of references are invalid:
> - References to `NULL`
> - References to `void`
> - References to invalid objects or functions
> - References to References (except with C++11 reference collapsing)

#### Example:

```cpp
int f(int&);
int main() 
{ 
	extern int i;
	f(i); 
}
```

You cannot tell from the function call `f(i)`that the argument is being passed by reference.