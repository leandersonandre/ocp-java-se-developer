Identifiers declarations
```java

# invalid
_
a.b
true
1_s
a!
```

Var declarations
```java
# invalid
var i = null;
var i = 2, j;
var i = 2, j = 3;
var i = 2, i = null;

```

Number literal declarations
```java
# valid
var i = 3_1;
var i = 3__1;
var i = 3_1.0_1;

# invalid
var i = _31;
var i = 31_;
var i = 31_.01;
var i = 31._01;
```

Block text declarations
```java
# valid
var i = 0;
var text = """
	bla"" + i + 
	""";
# quotes "" are automatically escaped.
# The substring + i + is a text, this is not a use of the variable i.

var text = """
	bla\nbla
	""";
# There is a line break.

var text = """
	first \s
	second \
	third
        """;
# the \ means dont break line.
# \s means keep the previous whitespaces
```

Short/byte automatic casting in operations
```java
# Compile error, short casting automatically to int
short i = 10;
short b = 10;
short c = i + b;

```
