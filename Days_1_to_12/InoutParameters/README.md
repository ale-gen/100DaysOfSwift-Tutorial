# Inout parameters

Inout parameters allow changing values which existed before calling the function. It means that we are working on real value (its reference) not its copy.

Example of custom function with inout parameter:

```
func addFive(to number: inout Int) {
    number += 5
}
```

Usage:
```
var myNumber = 13
print(myNumber) //prints 13
addFive(to: &myNumber)
print(myNumber) //prints 18
```

As you can see above - inout parameter contains special keywords (inout in declaration of function and & in calling a function).

Also the value which is passed to function as inout parameter can’t be constant.
