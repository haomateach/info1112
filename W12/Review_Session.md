# Review Session for Section 19

## Correction and Clarification

Don't force yourself to memorize the syntax of file, stream and I/O operations we learned this week. Just familiarize yourself with them. 

## Review Questions


Q1. How do you use more than one file access flag?

<details>

<summary> Click me to show the answer below!</summary>


Use `|` operator. For example:

```
fstream dataFile;
dataFile.open("info.txt", ios::in | ios::out);
```
This statement opens the file info.txt in both input and output modes. This means data may be written to and read from the file.

Note that, this is not the only solution.
</details>

 

Q2. Assuming that `diskInfo` is an fstream object, write a statement that opens the file `names.dat` for output (write data into the file).


<details>

<summary> Click me to show the answer below!</summary>

```
diskInfo.open("names.dat", ios::out);
```
Note that, this is not the only solution. 
</details>




Q3. Assuming that `diskInfo` is an fstream object, write a statement that opens the file `customers.txt` for output, where all output will be written to the end of the file.



<details>

<summary> Click me to show the answer below!</summary>

```
diskInfo.open("customers.txt", ios::out | ios::app );
```

Note that, this is not the only solution. 
</details>



Q4. What will the following program display on the screen?
``` cpp
#include <iostream>
#include <fstream>
#include <string>
using namespace std;
int main()
{
  fstream inFile("input.txt", ios::in);
  string item;
  inFile >> item;
  while (inFile)
  {
  cout << item << endl;
  inFile >> item;
  }
  inFile.close();
  return 0;
}
```
Assume the `input.txt` file contains 

```
Run Spot run
See Spot run

```



<details>

<summary> Click me to show the answer below!</summary>

```
Run
Spot
run
See
Spot
run
```

Explanation: `>>` will collect data from the file  `input.txt` through the `inFile` stream, and whenever `>>` run into space, it will stop collecting. 

</details>



Q5. Describe the difference between reading a file with the `>>` operator and the `getline` function.

<details>

<summary> Click me to show the answer below!</summary>

`>>` operator only consider the space character as a delimiter and will not read it from a file, while `getline` will collect text from a file line by line including the space character. 


</details>

Q6. What will be stored in the file out.txt after the following program runs?

```cpp
#include <iostream>
#include <fstream>
#include <iomanip>
using namespace std;
int main()
{
  const int SIZE = 5;
  ofstream outFile("out.txt");
  double nums[SIZE] = {100.279, 1.719, 8.602, 7.777, 5.099};
  outFile << fixed << setprecision(2);
  for (int count = 0; count < 5; count++)
  {
  outFile << setw(8) << nums[count];
  }
  outFile.close();
  return 0;
}


```

<details>

<summary> Click me to show the answer below!</summary>

```
  100.28    1.72    8.60    7.78    5.10
```

</details>



