# Variadic functions

Example of variadic function is commonly known ‘print’ function.

This type of function as a parameter can take values separated by comma (can take zero values or even hundreds of values).

Example of custom variadic function:

```
func sumExpenses(_ expenses: Double...) -> Double {
    var total = 0.0
    for expense in expenses {
        total += expense
    }
    return total
}
```

Usage: 

```
let sum = sumExpenses(1, 2, 4, 5)
print(sum) //prints 12
```
