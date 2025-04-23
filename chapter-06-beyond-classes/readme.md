duplicate default methods
```java
public interface W{
  public default int m(){return 0;}
}
public interface M{
  public default int m(){return 0;}
}

public class Y implements W, M{} // DOES NOT COMPILE,
// The compiler dont decide with default method should use.

public class Y implements W, M{
  public  int m(){return 0;} // COMPILE
}
```

Calling a hidden default method
```java
public interface W{
  public default int m(){return 0;}
}
public interface M{
  public default int m(){return 0;}
}

public class Y implements W, M{
  public  int m(){return W.super.m();} // Special syntax
}
```

Sealed class
```java
keywords
sealed: indicates that a class only be extended by named classes
permits: indicates what classes can extend a sealed class
no-seald: applied to a subclass of one sealed class and indicates that can be extended by any classes.

public sealed class A permits B, C{}
public class B extends A{}
public non-sealed class C extends A{}

// DOES NOT COMPILE
public sealed class A permits B{}
public class B {} // class B doesnt extends A
```
