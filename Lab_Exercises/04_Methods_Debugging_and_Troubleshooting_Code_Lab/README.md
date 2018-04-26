## Lab: Methods, Debugging and Troubleshooting Code

Problems for exercises and homework for the [“Programming Fundamentals” course @ SoftUni](https://softuni.bg/courses/programming-fundamentals).

You can check your solutions here: [https://judge.softuni.bg/Contests/304/Methods-and-Debugging-Lab](https://judge.softuni.bg/Contests/304/Methods-and-Debugging-Lab).

##  I. Declaring and Invoking Methods

### 1. Blank Receipt

Create a method that prints a blank cash receipt. The method should invoke three other methods: one for printing the header, one for the body and one for the footer of the receipt. 

The header should contain the following text:

CASH RECEIPT
------------------------------

The body should contain the following text:

Charged to____________________
Received by___________________

And the text for the footer:
------------------------------
© SoftUni

#### Examples

**Output**
CASH RECEIPT
------------------------------
Charged to____________________
Received by___________________
------------------------------
© SoftUni

#### Hints

1. First create a method with no parameters for printing the header starting with **static void**. Give it a **meaningful name** like "PrintReceiptHeader" and write the code that it will
execute:

2. Do the same for printing the receipt body and footer.

3. Create a **method that will call all three methods** in the necessary order. Again, give it a **meaningful and descriptive name** like "PrintReceipt" and write the code:

4. For printing **"©" **use Unicode **"\u00A9"**

5. **Call **(invoke) the PrintReceipt method from the main.

### 2. Sign of Integer Number

Create a method that prints the sign of an integer number n.

#### Examples

**Input** | **Output**
--------- | ----------
2         | The number 2 is positive.
-5        | The number -5 is negative.
0         | The number 0 is zero.

#### Hints

1. Create a method with a **descriptive name** like "PrintSign" which should receive **one parameter** of type **int**.

2. Implement the body of the method by handling different cases: 

a. If the number is greater than zero

b. If the number is less than zero

c. And if the number is equal to zero

3. Call (invoke) the newly created method from the main. 

### 3. Printing Triangle

Create a method for printing triangles as shown below:

#### Examples

**Input** | **Output**
--------- | ---------
3         |

1
1 2
1 2 3
1 2
1

**Input** | **Output**
--------- | ---------
4         |

1
1 2
1 2 3 
1 2 3 4
1 2 3
1 2
1

#### Hints

1. After you read the input

2. Start by creating a method **for printing a single line** from a **given start** to a **given end**. Choose a **meaningful
name** for it, describing its purpose:

3. Think how you can use it to solve the problem

4. After you spent some time thinking, you should have come to the conclusion that you will need two loops

5. In the first loop you can print the first half of the triangle without the middle line:

6. Next, print the middle line:

7. Lastly, print the rest of the triangle:

### 4. Draw a Filled Square

Draw at the console a filled square of size n like in the example:

#### Examples

**Input** | **Output**
--------- | ----------
4         |


#### Hints

1. Read the input

2. Create a method which will print the top and the bottom rows (they are the same). Don’t forget to give it a descriptive name and to give it as a parameter some length

a. Instead of loop you can use the "new string" command which creates a new string consisting of a character repeated some given times:

3. Create the method which will print the middle rows. Well, of course, you should probably name it "PrintMiddleRow" 

4. Use the methods that you've just created to draw a square

##    II. Returning Values and Overloading

### 5. Conversion

Create a method that converts a temperature from **Fahrenheit** to **Celsius**. Format the result to the 2nd decimal point. Use the formula: (fahrenheit - 32) * 5 / 9.

#### Examples

**Input** | **Output**
--------- | ----------
95        | 35.00
33.8      | 1.00
-40       | -40.00

#### Hints

1. Read the input

2. Create a method, which **returns a value of type **double:  

3. **Invoke** the method in the main and **save the return value in a new variable**:  

### 6. Calculate Triangle Area

Create a method that calculates and **returns** the [area](http://www.mathopenref.com/trianglearea.html) of a triangle by given base and height:

#### Examples

**Input** | **Output**
--------- | ---------- 
3         | 6
4

#### Hints

1. After reading the input

2. Create a method, but this time **instead** of typing **"static void"** before its name, type **"static double"** as this will make it to **return a value of type double**:

3. **Invoke** the method in the main and **save the return value in a new variable**:

### 7. Math Power

Create a method that calculates and returns the value of a number raised to a given power:

#### Examples

**Input** | **Output**
--------- | ---------- 
2         | 256
8
3         | 81
4

#### Hints

1. As usual, read the input

2. Create a method which will have two parameters - the number and the power, and will return a result of type double:

3. Print the result

### 8. Greater of Two Values

You are given two values of the same type as input. The values can be of type int, char of string. Create a method GetMax() that returns the greater of the two values: 

#### Examples

**Input** | **Output**
--------- | ----------  
int       | 16
2
16
char      | z
a
z
string    | Todor
Ivan
Todor

#### Hints

1. For this method you need to create three methods with the same name and different signatures

2. Create a method which will compare integers:

3. Create a second method with the same name which will compare characters. Follow the logic of the previous method:

4. Lastly you need to create a method to compare strings. This is a bit different as strings don't allow to be compared with the operators &gt; and &lt; You need to use the method "CompareTo()", which returns an integer value (greater than zero if the compared object is greater, less than zero if the compared object is lesser and zero if the two objects are equal.

5. The last step is to read the input, use appropriate variables and call the GetMax() from your Main(): 

## III. Debugging and Program Flow

### 9. Multiply Evens by Odds

Create a program that reads an **integer number** and **multiplies the sum of all its even digits** by **the sum of all its odd digits**:

#### Examples

**Input** | **Output**
--------- | ----------
12345     | 54

12345 has **2 even digits** - 2 and 4. Even digits has **sum of 6**. Also it has **3 odd digits** - 1, 3 and 5. Odd digits has **sum of 9**. **Multiply 6 by 9** and you get **54**.

**Input** | **Output**
--------- | ----------
-12345    | 54 

#### Hints

1. Create a method with a **name describing its purpose** (like GetMultipleOfEvensAndOdds). The method should have a **single integer parameter** and an** integer return value**. Also the method will call two other methods:

2. Create two other methods each of which will sum either even or odd digits

3. Implement the logic for summing odd digits:

4. Do the same for the method that will sum even digits

5. As you test your solution you may notice that it doesn't work for negative numbers. Following the program execution line by line, find and fix the bug (**hint: you can use Math.Abs()**)

### 10. Debug the Code: Holidays Between Two Dates

You are assigned to **find and fix the bugs** in an existing piece of code, using the Visual Studio **debugger**. You should
trace the program execution to find the lines of code that produce incorrect or unexpected results.

You are given a program (existing **source code**) that aims to **count the non-working days between two dates** given in format day.month.year (e.g. between **1.05.2015** and **15.05.2015** there are **5** non-working days – Saturday and Sunday).

#### Examples

**Input** | **Output**
--------- | ----------
1.05.2016 | 5
15.05.2016|

There are 5 non-working days (Saturday / Sunday) in this period: 1-May-2016, 7-May-2016, 8-May-2016, 14-May-2016, 15-May-2016

**Input** | **Output**
--------- | ----------
1.05.2016 | 1
2.05.2016 | 

Only 1 non-working day in the specified period: 1.05.2016 (Sunday)

**Input** | **Output**
--------- | ----------
15.05.2020| 0
10.05.2020| 

The second date is before the first. No dates in the range.

**Input** | **Output**
--------- | ----------
22.2.2020 | 4
1.3.2020  |  

TwoSaturdays and Sundays:
· 22.02.2020 and 23.02.2020
· 29.02.2020 and 1.03.2020

You can **find the broken code** in the judge system: [Broken Code for Refactoring](http://softuni.bg/downloads/svn/soft-tech/Sep-2016/Programming-Fundamentals-Sep-2016/03.%20Programming-Fundamentals-Methods-Debugging-and-Troubleshooting-Code/03.Programming-Fundamentals-Methods-and-Debugging-Lab-Broken-Solutions.zip). It looks as follows:

    HolidaysBetweenTwoDates.cs
    using System;
    using System.Globalization;
    classHolidaysBetweenTwoDates
    {
        staticvoid Main()
        {
            var startDate = DateTime.ParseExact(Console.ReadLine(),"dd.m.yyyy", CultureInfo.InvariantCulture);
            var endDate = DateTime.ParseExact(Console.ReadLine(),"dd.m.yyyy", CultureInfo.InvariantCulture);
            var holidaysCount = 0;

            for (var date = startDate; date &lt;= endDate; date.AddDays(1))
                if (date.DayOfWeek == DayOfWeek.Saturday && date.DayOfWeek == DayOfWeek.Sunday) 
                {
                    holidaysCount++;
                    Console.WriteLine(holidaysCount);
                }

         }
     }

#### Hints

There are **4****mistakes** in the code. You’ve got to **use the debugger** to find them and fix them. After you do that, submit your **fixed code in the judge contest**: [https://judge.softuni.bg/Contests/Practice/Index/304#8](https://judge.softuni.bg/Contests/Practice/Index/304#8).

### 11. Price Change Alert

You are assigned to **rework a given piece of code** which is working **without bugs** but is **not properly formatted**. 

The given program **tracks stock prices **and **gives updates** about the **significance in each price change**. Based on the significance, there are **four kind of changes**: no change at all (price is equal to the previous), minor (difference is below the significance threshold), price up and price down. 

You can **find the broken code**here: [Broken Code for Refactoring](http://softuni.bg/downloads/svn/soft-tech/Sep-2016/Programming-Fundamentals-Sep-2016/03.%20Programming-Fundamentals-Methods-Debugging-and-Troubleshooting-Code/03.Programming-Fundamentals-Methods-and-Debugging-Lab-Broken-Solutions.zip).

#### Input

· On the first line you are given **N** - the number of prices

· On the second line you are given the significance threshold

· On the next N lines, you are given prices

#### Output

· Don’t print anything for the first price

· If there is **no difference** from the previous price the output message is: "NO CHANGE: {current price}"

· In case of **minor change**: "MINOR CHANGE: {last price} to {current price} ({difference}%)"

· In case of **major change**: "PRICE UP: {last price} to {current price} ({difference}%)" or "PRICE DOWN: {last price} to {current price} ({difference}%)"

The percentage should be rounded to the second digit after the decimal point.

#### Examples

**Input** | **Output**
--------- | ----------
3         | PRICE UP: 10 to 11 (10.00%)
0.1       |MINOR CHANGE: 11 to 12 (9.09%)
10
11
12
**Input** | **Output**
--------- | ----------
3         | NO CHANGE: 10
0.1       | PRICE UP: 10 to 12 (20.00%)
10
10
12

#### Hints

1. Download the source code and get familiar with it

2. Deal with poor code formatting - Remove unnecessary blank lines, indent the code properly

3. Fix method parameters naming

4. Give methods a proper name
