
# Review Session for Section 12

## Correction and Clarification

C1. When you define a pointer
``` cpp
int * x
```
or de-reference a pointer
``` cpp
* x
```
, the number of spaces you have in between does not matter. 

C2. The debugger section may be more important than you thought. 

## Review Questions
Q1. Write a statement that displays the address of the variable `count` .


Q2. Write the definition statement for a variable `fltPtr` . The variable should be a pointer to a `float` .


Q3. What is the output of the following code?
``` cpp
int x = 50, y = 60, z = 70;
int *ptr = nullptr;

cout << x << " " << y << " " << z << endl;
ptr = &x;

*ptr *= 10;
ptr = &y;
*ptr *= 5;
ptr = &z;
*ptr *= 2;
cout << x << " " << y << " " << z << endl;
```

Q4. Rewrite the following loop so it uses pointer notation (with the indirection operator) instead of subscript notation.
``` cpp
for (int x = 0; x < 100; x++)
  cout << arr[x] << endl;
```

Q5. Assume `ptr` is a pointer to an `int` and holds the address `12000`. On a system with 4-byte integers, what address will be in ptr after the following statement?
``` cpp
ptr += 10;
```
Q6. Assume pint is a pointer variable. Is each of the following statements valid or invalid? If any is invalid, why?
``` cpp
A) pint++;
B) −−pint;
C) pint /= 2;
D) pint *= 4;
E) pint += x; // Assume x is an int.
```
Q7. Is each of the following definitions valid or invalid? If any is invalid, why?

A) 
``` cpp
int ivar;
int *iptr = &ivar;
```
B) 
``` cpp
int ivar, *iptr = &ivar;
```
C) 
``` cpp
float fvar;
int *iptr = &fvar;
```
D) 
``` cpp
int nums[50], *iptr = nums;
```

E) 
``` cpp
int *iptr = &ivar;
int ivar;
```

Q8. Assuming `arr` is an array of int `s`, will each of the following program segments display “True” or “False”?

A)
``` cpp
if (arr < &arr[1])
  cout << "True";
else
  cout << "False";
```
B) 
``` cpp
if (&arr[4] < &arr[1])
  cout << "True";
else
  cout << "False";
```
C) 
``` cpp
if (arr != &arr[2])
  cout << "True";
else
  cout << "False";
```
D) 
``` cpp
if (arr != &arr[0])
  cout << "True";
else
  cout << "False";
```

Q9. Give an example of the proper way to call the following function:

``` cpp
void makeNegative(int *val)
{
    if (*val > 0)
        *val = −(*val);
}
```

Q10. Complete the following program skeleton. When finished, the program will ask the user for a length (in inches), convert that value to centimeters, and display the
result. You are to write the function convert . ( Note: 1 inch = 2.54 cm. Do not modify function main.)

``` cpp
#include <iostream>
#include <iomanip>
using namespace std;
// Write your function prototype here.
int main()
{
double measurement;
cout << "Enter a length in inches, and I will convert\n";
cout << "it to centimeters: ";
cin >> measurement;
convert(&measurement);
cout << fixed << setprecision(4);
cout << "Value in centimeters: " << measurement << endl;
return 0;
}
//
// Write the function convert here.
//
```
<details>

<summary> Click me to show the code below!</summary>

``` cpp
#include <iostream>
#include <iomanip>
using namespace std;

void convert(double *);

int main(){
	
	double measurement;
	cout << "Enter a length in inches, and I will convert\n";
	cout << "it to centimeters: ";
	cin >> measurement;
	convert(&measurement);
	cout << fixed << setprecision(4);
	cout << "Value in centimeters: " << measurement << endl;
	return 0;
}

void convert(double * ptr ){
	
	*ptr *= 2.54;
	
	
	}

```
</details>
Q11. Look at the following array definition:

``` cpp
const int numbers[SIZE] = { 18, 17, 12, 14 };

```
Suppose we want to pass the array to the function processArray in the following manner:
``` cpp
processArray(numbers, SIZE);
```
Which of the following function headers is the correct one for the `processArray` function?
``` cpp
A) void processArray(const int *arr, int size)
B) void processArray(int * const arr, int size)
```

Q12. Assume `ip` is a pointer to an int . Write a statement that will dynamically allocate an integer variable and store its address in `ip` . Write a statement that will free the
memory allocated in the statement you wrote above.

Q13. Assume `ip` is a pointer to an int . Then, write a statement that will dynamically allocate an array of 500 integers and store its address in `ip` . Write a statement
that will free the memory allocated in the statement you just wrote.

Q14. Each of the following definitions and program segments has errors. Locate as many as you can.

1)
``` cpp
int ptr* = nullptr;
```
2) 
``` cpp
int x, *ptr = nullptr;
&x = ptr;
```
3)
``` cpp
int x, *ptr = nullptr;
*ptr = &x;
```
4) 
``` cpp
int x, *ptr = nullptr;
ptr = &x;
ptr = 100; // Store 100 in x
cout << x << endl;
```
5) 
``` cpp
int numbers[] = {10, 20, 30, 40, 50};
cout << "The third element in the array is ";
cout << *numbers + 3 << endl;
```
6)
``` cpp
int values[20], *iptr = nullptr;
iptr = values;
iptr *= 2;
```
7)
``` cpp
float level;
int fptr = &level;
```

8) 
``` cpp
int *iptr = &ivalue;
int ivalue;
```
