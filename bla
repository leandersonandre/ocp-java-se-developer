Switch expression data type:

```
Support only int, byte, short, and char and theirs wrapping classes.

long is not supported.
```

Variable declaration inside if statement
```java
public void bla(Object o) {
		if(o instanceof Integer b) {
			
		}else if(o instanceof Integer b && b  < 10) { # correct, b is declared and can be used
			b = 10;
			
		}else if(o instanceof Integer b || b  < 10) { # b is not declared because b couldnt be a Integer.
			b = 10;
		}
}
```

Switch expressions
```java
var x = switch (i) {
		case 1 -> 0;
		case 2 -> { yield 9;} # when use { } its mandatory to use yield keyword and ;
		default -> -1; # mandatory include default clausure
};
```
