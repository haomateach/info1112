Q1. Convert the following pseudocode to C++ code. Be sure to define the appropriate variables.
- Store 20 in the speed variable.
- Store 10 in the time variable.
- Multiply speed by time and store the result in the distance variable.
- Display the contents of the distance variable.

Q2. Convert the following pseudocode to C++ code. Be sure to define the appropriate variables.
- Store 172.5 in the force variable.
- Store 27.5 in the area variable.
- Divide force by area and store the result in the pressure variable.
- Display the contents of the pressure variable.

Q3. Rewrite the following program. Use a switch statement instead of the if/else if statement.

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

Q4. Write a C++ program to enable the conversion between US dollars and Canadian Dollars. The program will first ask for user input to decide whether the user would like to convert USD to CAD, or the other way around. Then the program will ask for user input to indicate the amount of money in the original currency, and then output the converted amount in the targeted currency. 

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

