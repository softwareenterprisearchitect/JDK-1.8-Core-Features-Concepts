## What are Lambda Expressions in Java?

- Java lambda expressions were the platform's first foray towards functional programming.
- An unnamed expression or function that is recast as a parameter for any other function is known as a Java Lambda Expression or Lambda Function.
- In Java, lambda expressions are functions that can be shared as an object. It can also be used to refer to a specific thing. Lambda Expressions require more compact coding, as well as implementing a mechanism for executing Java 8's functional interfaces. In Java, lambda expressions allow users to express a single functional unit that can be reused over multiple lines of code.


#Lambda Expressions Syntax:
```
(Argument List)-> {expression;}
'''

## Example

```java
public class LambdaExpressionExample{  
    public static void main(String[] args) {  
    // using lambda Expression  
        new Thread(():>System.out.println("Thread is started: using Lambda Expressions")).start();  
        // old way  
        new Thread(new Runnable() {  
            @Override  
            public void run() {  
                System.out.println("Thread is started: using old method");  
            }  
        }).start();  
    }  
}
```
