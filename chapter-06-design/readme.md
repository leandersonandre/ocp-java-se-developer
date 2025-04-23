Initializing classes
```java
public class A{
  static {System.out.print("A");}
}
public class B extends A{
  static { System.out.print("B");}
  public static void main(String args[]){
    System.out.print("C");
    new B();
    new B();
    new B(); 
  }
}
// print ABC once.
// Order
// Super class will be initialized first
// process all static variables in order
// process all static initializers in order
```

Initializing instances
```java
public class A{
  static {System.out.print("A");}
  public A() {
		System.out.print("G");
	}
	{System.out.print("D");}
}
public class B extends A{
  static { System.out.print("B");}
	{System.out.print("E");}
  public Main() {
		System.out.print("G");
	}
  public static void main(String args[]){
    System.out.print("C");
    new B();
    new B();
    new B(); 
  }
}
// print ABCDFEGDFEGDFEG once.
// Order
// Super class will be initialized first
// process all instance variables in order
// process all instance initializers in order
// process the constructor
```

Hiding Static Methods
Static methods are not inherit from each other.
```java
class A{
  public static void m() { // same signature
		System.out.print("A");} 
}
class B extends A{
  public static void m() { // same signature
		System.out.print("B");} 
}
public class C {
	public static void main(String args[]){
		B b = new B();
		b.m(); // print B
		A a = new B();
		a.m(); // print A
	}
}
class D{
  public static void m() { // same signature
		System.out.print("D");} 
}
class E extends D{
  public  void m() { // DOES NOT COMPILE
		System.out.print("E");} 
}
```

Hiding Static Methods
Static methods are not inherit from each other.
```java
class A{
  protected boolean x = false;
}
class B extends A{
  protected boolean x = true;
}
public class C {
	public static void main(String args[]){
		B b = new B();
		A a = b;
		System.out.println(b.x); // print true
		System.out.println(a.x); // print false
	}
}
```

keywords combinations
```
// abstratc and final is illegal
public abstract final void method();

// abstract and final is illegal
private abstract void method();

// abstract and static is illegal
abstract static void method();
```
