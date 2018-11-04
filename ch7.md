# chapter 7 notes

## design of class
- things that go in header file
  - class definition
  - declaration of functions that are conceptually part of the class but does not belong to class itself e.g. print.
	- but where to define them??? seems to be utility functions
    - need to define in .h file so that user can use
    - definitely should not be defined in .h file otherwise it will be defined each time the .h file is included ->linker error (i.e., same functions in main .o file & person.o file)

- things that go in cpp file
  - implementation of non-inline member functions

