String trim() and strip() method

```java
var s = "  bla\t \n ";
System.out.println(s.trim()); // bla
\\ remove whitespace include \t, \n, \r
\\ strip() support unicode
```

String intern() method

```java
var s = "bla";
var t = new String("bla");
System.out.println(s == t); // false

// If the literal is not yet in the string pool, Java will add it at this time.
var t = new String("bla").intern();
System.out.println(s == t); // true
```

