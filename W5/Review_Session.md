
# Review Session for Section 11

## Correction and Clarification

Nothing to correct and clarify this week from the videos. This section is very important and not easy. Post questions in the discussion forum if you want to further clarification on certain topics.


## Review Questions

Q1. Is the following a function header or a function call?

``` cpp
calcTotal();
```
Q2. Is the following a function header or a function call?

``` cpp
void showResults()
```

Q3.  What will the output of the following program be if the user enters 10?
``` cpp
#include <iostream>
using namespace std;
void func1()
{
  cout << "Able was I\n";
}
void func2()
{
  cout << "I saw Elba\n";
}
int main()
{
  int input;
  cout << "Enter a number: ";
  cin >> input;
  if (input < 10)
  {
      func1();
      func2();
  }
  else
  {
    func2();
    func1();
  }
  return 0;
}
```
Q4.Indicate which of the following is the function prototype, the function header, and the function call:
``` cpp
void showNum(double num)
void showNum(double);
showNum(45.67);
```
Q5. Write a function named `timesTen` . The function should have an integer parameter named `number` . When `timesTen` is called, it should display the product of number times ten. ( Note : just write the function. Do not write a
complete program.)

<details>

<summary> Click me to show the code below!</summary>

``` cpp
//Write a function named timesTen . 
//The function should have an integer parameter named number . 
//When timesTen is called, it should display the product of number times ten. 


#include <iostream>
using namespace std;

void timesTen(int);



int main()
{
  int inputNumber{};
  cout << "Enter a number plz:\n";
  cin >> inputNumber;
  timesTen(inputNumber);
	
	
  return 0;
}

void timesTen(int number){
	
	
	cout << number*10 << endl;
	
	
}

```
</details>

Q6. What is the output of the following program?
``` cpp
#include <iostream>
using namespace std;
void showDouble(int); // Function prototype
int main()
{
  int num;
  for (num = 0; num < 10; num++)
    showDouble(num);
  return 0;
}
// Definition of function showDouble.
void showDouble(int value)
{
  cout << value << "\t" << (value * 2) << endl;
}
```
Q7. What is the output of the following program?
``` cpp
#include <iostream>
using namespace std;
void func1(double, int); // Function prototype
int main()
{
  int x = 0;
  double y = 1.5;
  cout << x << " " << y << endl;
  func1(y, x);
  cout << x << " " << y << endl;
  return 0;
}

void func1(double a, int b)
{
  cout << a << " " << b << endl;
  a = 0.0;
  b = 10;
  cout << a << " " << b << endl;
}
```

Q8. The following program skeleton asks for the number of hours you’ve worked and your hourly pay rate. It then calculates and displays your wages. The
function showDollars , which you are to write, formats the output of the wages.

``` cpp
#include <iostream>
using namespace std;
void showDollars(double); // Function prototype
int main()
{
  double payRate, hoursWorked, wages;
  cout << "How many hours have you worked? "
  cin >> hoursWorked;
  cout << "What is your hourly pay rate? ";
  cin >> payRate;
  wages = hoursWorked * payRate;
  showDollars(wages);
  return 0;
}
// You must write the definition of the function showDollars
// here. It should take one parameter of the type double.
// The function should display the message "Your wages are $"
// followed by the value of the parameter. It should be displayed
// with 2 places of precision after the decimal point, in fixed
// notation, and the decimal point should always display.
```

<details>

<summary> Click me to show the code below!</summary>

``` cpp
void showDollars(double dollars){
	
	cout <<fixed<<setprecision(2);
	cout<< "Your wages are $" << dollars<<endl;
	}

```
</details>


Q9. What is the difference between a static local variable and a global variable?


Q10. What is the output of the following program?

``` cpp
#include <iostream>
using namespace std;
void myFunc(); // Function prototype
int main()
{
int var = 100;
cout << var << endl;
myFunc();
cout << var << endl;
return 0;
}
// Definition of function myFunc
void myFunc()
{
int var = 50;
cout << var << endl;
}
```

Q11. What is the output of the following program?

``` cpp
#include <iostream>
using namespace std;
void showVar(); // Function prototype
int main()
{
  for (int count = 0; count < 10; count++)
  showVar();
  return 0;
}
// Definition of function showVar
void showVar()
{
  static int var = 10;
  cout << var << endl;
  var++;
}
```

