# key takeway
- avoid undefined behavior(e.g., asign out of range signed value to signed
  or implementation dependent behavior
- don't mix unsigned and signed. signed get to converted to unsigned

# string literal
- null character appende

# initialization
- initialization  & assignment NOT THE SAME THING
- default initialization
  - build-in type->undefied if local, 0 if outside any function

# declaration v. definition
- for variable, definition is declaration -> need to use extern to obtain declaration that is not definition
# compound type

```cpp
int *&r = p; //r is a reference to pointer to int.
const int &rc = ci //reference to const
const int *pci = &ci; //pointer to const
int *const cp = i; //const pointer
const int *const cpci; //const pointer to const int

```
# type alias
- typedef is the traditional way
- using is introduced in the new standard
- auto
  - top level const ignore
  - auto of reference yield type of object itself

- decltype
  - use this to define variable
  - e.g. in for loop (for decltype(v.size()) i = 0; ...)
  - v. reference
	- this is the only occasion where reference is treated as ref, not object

