# Struct VS Class

1. Class never has its own initializer. Instead you always have to create it.

2. Class can inherit from another class.

3. Class can be defined as final, what is connected with inheritance.

4. Class is reference type, but struct not. It means that struct is always copying to new instance of object, but when you change values of properties of class you may change few objects of that class.

5. Class can have deinitilizer which is called when instance of class is destroyed.

6. Properties of class can be changed even if the instance is declared as constant.
