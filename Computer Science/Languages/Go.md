## What is Go? why learn Go?



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

### Pointers
Sometimes when we pass variables in variety of functions, classes and objects sometimes these variables are actually not passed along instead a copy is generated which is passed to the functions or classes or objects. This causes irregularity in the program to avoid this problem we use pointers. Pointers works by not passing the variables but the memory address of the variable to the function, class, object. Due to this whatever process you want to do on the variable you are doing with the real variable only and not the copy.


```go
var <ptr_name> *<datatype> // * only creates the pointer and doesn't reference it.
fmt.Println(<ptr_name>) // Gives nil because no reference is given to it to point to.
```
In the previous case we just created the pointer and didn't reference it.


```go
number := 23
var ptr = &number //'&' creates a pointer and references to the memory location of the variable.

fmt.Println(ptr) // Gives the memory address
fmt.Println(*ptr) // Gives the value present at the memory address
```
Here we are creating a variable named as number with value 23, then a pointer 'ptr' that is pointing to the memory address of the variable number. 


# Advance Data Structures

## Arrays
- An array is a fixed-size sequence of elements of the same type.
- The size of an array is determined at compile-time and cannot be changed during runtime.

```go
var <array_name> [n]<datatype> // Initialise the array
<array_name>[index] = value    // Putting values inside the array

//Another way of creating an array.
var elements = [2]string{"element1","element2"}
```

**If we don't insert value at any index it will be filled with:**
- " " in case of strings 
- 0 in case of numbers 
- false in case of bool



## Slices
- A slice is a flexible, variable-length sequence of elements of the same type.
- The size of a slice can be changed dynamically during runtime.
- Slices are backed by arrays, but they provide a more convenient way to work with collections in Go.

```go
var <slice_name>  = []<datatype>{data, goes, here}  // Creates a Slice
<slice_name> = append(<slice_name>,element1,element2) // Adds the elements in slice 

//Another way: Initialising slice using make()
<array_name> := make([]<datatype>,n) 
// here n is just default size if you want you can still add more elements in the slice // it will reallocate the memory if elements > n
```

**Removing a value from slices based on index**
```go
var slice = []string{"hello","who","am","i","are","you"}
var index int = 3 // 3rd index element to remove ie "i"
slice = append(slice[:index], slice[index+1:]...) //#todo explain why use ...
delete(slice,index) // Another way of deleting
```



## Maps
Key value pair data structure

```go
<map_name> = make(map[<key_datatype>]<value_datatype>)
languages = make(map[string]string) 
// Creates a languages map with string -> string pair
languages["js"]= "javascript" // Inserting values
delete(languages,"js") // Deleting values
```

**Iterating through map**
```go
for key,value := range <map_name>{
	fmt.Printf("Key is %v and its value is %v",key,value)
}
// Incase you want to ignore key or value just write '_' as the name
```


## Structs
**There is no concept of inheritance, super, parent, child in Go.**

```go
func main() {
    arbash := User{"arbash", "arbash@cc.com", false, 21} //Create a user
    fmt.Println(arbash) // Just prints the values
    fmt.Printf("Details are: %+v", arbash) //Print key and values 
}

//Initialisation of Struct
type User struct {
    Name   string  //Public variable as Name starts with uppercase
    Email  string
    Status bool
    Age    int
    num    int     //Private variable as num starts with lowercase
}
```

## If - else
Same as other languages.
**but not this syntax**
```go
if i:=3;i<10{ // Here we are intialising and checking in the same line
	fmt.Println("Less than")
}else {
	fmt.Println("Greater than")
}
// Usually use this when handling web requests
```

## Switch Cases
Same as other languages.
however there is a concept of fallthrough
```go
switch number {
    case 1:
        fmt.Println("Dice value is 1")
    case 2:
        fmt.Println("Dice value is 2")
    case 3:
        fmt.Println("Dice value is 3")
        fallthrough
    case 4:
        fmt.Println("Dice value is 4")
        fallthrough
    case 5:
        fmt.Println("Dice value is 5")
    case 6:
        fmt.Println("Dice value is 6")
    default:
        fmt.Println("Default case")
    }
```
here we see fallthrough in  case 3 and 4 what this does is:
If the value of number is 3 it will not only run the 3rd case but also the case below it i.e. 4th.
now 4th case also has a fallthrough so it will also cause case5 to run. the program stops after running case5.

