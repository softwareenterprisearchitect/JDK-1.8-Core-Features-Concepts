# Functional Methods , Default Methods and Static Methods In JDK 1.8 
> @FunctionalInterface : 1 and only one abstract method in Java

> default Method : 0/1 to ... N default methods.

> static Method: 0/1 to ... N static methods.


``` java 
package com.jdk18.exmp.fp


@FunctionalInterface
public interface Interface1 {

	void method1(String str);
	
	default void log(String str){
		System.out.println("I1 logging::"+str);
	}
	
	static void print(String str){
		System.out.println("Printing "+str);
	}
	
	//trying to override Object method gives compile-time error as
	//"A default method cannot override a method from java.lang.Object"
	
//	default String toString(){
//		return "i1";
//	}
	
}
'''

# Implementing Functional Interfaces In Java :
> We can implement functional interfaces in same way as regular interfaces by implementing it in subclasses.

``` java
public class MyClass implements Interface1, Interface2 {

	@Override
	public void method2() {
	}

	@Override
	public void method1(String str) {
	}

	//MyClass won't compile without having it's own log() implementation
	@Override
	public void log(String str){
		System.out.println("MyClass logging::"+str);
		Interface1.print("abc");
	}
	
}
```
