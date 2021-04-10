# golang pointers 
## What is the difference between * and &

One of the most fun things as a software developer is learning new languages. NodeJS is awesome, and one of the easiest ways to get a micro-service up and running. I will not go into the pros and cons of NodeJS vs. Golang as a backend language; only to say that the project and client I am working with decided to move to Golang. I love it. There is a learning curve, however, as with most new things you pick up. The basics matter, as you need to learn the alphabet before you can compose full sentences. One of the most basic concepts in Golang (as well as other languages such as C, and C++), is the concept of pointers.

This is how I understand pointers in golang. I tend to need very explicit narratives. You may not have the same learning style, but hopefully this helps nonetheless. 

Pointers are hex memory addresses of a variable. There are two notations in golang to work with pointers, and each notation serve a different, but related purpose. The notations are * and &.

Consider the following block of code:

```
package main

import "fmt"

func main() {
  var a string = "hello world"
  fmt.Println(a) // output: hello world
  fmt.Println(&a) // output: 0xc00010a220 (won't be this exactly)
}
```
As expected, the output of printing the variable "a" to the terminal is the string "hello world". The output, however, of printing &a, or "pointer to a" - is a hex memory address.

Great, that's easy enough to understand. "&a" simply denotes that the system is to provide the memory address of the variable a. A reference if you will. 

### What is & in golang?
>& - Says, "get the address of the variable that follows"

Now let's build on the above code and look at another situation:


```
package main

import "fmt"

func main() {
  var a string = "hello world"
  fmt.Println(a) // output: hello world
  fmt.Println(&a) // output: 0xc00010a220 (won't be this exactly)

  var b *string = &a //declare "b" as type "pointer to string"
  fmt.Println(b) // output: 0xc00010a220 (wont' be this exactly)
  fmt.Println(*b) // output: hello world
}
```
`var b *string` says that whatever is assigned to "b" must be a pointer memory address. Furthermore, that memory address must point to a type string. Therefore, on the right side of equation, we assign the pointer memory address of a (&a) to b. 

The result of outputting b to the terminal is the memory address of a, as denotted by the assignment of &a to b.

The result of outputting *b, however, is "hello world", because prefixing any value (or variable that holds a value) with "*" tells the system to use the value as a pointer and return whatever is at that address. 

### What is * in a type declaration? 
>"*" says "you are declaring that this variable holds a memory address to a string, or int or whatever type follows *". For example, "var a *int" declares that the variable "a" holds a memory address(pointer) to an int datatype.

### What is * everywhere else?

>"*" says "give me whatever the variable that follows is pointing to". So your variable better be an actual memory address, otherwise you'll get an error. It tells the system to use the value as a pointer and return whatever is at that address.
