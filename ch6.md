# chater 6 notes
## a summary of const expression, constexpr, constexpr functions
- constant expression
  - expressions that whose value cannot change
  - can be evaluated at compile time
  - examples
    - literal //const int m= 20
    - const object initialized from a constant expression // const int l = m + 1;

- constexpr
  - by declaring something as constexpr, we are asking compiler to verify that something is a constant expression
  - variable declared as constexpr must be initialized by constant expression
  - constexpr variable can be initialized by
	- (1) literal
    - (2) constant expression
    - (3) constexpr function // constexpr int sz = size() is only legal if size() is a constexpr function

- constexpr function
  - a function that can be used in a constant expression
  - (1) return type must be literal type
  - (2) parameter(args) must be literal type
    - constexpr size_t scale(size_t cnt) { return new_sz() * cnt; }
    - the return type of scale function is a constexpr function if arg(i.e. cnt) is a constant expression (assuming new_sz() is;
  - (3) exactly one return statement

