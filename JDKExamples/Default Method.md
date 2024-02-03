# What Is a Default Method, and When Should It Be Used?
> A default method is an interface method that has an implementation.To add new functionality to an interface while keeping backward compatibility with existing classes that implement the interface, we can utilise a default method:

'''java
public interface Vehicle {
    public void move();
    default void hoot() {
        System.out.println("peep!");
    }
}
'''


> When a new abstract method is added to an interface, all implementing classes will break until the new abstract method is implemented. The default method was used to fix this problem in Java 8.

> The Collection interface, for example, lacks a forEach function declaration. As a result, implementing such a method would disrupt the entire collections API.

> The default method was introduced in Java 8 to allow the Collection interface to provide a default implementation of the forEach method without requiring the classes that implement this interface to do so.
