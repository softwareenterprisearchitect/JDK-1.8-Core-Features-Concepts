# What are functional or SAM interfaces?
> An interface with only one abstract method is known as a functional interface. As a result, it's also known as the SAM (Single Abstract Method) interface. Because it covers a function as an interface, or in other words, because a function is represented by a single abstract method of the interface, it's called a functional interface.

> Default, static, and overridden methods can all be found in functional interfaces. The @FunctionalInterface annotation can be used to declare Functional Interfaces. This annotation will cause a compiler error if it is used on interfaces with more than one abstract method.
```java
@FunctionalInterface
  
interface Square {
    int calculate(int x);
}
'''


# Implements Functional Interface

```java  
class Test {
    public static void main(String args[])
    {
        int a = 5;
  
        // lambda expression to define the calculate method
        Square s = (int x) -> x * x;
  
        // parameter passed and return type must be
        // same as defined in the prototype
        int ans = s.calculate(a);
        System.out.println(ans);
    }
}
'''
