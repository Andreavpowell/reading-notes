# JavaScript Expressions and Operators
* JavaScript has binary, unary, and one special ternary operator (conditional operator).
* Binary - requires two operands, one before and after the operator `operand1 operator operand2`
  * `3+4` or `x*y`
* Unary - requires a single operand before or after the operator `operator operand`
  * `x++` or `++x`

## Assignment Operators
* assigns a value to its left operand based on the value of its right operand
* the simple assignment operator is `=`
  * `x = y` assigns the value of `y` to `x`  

Name                            | Shorthand Operator | Meaning 
-----------                     | ------------------ | -------
assginment                      | `x = y`            | x = y
addition assignment             | `x += y`           | x = x 
subtraction assignment          | `x -= y`           | x = x - y
multiplication assignment       | `x *= y`           | x = x * y
division assignment             | `x /= y`           | x = x / y
remainder assignment            | `x %= y`           | x = x % y
exponentiation assignment       | `x **= y`          | x = x ** y
left shift assignment           | `x <<= y`          | x = x << y
right shift assignment          | `x >>= y`          | x = x >> y
unsigned right shift assignment | `x >>>= y`         | x = x >>> y
bitwise **and** assignment      | `x &= y`           | x = x & y
bitwise **xor** assignment      | `x ^= y`           | x = x ^ y
bitwise **or** assignment       | `x \|= y`          | x = x \| y
logical **and** assignment      | `x &&= y`          | x && (x = y)
logical **or** assignment       | `x \|\|= y`        | x \|\| (x = y)
logical nullish assignment      | `x ??= y`          | x ?? (x = y)  

## Return Value and Chaining
* arguments like `x = y` have a retun value (like most expressions)
* can be retrieved by e.g. assigning the expression or logging it  
`const z = (x = y); // Or equivalently: const z = x = y;`  
  
   `console.log(z); // Log the return value of the assignment x = y.`  
   `console.log(x = y); // Or log the return value directly`  

* return value matches the expression to the right of `=` in the "Meaning" column above
* this means `(x = y)` returns `y`, `(x += y)` returns the sum `x + y`, `(x **= y)` returns the resulting power `x ** y`, and so on
* in the case of logical assignments `(x &&= y)`, `(x || y)`, and `(x ?? = y)`, the return value is that of the logical operation without the assignment, so `x && y`, `x || y`, and `x ?? y` respectively
* return values are always based on the operands' values *before* the operation
* when changing these expressions, each assignment is evaluated **right-to-left**
  * `w = z = x = y` is equivalent to `w = (z = (x = y))` or `x = y; z = y; w = y`
  * `z += x *= y` is equivalent to `z += (x *= y)` or `tmp = x * y; x *= y; z += tmp`(without the `tmp`)
  
## Destructuring
* for complex assignments use descruturing assignments
* this syntax is a JS expression that makes it possible to extract data from arrays or objects using a syntax that mirrors the construction of array and object literals  
* `var foo = ['one', 'two', 'three'];`  

   `// without destructuring`  
   `var one   = foo[0];`  
   `var two   = foo[1];`  
   `var three = foo[2];`  

    `// with destructuring`  
    `var [one, two, three] = foo;`

## Comparison Operators
* compares its operands and returns a logical value based on whether the comparison is true.
* can be numerical, string, logical, or object values
* strings are compared based on standard lexicographical ordering using Unicode values
* if the two operands are not the same type, JS tries to convert them to an appropriate for comparison and this usually results in comparing them numerically
* expectations to type conversion within comparisons involve `===` and `!==` operators which perform equality and inequality comparisons
* these operators don't attempt to convert the operands to compatible types before checking equality
* this describes the comparison operators in terms of this sample:
  * `var var1 = 3;`  
    `var var2 = 4;`  
