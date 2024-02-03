## Functional Interfaces and Lambda Expressions
> @FunctionalInterface annotation. Functional interfaces are a new concept introduced in Java 8. 
  
> An interface with exactly one abstract method becomes a Functional Interface.
> We don’t need to use @FunctionalInterface annotation to mark an interface as a Functional Interface.

> @FunctionalInterface annotation is a facility to avoid the accidental addition of abstract methods in the functional interfaces. 
  You can think of it like @Override annotation and it’s best practice to use it. java.lang.Runnable with a single abstract method run() is a great example of a functional interface.

> One of the major benefits of the functional interface is the possibility to use lambda expressions to instantiate them. 
  We can instantiate an interface with an anonymous class but the code looks bulky.

# Runnable interfaces as Functional Interfaces : 
  ```java
  Runnable r = new Runnable(){
			@Override
			public void run() {
				System.out.println("My Runnable");
			}};
```

Since functional interfaces have only one method, lambda expressions can easily provide the method implementation. We just need to provide method arguments and business logic. For example, we can write above implementation using lambda expression as:

  ```java
Runnable r1 = () -> {
			System.out.println("My Runnable");
		};
'''

- If you have single statement in method implementation, we don’t need curly braces also. For example above Interface1 anonymous class can be instantiated using lambda as follows:

Interface1 i1 = (s) -> System.out.println(s);
		
i1.method1("abc");

- So lambda expressions are a means to create anonymous classes of functional interfaces easily. There are no runtime benefits of using lambda expressions, so I will use it cautiously because I don’t mind writing a few extra lines of code.

- A new package java.util.function has been added with bunch of functional interfaces to provide target types for lambda expressions and method references. Lambda expressions are a huge topic, I will write a separate article on that in the future.
