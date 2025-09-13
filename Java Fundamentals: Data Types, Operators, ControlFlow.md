### Data Types
- Java = Statically-typed language (every var must have a declared data type)
- Data Types define what kind of values the variable can hold and operations that can be performed on it.
#### Primitive Data Types
- They store actual values directly in memory. 
- - `byte` = An 8-bit signed integer. -128 -> 127. To save memory for storing in large arrays.
- - `short` = An 16-bit signed integer. -32768 -> 32767, less commonly
-- `int` = An 32-bit signed integer. -2bn -> 2bn. Most commonly used integer type.
- - `long` = A 64-bit signed integer. -9,18zeroes ->9,18zeros. Always append 'L' or 'l' to a `long` literal to indicate its a `long` value
- - `float` = A 32-bit single-precision floating-point number. Append 'F' or 'f' to a `float` literal.
- - `double` = 64-bit double-precision floating-point number. 
- - `char` = 16-bit Unicode character.
- - `boolean` = Used for logical operations, `true` or `false`

#### Reference Data Types
- Do not store actual value in memory, they hold a ref.. to the memory location where the object is stored.
- Classes: Blueprints for creating objects
- Interfaces: Contracts that define set of methods which must be implemented by a class.
- - Arrays: Collection of elements of same data type

#### Type Conversion (Casting)
- Implicit Conversion (Widening): Automatic from small to large 
```java
int x = 10;
long y = x;
double z = x;
```

- Explicit Conversion (Narrowing):
```java
double a = 10.09;
int b = (int) a;
long bigValue = 99999L;
int smallValue = (int) bigValue;
//Can result into loss of data or unexpected results
```

### Operators in Java

#### Arithmetic Operators

##### Basic
- `+`
- `-`
- `*`
- `/`
- `%` => Remainder of the division

##### Relational Operators
- `==`
- `!=`
- `>`
- `<`
- `<=`
- `>=`

##### Logical Operators
- `&&`
- `||`
- `!`

##### Assignment operators
- =
- +=
- -=
- *=
- /=
- %= 

##### Increment and Decrement Operators
- ++
- `--`

##### Bitwise Operators
- Perform operations on individual bits of integers. Less commonly used in app development but imp in low-level programming or when optimizing for performance.

- &
- |
- ^
- ~
- <<
- `>>`
- `>>>`

##### Ternary Operator
- cond ? ifTrueExp : ifFalseExp

##### Operator Precedence
- Operators have a precedence which determine the order in which they are evaluated.
- Use parenthesis to override the default precedence make code more readable

### Control Flow
- `if-else` statement
- `switch` statement  -> execute one of the several blocks based on the value of variable.
```java
int day = 3;
String dayName;
switch(day) {
    case 1:
        dayName = "Monday";
        break;
    case 2:
        dayName = "Tuesday";
        break;
    default:
        dayName="U
        nknown";
}
```
Don't forget break at each case block, the execution will "fall through" to the next `case`

#### Looping Statements
- `for` loop -> Execute a block n number of times
- `while` loop -> Execute a block as long a cond is `true`
- `do-while` loop -> Execute block atleast once.
- `for-each loop`: Iterates over an array or collection

#### Jump statements
- `break` statement: Terminate the current loop or `switch` statement
- `continue` statement: Skip the rest of the current iteration of the loop and process to next iteration
- `return`: Exit the current method