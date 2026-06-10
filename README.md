# OOP Lab Manual

## Week 07

### Experiment 01

Write a program that declares a `Complex` data type having real and imaginary as its private members.

Using operator overloading, declare operators that help in performing arithmetic operations on two complex objects. Also overload the assignment (`=`) operator to assign one complex object to another.

Example:

```cpp
Complex c, b;

c - b;
c + b;
c * b;
```

#### Class Specification

```cpp
class Complex
{
    double rp; // real part of the complex number
    double ip; // imaginary part of the complex number

public:
    Complex(double, double);
    Complex operator+(const Complex&);
    Complex operator-(const Complex&);
    Complex operator*(const Complex&);
    void print();
};
```

Create objects of the Complex class and demonstrate addition, subtraction, multiplication, and assignment operations using operator overloading.

---

### Experiment 02

Design a class named `Month`.

The class should have the following private members:

- `name` : A string object that holds the name of a month, such as "January", "February", etc.
- `monthNumber` : An integer variable that holds the number of the month. Valid values are 1 through 12.

#### Member Functions

- A default constructor that sets `monthNumber` to 1 and `name` to `"January"`.
- A constructor that accepts the name of the month as an argument. It should set `name` to the value passed and `monthNumber` to the correct value.
- A constructor that accepts the number of the month as an argument. It should set `monthNumber` to the value passed and `name` to the correct month name.
- Appropriate setter and getter functions for the `name` and `monthNumber` member variables.

#### Operator Overloading

##### Prefix and Postfix ++

Overload the prefix and postfix `++` operators to increment `monthNumber` and set `name` to the next month.

If `monthNumber` is 12, then incrementing should set:

```text
monthNumber = 1
name = "January"
```

##### Prefix and Postfix --

Overload the prefix and postfix `--` operators to decrement `monthNumber` and set `name` to the previous month.

If `monthNumber` is 1, then decrementing should set:

```text
monthNumber = 12
name = "December"
```

##### Stream Operators

Also overload:

```cpp
<<
>>
```

operators so that `cout` and `cin` can work directly with objects of the Month class.

Demonstrate all constructors, overloaded operators, and member functions in a complete program.

---

## Learning Objectives

After completing these experiments, students will be able to:

- Understand operator overloading in C++.
- Implement arithmetic operations using overloaded operators.
- Overload assignment and stream operators.
- Design classes with constructors and accessor functions.
- Apply prefix and postfix increment/decrement operators.
- Work with user-defined data types in object-oriented programming.

## Technologies Used

- C++
- Classes and Objects
- Operator Overloading
- Constructors
- Stream Operators
- Object-Oriented Programming
