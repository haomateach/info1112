
# Review Session for Section 7, 8 and 9 (C76-C81)

## Correction and Clarification
- In Component 55 of Section 7, there is an error in the code. The code examples in this video show the declaration of `days_in_year` as follows: 
```cpp
const double days_in_year {365};
``` 
This is incorrect. The type of `days_in_year` should be `int` since it is being used to declare the size of the array `hi_temperatures`.The correct declaration should be:
```cpp
const int days_in_year {365};
```

- `enum` type is introduced in Component 80 and has not been explained in detail. You can refer to https://www.programiz.com/cpp-programming/enumeration


<!---
- Summary of the process of translating a C++ source file into an executable file 
![alt text](./img/theprocess.PNG "Logo Title Text 1")

-->

## Review Questions
Q1. Assume `value` is an integer variable. If the user enters 3.14 in response to the
following programming statement, what will be stored in value ?

`cin >> value;`

A) 3.14

B) 3

C) 0

D) Nothing. An error message is displayed.

Q2. The following program will run, but the user will have difficulty understanding what to do. How would you improve the program?
``` cpp
// This program multiplies two numbers and displays the result.
#include <iostream>
using namespace std;
int main()
{
double first, second, product;
cin >> first >> second;
product = first * second;
cout << product;
return 0;
}
```

Q3. What's the value of the following expression: `5 + 19 % 3 − 1`

Q4. Complete the following program skeleton so it displays the volume of a cylindrical fuel tank. The formula for the volume of a cylinder is

Volume = π* r^2 *h

where

π is 3.14159

r is the radius of the tank

h is the height of the tank

``` cpp
#include <iostream>
#include <cmath>
using namespace std;
int main()
{
  double volume, radius, height;
  cout << "This program will tell you the volume of\n";
  cout << "a cylinder-shaped fuel tank.\n";
  cout << "How tall is the tank? ";
  cin >> height;
  cout << "What is the radius of the tank? ";
  cin >> radius;
  // You must complete the program.
}

```

Q5. Assume the following variable definitions:
```
int a = 5, b = 12;
double x = 3.4, z = 9.1;
```
What are the values of the following expressions?
``` cpp
A) b / a
B) x * a
C) static_cast<double>(b / a)
D) static_cast<double>(b) / a
E) b / static_cast<double>(a)
F) static_cast<double>(b) / static_cast<double>(a) 
G) b / static_cast<int>(x)
H) static_cast<int>(x) * static_cast<int>(z)
I) static_cast<int>(x * z) 
J) static_cast<double>(static_cast<int>(x) * static_cast<int>(z))
```

Q6. Complete the following program skeleton so it asks the user to enter a character. Store the character in the variable `letter`. Use a type cast expression with the
variable in a cout statement to display the character’s ASCII code on the screen.
``` cpp
#include <iostream>
using namespace std;

int main()
{
char letter;
// Finish this program
// as specified above.
return 0;
}
```
Q7. What will the following program display?
``` cpp
#include <iostream>
using namespace std;
int main()
{
  int integer1, integer2;
  double result;
  integer1 = 19;
  integer2 = 2;
  result = integer1 / integer2;
  cout << result << endl;
  result = static_cast<double>(integer1) / integer2;
  cout << result << endl;
  result = static_cast<double>(integer1 / integer2);
  cout << result << endl;
  return 0;
}
```
 
Q8.Write statements using combined assignment operators to perform the following:
```
A) Add 6 to x .
B) Subtract 4 from amount .
C) Multiply y by 4.
D) Divide total by 27.
E) Store in x the remainder of x divided by 7.
F) Add y * 5 to x .
G) Subtract discount times 4 from total .
H) Multiply increase by salesRep times 5.
I) Divide profit by shares minus 1000.
```
Q9. What will the following program display?
``` cpp
#include <iostream>
using namespace std;
int main ()
{
int a = 0, b = 2, x = 4, y = 0;
cout << (a == b) << endl;
cout << (a != y) << endl;
cout << (b <= x) << endl;
cout << (y > a) << endl;
return 0;
}
```
Q10. Write an if statement that performs the following logic: if the variable `x` is equal to 20, then assign 0 to the variable `y`.

