
# Review Session for Section 13

## Correction and Clarification
C1. You may wonder about the 7:25 of Section 150. You can refer to

https://www.udemy.com/course/beginning-c-plus-plus-programming/learn/lecture/9535596#questions/8327306

## Review Questions

Q1. True or False: You must declare all private members of a class before the public members.

<details>

<summary> Click me to show the answer below!</summary>

False. There is no rule requiring you to declare private members before public members. For example, the `Rectangle` class could be declared as follows:
``` cpp
class Rectangle
{
public:
  void setWidth(double);
  void setLength(double);
  double getWidth() const;
  double getLength() const;
  double getArea() const;
private:
  double width;
  double length;
};
```
In addition, it is not required that all members of the same access specification be declared in the same place. Here is yet another declaration of the `Rectangle` class.
``` cpp
class Rectangle
{
private:
  double width;
public:
  void setWidth(double);
  void setLength(double);
  double getWidth() const;
  double getLength() const;
  double getArea() const;
private:
  double length;
};
```
</details>

Q2. Assume that `RetailItem` is the name of a class, and the class has a void member function named `setPrice` , which accepts a `double` argument. Which of the following
shows the correct use of the scope resolution operator in the member function definition?

A) `RetailItem::void setPrice(double p)`

B) `void RetailItem::setPrice(double p)`

<details>

<summary> Click me to show the answer below!</summary>

B)

</details>


Q3. An object’s private member variables are accessed from outside the object by

A) public member functions

B) any function

C) the dot operator

D) the scope resolution operator

<details>

<summary> Click me to show the answer below!</summary>

A) public member functions

</details>


Q4.  Assume that `RetailItem` is the name of a class, and the class has a void member function named `setPrice` , which accepts a `double` argument. If `soap` is an
instance of the `RetailItem` class, which of the following statements properly uses the `soap` object to call the `setPrice` member function?

A) `RetailItem::setPrice(1.49);`

B) `soap::setPrice(1.49);`

C) `soap.setPrice(1.49);`

D) `soap:setPrice(1.49);`

<details>

<summary> Click me to show the answer below!</summary>

C) `soap.setPrice(1.49);`

</details>


Q5. Briefly describe the purpose of a constructor.

<details>

<summary> Click me to show the answer below!</summary>


A constructor is a member function that has the same name as the class. It is automatically called when the object is created in memory, or instantiated. It is helpful to think of constructors as initialization routines. They

</details>


Q6. Briefly describe the purpose of a destructor.

<details>

<summary> Click me to show the answer below!</summary>

Destructors are member functions with the same name as the class, preceded by a tilde character (~). For example, the destructor for the `Rectangle` class would be named `~Rectangle`. Destructors are automatically called when an object is destroyed. In the same way that constructors set things up when an object is created, destructors perform shutdown procedures when the object goes out of existence. For example, a common use of destructors is to free memory that was dynamically allocated by the class object.

In addition to the fact that destructors are automatically called when an object is destroyed, the following points should be mentioned:
- Like constructors, destructors have no return type.
- Destructors cannot accept arguments, so they never have a parameter list.

</details>


Q7. A member function that is never declared with a return data type, but that may have arguments is

A) The constructor

B) The destructor

C) Both the constructor and the destructor

D) Neither the constructor nor the destructor

<details>

<summary> Click me to show the answer below!</summary>

A)

</details>

Q8. A member function that is never declared with a return data type and can never have arguments is

A) The constructor

B) The destructor

C) Both the constructor and the destructor

D) Neither the constructor nor the destructor

<details>

<summary> Click me to show the answer below!</summary>

B)

</details>


Q9. Destructor function names always start with

A) A number

B) Tilde character ( ~ )

C) A data type name

D) None of the above

<details>

<summary> Click me to show the answer below!</summary>

B)

</details>


Q10. A constructor that requires no arguments is called

A) A default constructor

B) An overloaded constructor

C) A null constructor

D) None of the above


<details>

<summary> Click me to show the answer below!</summary>

A)

When a constructor doesn’t accept arguments, it is known as the `default constructor`. If a constructor has default arguments for all its parameters, it can
be called with no explicit arguments. It then becomes the default constructor. For example, suppose the constructor for the Sale class had been written as the following:
``` cpp
Sale(double cost = 0.0, double rate = 0.05)
{ itemCost = cost;
  taxRate = rate; }
```
This constructor has default arguments for each of its parameters. As a result, the constructor can be called with no arguments, as shown here:
```Sale itemSale;```
This statement defines a `Sale` object. No arguments were passed to the constructor, so the default arguments for both parameters are used. Because this constructor can be called with no arguments, it is the default constructor.

**When all of a class’s constructors require arguments, then the class does not have a default constructor. In such a case you must pass the required arguments to the constructor when creating an object. Otherwise, a compiler error will result.**


</details>



Q11. TRUE or FALSE: Constructors are never declared with a return data type.

<details>

<summary> Click me to show the answer below!</summary>

True

</details>

Q12. TRUE or FALSE: Destructors are never declared with a return type.

<details>

<summary> Click me to show the answer below!</summary>

True

</details>


Q13. TRUE or FALSE: Destructors may take any number of arguments.

<details>

<summary> Click me to show the answer below!</summary>

False

</details>


Q14. What will the following program display on the screen?
``` cpp
#include <iostream>
using namespace std;
class Package
{
  private:
    int value;
  public:
    Package()
    { value = 7; cout << value << endl; }
    Package(int v)
    { value = v; cout << value << endl; }
    ~Package()
    { cout << value << endl; }
  };
int main()
{
  Package obj1(4);
  Package obj2;
  Package obj3(2);
  return 0;
}
```

<details>

<summary> Click me to show the answer below!</summary>


4

7

2

2

7

4

</details>


Q15. In your answer for Q14. indicate for each line of output whether the line is displayed by constructor #1, constructor #2, or the destructor.

<details>

<summary> Click me to show the answer below!</summary>

4   Constructor #2

7   Constructor #1

2   Constructor #2

2   Destructor

7   Destructor

4   Destructor


</details>

Q16. Why would a member function be declared private?

<details>

<summary> Click me to show the answer below!</summary>

Private member function may only be called from a function that is a member of the same class. Sometimes a class will contain one or more member functions that are necessary for internal processing, but should not be called by code outside the class. For example, a class might have a member function that performs a calculation only when a value is stored in a particular member variable and should not be performed at any other time. That function should not be directly accessible by code outside the class because it might get called at the wrong time. In this case, the member function should be declared private . When a member function is declared private , it may only be called internally.

</details>


Q17. What is the difference between an instance member variable and a static member variable?

<details>

<summary> Click me to show the answer below!</summary>
When a member variable is declared with the key word static , there will be only one copy of the member variable in memory, regardless of the number of instances of the class that might exist. A single copy of a class’s static member variable is shared by all instances of the class.
</details>

Q18. Static member variables are declared inside the class declaration. Where are static member variables defined?

<details>

<summary> Click me to show the answer below!</summary>

Outside of the class definition. For example,

``` cpp
 // Tree class
class Tree
 {
 private:
  static int objectCount; // Static member variable.
 public:
  // Constructor
  Tree()
  { objectCount++; }
  // Accessor function for objectCount
   int getObjectCount() const
   { return objectCount; }
 };

  // Definition of the static member variable, written
   // outside the class.
   int Tree::objectCount = 0;
```
</details>


Q19. If class X declares function f as a friend, does function f become a member of class X ?

<details>

<summary> Click me to show the answer below!</summary>

No.
</details>
