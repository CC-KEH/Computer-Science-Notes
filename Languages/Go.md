
## Types
- Almost everything is a type
- the first letter of the method decides the access of the method
- Variable type should be initialized in advance

#### Various types:
- String
- Integer
- Bool
- uint8  :  unsigned 8 bit Integers (0 - 255)  and similarly for 16, 32, 64
- int8  :    signed 8 bit Integers (-128 - 127) and similarly for 16, 32, 64
- uintptr
- float32  : 5 values after the decimal, float64 - 13 values after decimal
- Complex64  : complex numbers with float 32 real and imaginary parts, similarly for complex128 - 64 bit float

#### Aliases for various types
- uint -> int
- unint8 -> byte
- int32 -> rune 

##### Advance Types:
- Arrays
- Slices
- Maps
- Structs
- Pointers

#### Others:
- Functions
- Channels
- etc.


## Lexer




# Memory Management

- Allocation and deallocation happens automatically
- Garbage collection happens automatically
- The GOGC variable sets the initial garbage collection target percentage. A collection is triggered when the ratio of freshly allocated data to live date remaining after the **previous** collection reaches this percentage. The default is GOGC=100, Setting GOGC=off disables the Garbage collector entirely. [To change GOGC value use runtime package](https://pkg.go.dev/runtime)
- various other methods that helps in low level programming can be found in runtime package. 

#### Following are the methods that we are usually going to use in memory management.

| new()                                  | make()                               |
| -------------------------------------- | ------------------------------------ |
| allocate memory but no initialization. | allocate memory with initialization. |
| you will get the memory address        | you will get the memory address      |
| Zeroed memory                          | Non-zeroed memory                    |

#### Pointers 