Q11. Write an if statement that performs the following logic: if the variable `sales` is greater than 50,000, then assign 0.25 to the `commissionRate` variable, and
assign 250 to the `bonus` variable.

Q12. The following code segment is syntactically correct, but it appears to contain a logic error. Can you find the error?
``` cpp
if (interestRate > .07)
  cout << "This account earns a $10 bonus.\n";
  balance += 10.0;
```

Q13. TRUE or FALSE: The following if/else statements cause the same output to display.

A) 
``` cpp
if (x > y)
  cout << "x is the greater.\n";
else
  cout << "x is not the greater.\n";
```
B) 
``` cpp
if (y <= x)
  cout << "x is not the greater.\n";
else
  cout << "x is the greater.\n";
```
Q14. The following code is used in a bookstore program to determine how many discount coupons a customer gets. What will be the output if the `numBooks` is 1, 3, 4, 5 or 10?
``` cpp
int numBooks, numCoupons;
cout << "How many books are being purchased? ";
cin >> numBooks;
if (numBooks < 1)
  numCoupons = 0;
else if (numBooks < 3)
  numCoupons = 1;
else if (numBooks < 5)
  numCoupons = 2;
else
  numCoupons = 3;
  cout << "The number of coupons to give is " << numCoupons << endl;
```
Q15. Evaluate the following expressions assuming the variables a = 2 , b = 4 , and c = 6 . 
``` cpp
a == 4 || b > 2 
6 <= c && a > 3
1 != b && c != 3 
a >= -1 || a <= b 
!(a > 2)
```
Q16. Write an if statement that prints the message “The number is valid” if the variable `speed` is within the range 0 through 200.

Q17. Rewrite the following if/else statements as conditional expressions:

A) 
```cpp 
if (x > y)
  z = 1;
else
  z = 20;
```
B) 
```cpp
if (temp > 45)
  population = base * 10;
else
  population = base * 2;
```
Q18. The following statements use conditional expressions. Rewrite each with an if/else statement.
```
A) j = k > 90 ? 57 : 12;
B) factor = x >= 10 ? y * 22 : y * 35;
C) total += count == 1 ? sales : count * sales;
D) cout << (((num % 2) == 0) ? "Even \ n" : "Odd\n");
```

Q19. Explain why you cannot convert the following if/else if statement into a switch statement.

```cpp
if (temp == 100)
  x = 0;
else if (population > 1000)
  x = 1;
else if (rate < .1)
  x = −1;
```
Q20. What is wrong with the following switch statement?

``` cpp
switch (temp)
{
case temp < 0 : cout << "Temp is negative.\n";
break;
case temp == 0: cout << "Temp is zero.\n";
break;
case temp > 0 : cout << "Temp is positive.\n";
break;
}
```
Q21. Complete the following program skeleton by writing a switch statement that displays “one” if the user has entered 1, “two” if the user has entered 2, and
“three” if the user has entered 3. If a number other than 1, 2, or 3 is entered, the program should display an error message.
``` cpp
#include <iostream>
using namespace std;
int main()
{
int userNum;
cout << "Enter one of the numbers 1, 2, or 3: ";
cin >> userNum;
//
// Write the switch statement here.
//
return 0;
}
```
Q22. What's the code output? 

``` cpp
// This program uses two variables with the name number.
#include <iostream>
using namespace std;

int main()
{
// Define a variable named number.
  int number;

  cout << "Enter a number greater than 0: ";
  cin >> number;
  if (number > 0)
  {
     int number; // Another variable named number.
     cout << "Now enter another number: ";
     cin >> number;
     cout << "The second number you entered was "<< number << endl;
  }
  cout << "Your first number was " << number << endl;
  return 0;
}
```

