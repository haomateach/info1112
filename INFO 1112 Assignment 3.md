# INFO 1112 Assignment 3

Q1.  Rewrite the function below so that so it uses pointers instead of reference variables, and then **demonstrate the function in a complete program**.

``` cpp
int doSomething(int &x, int &y)
{
	int temp = x;
	x = y * 5;
	y = temp * 3;
	return x + y;
}

```

Q2. Write a function that accepts an int array and the array’s size as arguments. The function should create a **copy** of the array, except that the element values should be reversed in the copy. The function should return a pointer to the new array. Demonstrate the function in a complete program.

Hint: 
- Use Dynamic Memory Allocation

- The original array should not be modified. 

  

Q3. Write a class declaration named **Cylinder**  with a private member variable named `radius` and `height` . Write set and get functions to access the `radius` and `height` variables, and a function named `getVolume` that returns the volume of the Cylinder. The volume is calculated as

```
3.14159 * radius * radius * height
```

Use test cases in main function to test your class. 



Q4. Design a `PayRoll` class that has data members for an employee’s hourly pay rate, number of hours worked, and total pay for the week. Write a program with an array of
seven PayRoll objects. The program should ask the user for the number of hours each employee has worked and will then display the amount of gross pay each has earned.

Please conduct Input Validation and do not accept values greater than 60 for the number of hours worked.

  
