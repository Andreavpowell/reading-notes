# Programming with JavaScript

## Control Flow
* the order in which the computer executes statements in a script
* run in order top to bottom unless the computer comes across control structures like conditionals (`if...else`) or loops
* control structures can dictate complex flows of processing even within just a few lines

## JavaScript Functions
* a block of code for a particular task
* is executed when something "calls it"

### Function Syntax
* function - `function` followed by a name then ()
* can contain letters, digits, _, and $ (same as variables) 
* the () may contain parameter names separated by commas (`parameter1, parameter2, ...`).
* code to be executed by the function is in {}
* function arguments are the values recieved by the function when it is invoked
* the arguments (parameters) behave as local variables
* function is the samae as a procedure or subroutine in other languages

### Function Invocation
* functions execute when something invokes (calls) it
  * when an event occurs (user clicks a button)
  * when it's invoked from JS code (invoked)
  * automatically (self invoked)

### Function Return
* when js reaches a `return` the function will stop executing
* if the function is invoked from a statement, JS will return to execute the code after the invoking statement
* functions often compute a return value which is *returned* to the "caller"

### Why Functions?
* reuse code
* use the same code many times with different arguments to produce different results

### Functions used as Variable Values
* functions can be used same as variables in all types of formulas, assignments, and calculations

### Local Variables
* variables within a function become local to the function
* local variables can only be accessed from within the function
* some local variables are created when a function starts and deleted when the function is complete

## JavaScript Operators

### JavaScript Arithmetic Operators
Performs arithmetic on numbers
* `+` - addition
* `-` - subtraction
* `*` - multiplication
* `**` - exponentiation (ES2016)
* `/` - division
* `%` - modulus (division remainder)
* `++` - increment
* `--` - decrement

### JavaScript Assignment Operators
Assigns values to JS variables  
Operator | Example | Same As
-------- | ------- | -------
`=`      | `x = y` | `x = y`
`+=`     | `x += y`| `x = x + y`
`-=`     | `x -= y`| `x = x -y`
`*=`     | `x *= y`| `x = x * y`
`/=`     | `x /= y`| `x = x / y`
`%=`     | `x %= y`| `x = x % y`
`**=`    | `x **= y`| `x = x ** y`

### JavaScript String Operators
* assignment operators can also be used to add (concatenate) strings:   
`let text1 = "My name is ";`  
`text1 += "Andrea Powell";`

### Adding Strings and Numbers
* adding two numbers will return the sum; adding a number and a string will return a string:  
`let x = 5 + 5;`  
`let y = "5" + 5;`  
`let z = "Howdy" + 5;`  
x, y, and z results:  
`10`  
`55`  
`Howdy5`  

### JavaScript Comparison Operators

Operator | Description
-------- | ----------
`==`     | equal to
`====`   | equal value and equal type
`!=`     | not equal
`!==`    | not equal value or equal type
`>`      | greater than
`<`      | less than
`>=`     | greater than or equal to
`<=`     | less than or equal to
`?`      | ternary operator

### JavaScript Logical Operators
Operator | Description
-------- | -----------
`&&`     | logical and
`\|\|`   | logical or
`!`      | logical not  

### JavaScript Type Operators
Operator     | Description
--------     | --------
`typeof`     | returns type of variable
`instanceof` | returns true if an object is an instance of an object type

### JavaScript Bitwise Operators
* works on 32 bits numbers
* any numeric operand in the operation is converted to a 32 bit number
* result is converted back to a JS number  
* below uses 4 bits unsigned examples but js uses 32-bit signed numbers
* in js, `~ 5` will not return `10` it will return `-6`

Operator | Description          | Example  | Same As       | Result | Decimal
-------- | ----------           | -------  | -------       | ------ | -------
`&`      | and                  | `5 & 1`  | `0101 & 0001` | `0001` | `1`
`\|`     | or                   | `5 \| 1` | `0101 \| 0001`| `0101` | `5`
`~`      | not                  | `~5`     | `~0101`       | `1010` | `10`
`^`      | xor                  | `5 ^ 1`  | `0101 ^ 0001` | `0100` | `4`
`<<`     | zero fill left shift | `5 << 1` | `0101 << 1`   | `1010` | `10`
`>>`     | signed right shift   | `5 >> 1` | `0101 >> 1`   | `0010` | `2`
`>>>`    | zero fill right shift| `5 >>> 1`| `0101 >>> 1`  | `0010` | `2`

