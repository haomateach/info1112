

# INFO 1112 Assignment 4

Q. Design a `Student`class that has the following members [30 points]:
- A member variable for the name of the student (a string) [2 points]
- A member variable for the year that the student was enrolled (a string) [2 points]
- A constructor and a destructor [10 points] and appropriate accessors and mutators [10 points]
- A virtual print function that displays the student's name and the year he/she was enrolled [6 points].

Design a `KpuStudent` class that is derived from the `Student` class [30 points]. The `KpuStudent` class should have the following members:
- A member variable for the campus location (a string, could be "Surrey", "Richmond" or "Langley") [4  points]
- A constructor and a destructor [10 points] and appropriate accessors and mutators [10 points]
- A print function that overrides the print function in the base class. The `KpuStudent` class’s print function should display only the student's name and his/her campus location. [6 points]

Design a `HogwartsStudent` class that is derived from the `Student` class [30 points]. The `HogwartsStudent` class should have the following members:
- A member variable for the house affiliation of the student (a string, could be "Hufflepuff", "Ravenclaw", "Gryffindor" or "Slytherin"). [4 points]
- A constructor and a destructor [10 points] and appropriate accessors and mutators [10 points].
- A print function that overrides the print function in the base class. The `HogwartsStudent` class’s print function should display only the student’s name and the student's house affiliation [6 points]. 

Demonstrate the classes in a program that has an array of `Student` pointers [10 points]. 

The array elements should be initialized with the addresses of dynamically allocated `Student` ,`KpuStudent` , and `HogwartsStudent` objects [5 points]. (See Program 15-14 on Page with Page No. 937  of the uploading reading task , lines 17 through 22, for an
example of how to do this.) The program should then step through the array, calling each object’s print function [5 points].