Q12. What kinds of values may be specified as default arguments?

<details>
<summary>Click to show the answer!</summary>
	Trailing parameters. If a parameter has a default value, every parameter that comes after MUST have default values. 
</details>


Q13. Write the prototype and header for a function called `compute` . The function should have three parameters: an `int` , a `double` , and a `long` (not necessarily
in that order). The int parameter should have a default argument of 5, and the long parameter should have a default argument of 65536. The double parameter should not have a default argument.

Q14. Write the prototype and header for a function called `calculate` . The function should have three parameters: an `int` , a reference to a `double` , and a `long` (not necessarily in that order.) Only the int parameter should have a default
argument, which is 47.

Q15. What is the output of the following program?

``` cpp
#include <iostream>
using namespace std;
void test(int = 2, int = 4, int = 6);

int main()
{
  test();
  test(6);
  test(3, 9);
  test(1, 5, 7);
  return 0;
}
void test (int first, int second, int third)
{
  first += 3;
  second += 6;
  third += 9;
  cout << first << " " << second << " " << third << endl;
}
```

Q16. The following program asks the user to enter two numbers. What is the output of the program if the user enters 12 and 14?

``` cpp
#include <iostream>
using namespace std;
void func1(int &, int &);
void func2(int &, int &, int &);
void func3(int, int, int);
int main()
{
int x = 0, y = 0, z = 0;
cout << x << " " << y << " " << z << endl;
func1(x, y);
cout << x << " " << y << " " << z << endl;
func2(x, y, z);
cout << x << " " << y << " " << z << endl;
func3(x, y, z);
cout << x << " " << y << " " << z << endl;
return 0;
}
void func1(int &a, int &b)
{
  cout << "Enter two numbers: ";
  cin >> a >> b;
}
void func2(int &a, int &b, int &c)
{
  b++;
  c−−;
  a = b + c;
}
void func3(int a, int b, int c)
{
  a = b − c;
}
```

Q17. What is the output of the following program?

```cpp
#include <iostream>
using namespace std;
int manip(int);
int manip(int, int);
int manip(int, double);
int main()
{
  int x = 2, y= 4, z;
  double a = 3.1;
  z = manip(x) + manip(x, y) + manip(y, a);
  cout << z << endl;
  return 0;
}
int manip(int val)
{
  return val + val * 2;
}
int manip(int val1, int val2)
{
  return (val1 + val2) * 2;
}
int manip(int val1, double val2)
{
  return val1 * static_cast<int>(val2);
}
```
Q18. Design a recursive function to calculate the summation of all integers from 1 to `n` (`n`>=1).

Q19. When an array name is passed to a function, what is actually being passed?

Q20. When used as function arguments, are arrays passed by value?

Q21. What is the output of the following program? 
``` cpp

#include <iostream>
using namespace std;
// Function prototypes
void fillArray(char [], int);
void showArray(const char [], int);
int main ()
{
  const int SIZE = 8;
  char prodCode[SIZE] = {'0', '0', '0', '0', '0', '0', '0', '0'};
  fillArray(prodCode, SIZE);
  showArray(prodCode, SIZE);
  return 0;
}
// Definition of function fillArray.
// (Hint: 65 is the ASCII code for 'A')
void fillArray(char arr[], int size)
{
char code = 65;
  for (int k = 0; k < size; code++, k++)
      arr[k] = code;
}
// Definition of function showArray.
void showArray(const char codes[], int size)
{
  for (int k = 0; k < size; k++)
      cout << codes[k];
  cout << endl;
}
```

Q22. The following program skeleton, when completed, will ask the user to enter 10 integers, which are stored in an array. The function avgArray , which you must
write, is to calculate and return the average of the numbers entered.
``` cpp
#include <iostream>
using namespace std;
// Write your function prototype here
int main()
{
  const int SIZE = 10;
  int userNums[SIZE];
  cout << "Enter 10 numbers: ";
  for (int count = 0; count < SIZE; count++)
  {
    cout << "#" << (count + 1) << " ";
    cin >> userNums[count];
  }
  cout << "The average of those numbers is ";
  cout << avgArray(userNums, SIZE) << endl;
  return 0;
}
//
// Write the function avgArray here.
//
```
