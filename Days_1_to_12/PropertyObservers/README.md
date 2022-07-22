# Property observers

This kind of values enable to update or perform some actions when this value is changed.

Example:

I created two structures:

* Item:

```
struct Item {
    var name: String
    var estimatedPrice: Double
}
```

* Shopping list:

```
struct ShoppingList {

    var estimatedExpense: Double = 0.0
    var items: [Item] = [] {
        didSet {
            estimatedExpense = items.reduce(0) { $0 + $1.estimatedPrice }
        }
    }
} 
```

Usage:

```
let bread = Item(name: "🍞", estimatedPrice: 3.90)
let milk = Item(name: "🥛", estimatedPrice: 2.79)
let banana = Item(name: "🍌", estimatedPrice: 0.90)

let itemsToBuy = [bread, milk, apple]

var shoppingList = ShoppingList()
shoppingList.items = itemsToBuy
let estimatedExpense = shoppingList.estimatedExpense
print(estimatedExpense) //print 7.59 ✅
````

:warning: Warning! Computed properties can’t be constants!
