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
