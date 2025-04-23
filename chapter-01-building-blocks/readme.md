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
