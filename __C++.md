	# Variable types
-   `int` - stores integers (whole numbers), without decimals, such as 123 or -123
-   `double` - stores floating point numbers, with decimals, such as 19.99 or -19.99
-   `char` - stores single characters, such as 'a' or 'B'. Char values are surrounded by single quotes
-   `string` - stores text, such as "Hello World". String values are surrounded by double quotes
-   `bool` - stores values with two states: true or false
---
- A floating point number can also be a scientific number with an "e" to indicate the power of 10:
```c++
float f1 = 35e3;  
double d1 = 12E4;  
cout << f1;  
cout << d1;
```
---
- you can use ASCII values to display certain characters:
```c++
char a = 65, b = 66, c = 67;  
cout << a;  
cout << b;  
cout << c;
```
--- 
Logical operators are used to determine the logic between variables or values:
&&  = Logical and
||  = Logical or
! = Logical not
***
However, `cin` considers a space (whitespace, tabs, etc) as a terminating character, which means that it can only display a single word (even if you type many words):
That's why, when working with strings, we often use the `getline()` function to read a line of text. It takes `cin` as the first parameter, and the string variable as second:
```c++
string fullName;  
cout << "Type your full name: ";  
getline (cin, fullName);  
cout << "Your name is: " << fullName;  
  
// Type your full name: John Doe  
// Your name is: John Doe
```
--- 
Other functions, such as `sqrt` (square root), `round` (rounds a number) and `log` (natural logarithm), can be found in the `<cmath>` header file:
```c++
// Include the cmath library  
#include <cmath>  
  
cout << sqrt(64);  
cout << round(2.6);  
cout << log(2);
```
--- 
A boolean variable is declared with the `bool` keyword and can only take the values `true` or `false`:
```c++
bool isCodingFun = true;  
bool isFishTasty = false;  
cout << isCodingFun;  // Outputs 1 (true)  
cout << isFishTasty;  // Outputs 0 (false)
```
--- 
There is also a short-hand if else, which is known as the **ternary operator** because it consists of three operands. It can be used to replace multiple lines of code with a single line. It is often used to replace simple if else statements:
Instead of writing:
```c++
int time = 20;  
if (time < 18) {  
  cout << "Good day.";  
} else {  
  cout << "Good evening.";  
}
```
You can simply write:
```c++
int time = 20;  
string result = (time < 18) ? "Good day." : "Good evening.";  
cout << result;
```
--- 
## C++ Switch Statements
Use the `switch` statement to select one of many code blocks to be executed.
```c++
switch(_expression_) {  
  case x:  
    _// code block_  
    break;  
  case y:  
    _// code block_  
    break;  
  default:  
    _// code block_  
}
```
---
## The Do/While Loop

The `do/while` loop is a variant of the `while` loop. This loop will execute the code block once, before checking if the condition is true, then it will repeat the loop as long as the condition is true.
```c++
do {  
  _// code block to be executed_}  
while (_condition_);
```
The example below uses a `do/while` loop. The loop will always be executed at least once, even if the condition is false, because the code block is executed before the condition is tested:
```c++
int i = 0;  
do {  
  cout << i << "\n";  
  i++;  
}  
while (i < 5);
```
---
## C++ For Loop

When you know exactly how many times you want to loop through a block of code, use the `for` loop instead of a `while` loop:
```c++
for (_statement 1_; _statement 2_; _statement 3_) {  
  _// code block to be executed_  
}
```
**Statement 1** is executed (one time) before the execution of the code block.

**Statement 2** defines the condition for executing the code block.

**Statement 3** is executed (every time) after the code block has been executed.

The example below will print the numbers 0 to 4:
```c++
for (int i = 0; i < 5; i++) {  
  cout << i << "\n";  
}
```
#### Example explained

Statement 1 sets a variable before the loop starts (int i = 0).

Statement 2 defines the condition for the loop to run (i must be less than 5). If the condition is true, the loop will start over again, if it is false, the loop will end.

Statement 3 increases a value (i++) each time the code block in the loop has been executed.
***
## The foreach Loop
```c++
for (_type variableName_ : _arrayName_) {  
  // code block to be executed  
}
```
```c++
int myNumbers[5] = {10, 20, 30, 40, 50};  
for (int i : myNumbers) {  
  cout << i << "\n";  
}
```
---
## C++ Arrays

Arrays are used to store multiple values in a single variable, instead of declaring separate variables for each value.

To declare an array, define the variable type, specify the name of the array followed by **square brackets** and specify the number of elements it should store:
```c++
string cars[3] = {"Volvo", "BMW", "Ford"}; // Also three arrays
```
## Omit Array Size

In C++, you don't have to specify the size of the array. The compiler is smart enough to determine the size of the array based on the number of inserted values:
```c++
string cars[] = {"Volvo", "BMW", "Ford"}; // Three arrays
```