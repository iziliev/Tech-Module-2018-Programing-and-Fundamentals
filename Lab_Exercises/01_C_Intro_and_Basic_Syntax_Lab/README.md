## Lab: C# Intro and Basic Syntax

Problems for exercises and homework for the[“Programming Fundamentals Extended” course @ SoftUni](https://softuni.bg/courses/programming-fundamentals).

### Problem 1. Greeting

Write a program, which **greets** the user by their **name**, which it** reads **from the** console**.

#### Examples

**Input** | **Output**
--------- | ----------
Pesho     | Hello, Pesho!
Ivan      | Hello, Ivan!
Merry     | Hello, Merry!

### Problem 2. Add Two Numbers

Write a program, which **reads 2 whole numbers** and **adds** them together. Then, print them in the following format: 
· “a + b = sum”

#### Examples

**Input** | **Output** 
--------- | ----------
2         | 2 + 5 = 7
5     

**Input** | **Output**
--------- | ----------
1         | 1 + 3 = 4
3

**Input** | **Output**
--------- | ----------
-3        | -3 + 5 = 2
5

### Problem 3. Employee Data

Write a program to read **data** about an **employee** and print it on the console with the appropriate formatting. The order the input comes in is as such:

· Name – **no** formatting

· Age – **no** formatting

· Employee ID – **8-digit padding** (employee id 356 is 00000356)

· Monthly Salary – formatted to **2 decimal places** (2345.56789 becomes 2345.56)

#### Examples

**Input** | **Output**
--------- | ----------
Ivan      | Name: Ivan
24        | Age: 24
1192      | Employee ID: 00001192
1500.353  | Salary: 1500.35

**Input** | **Output**
--------- | ----------
Peter     | Name: Peter
30        | Age: 30    
113236    | Employee ID: 00113236
1738.1112 | Salary: 1738.11

**Input** | **Output**
--------- | ----------
Naiden    | Name: Naiden
27        | Age: 27
1111222   | Employee ID: 01111222
3560      | Salary: 3560.00

#### Hints

· You can use “D” and “F” to format numbers in C#. You can read more about formatting strings [here](https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx).
