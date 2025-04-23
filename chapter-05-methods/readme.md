Varargs

```java
public void method(int...i){}
public void method(int k, int...i){}
public void method(int...i,int k){} // not compile, vargs should be the last one
public void method(int...i,int...k){} // does not compile, two vargs
```

Using varargs

```java
public void method(int k, int...i){
  System.out.println(i.length);
}

method(1);                  // print 0
method(1,2);                // print 1
method(1,2,3);              // print 2
method(1, new int[]{4,5});  // print 2
method(1, null);            // NullPointerException
```

Overloading varargs
```java
public class C{
  public void m(int[] i) {}
  public void m(int...i) {} // DOES NOT COMPILE
}
```
