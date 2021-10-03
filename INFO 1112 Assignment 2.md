
# INFO 1112 Assignment 2

The questions below are relevant to Section 9，10 and 11. 



Q1. 

``` cpp

// This program finds the average time spent programming by a student
// each day over a three day period.

// PLACE YOUR NAME HERE

#include <iostream>
using namespace std;

int main()
{
	int numStudents;
	float numHours, total, average;
	int student, day = 0;	// these are the counters for the loops

	cout << "This program will find the average number of hours a day"
		 << " that a student spent programming over a long weekend\n\n";
	cout << "How many students are there ?" << endl << endl;
	cin >> numStudents;

	for (student = 1; student <= numStudents; student++)
	{
		total = 0;

		for (day = 1; day <= 3; day++)
		{
			cout << "Please enter the number of hours worked by student "
				 << student << " on day " << day << "." << endl;
			cin >> numHours;

			total = total + numHours;
		}

		average = total / 3;

		cout << endl;
		cout << "The average number of hours per day spent programming by "
			 << "student " << student << " is " << average
			 << endl << endl << endl;
	}

	return 0;
}
```
 Note that the inner loop of this program is always executed exactly three times—once for each day of the long weekend. Modify the code so that the inner loop iterates n times, where n is a positive integer input by the user. In other words, let the user decide how many days to consider just as they choose how many students to consider.

Sample Run:
```
This program will find the average number of hours a day that a student spent programming over a long weekend

How many students are there?
2
Enter the number of days in the long weekend
2

Please enter the number of hours worked by student 1 on day 1
4

Please enter the number of hours worked by student 1 on day 2
6

The average number of hours per day spent programming by student 1 is 5


Please enter the number of hours worked by student 2 on day 1
9

Please enter the number of hours worked by student 2 on day 2
13

The average number of hours per day spent programming by student 2 is 11
```

Q2. Modify the program from Q1 so that it also finds the average number of hours per day that a given student studies biology as well as programming. For each given student include two prompts, one for each subject. Have the program print out which subject the student, on average, spent the most time on.

Q3. Using **C++ style string** to write a program that reads a sentence as input and converts each word of the sentence following the rule below:

- For every word in the sentence, the first letter is relocated the end of the word.
- Then append the string “KPU” to the word. 

More requirements:
- All letters in the output should be uppercase. 

More assumptions:
- The input sentence contains no non-alphabetic letters

Sample Run:

```
Please enter the original sentence: i LOVE to program
Translated: IKPU OVELKPU OTKPU ROGRAMPKPU
```

Q4. In a program, write a function that accepts three arguments: an array, the size of the array, and a number `n` . Assume that the array contains integers. The function should display all of the numbers in the array that are greater than the number `n`. Write two test cases in the `main` function to verify the function you wrote. 

Q5. Write a function that accept one positive integer argument and returns true if the argument is a prime number, or false otherwise. Write two test cases in the `main` function to verify the function you wrote. 

For the definition of prime number, you can refer to the wikipedia: https://en.wikipedia.org/wiki/Prime_number

Further explanation of the prime number: 
- 7 is prime because it can **only** be evenly divided by 1 and 7.  
- 4 is not prime because it can be divided evenly by 1, 2, 4. 