Q23. What will the following program segments display?
```cpp
A) 
x = 2;
y = x++;
cout << x << y;
B)
x = 2;
y = ++x;
cout << x << y;
C)
x = 2;
y = 4;
cout << x++ << −−y;
D)
x = 2;
y = 2 * x++;
cout << x << y;

E)
x = 99;
if (x++ < 100)
  cout "It is true!\n";
else
  cout << "It is false!\n";
F) 
x = 0;
if (++x)
  cout << "It is true!\n";
else
  cout << "It is false!\n";
```

Q24. Define the following arrays:

```
A) empNums , a 100-element array of int
B) payRates , a 25-element array of float
C) miles , a 14-element array of long
```

Q25. Define the following vectors:

```
A) empNums , a 100-element vector of int
B) payRates , a 25-element vector of float
C) miles , a 14-element vector of long
```

Q26. Define the following arrays:
```
A) ages , a 10-element array of int s initialized with the values 5, 7, 9, 14, 15, 17, 18, 19, 21, and 23.
B) temps , a 7-element array of float s initialized with the values 14.7, 16.3, 18.43, 21.09, 17.9, 18.76, and 26.7.
C) alpha , an 8-element array of char s initialized with the values ‘J’, ‘B’, ‘L’, ‘A’, ‘*’, ‘$’, ‘H’, and ‘M’.
```

Q27. Define the following vectors:
```
A) ages , a 10-element vector of int s initialized with the values 5, 7, 9, 14, 15, 17, 18, 19, 21, and 23.
B) temps , a 7-element vector of float s initialized with the values 14.7, 16.3, 18.43, 21.09, 17.9, 18.76, and 26.7.
C) alpha , an 8-element vector of char s initialized with the values ‘J’, ‘B’, ‘L’, ‘A’, ‘*’, ‘$’, ‘H’, and ‘M’.
```

Q28. Given the following array definition:
```
int values[] = {2, 6, 10, 14};
```
What does each of the following display?
```
A) cout << values[2];
B) cout << ++values[0];
C) cout << values[1]++;
D) x = 2; cout << values[++x];
```
Q29. Define a two-dimensional array of int s named grades . It should have 3 rows and 2 columns.

Q30. Define a two-dimensional vector of int s named grades.

Q31. Rewrite the following program. Use a switch statement instead of the if/else if statement.
``` cpp
#include <iostream>
using namespace std;
int main()
{
  int selection;
  cout << "Which formula do you want to see?\n\n";
  cout << "1. Area of a circle\n";
  cout << "2. Area of a rectangle\n";
  cout << "3. Volume of a cylinder\n"
  cout << "4. None of them!\n";
  cin >> selection;
  if (selection == 1)
    cout << "Pi times radius squared\n";
  else if (selection == 2)
    cout << "Length times width\n";
  else if (selection == 3)
    cout << "Pi times radius squared times height\n";
  else if (selection == 4)
    cout << "Well okay then, good bye!\n";
  else
    cout << "Not good with numbers, eh?\n";
  return 0;
}
```
Q32. Write a C++ program to enable the conversion between US dollars and Canadian Dollars. The program will first ask for user input to decide whether the user would like to convert USD to CAD, or the other way around. Then the program will ask for user input to indicate the amount of money in the original currency, and then output the converted amount in the targeted currency. 

Examples:

```
Please enter 0 to indicate USD->CAD conversion, or enter 1 to indicate CAD->USD conversion: 0
Please enter the amount of USD dollars: XXX
They can be converted to YYY CAD.
```
```
Please enter 0 to indicate USD->CAD conversion, or enter 1 to indicate CAD->USD conversion: 1
Please enter the amount of CAD dollars: XXX
They can be converted to YYY USD.
```

Here XXX represent the numerical input from user, and YYY represent the calculated numerical value by the program. You can assume **1 United States Dollar equals 1.32 Canadian Dollar** in this question. 
