# Programming Fundamentals - Assignment 1
## Day 1: 50 Questions with Answers

---

### Question 1: What is a variable in C/C++?

A variable is basically a container or a box in memory where we can store some data. Think of it like a labeled jar — you put something inside it, and whenever you need that thing, you just look at the label and use it. In programming terms, a variable has a name, a data type, and a value. For example, `int age = 20;` creates a variable named `age` that stores the integer value 20. The computer allocates some memory space for this variable, and we can access or modify that value throughout the program using its name.

---

### Question 2: Why do we use variables in programs?

We use variables because programs need to work with data, and data keeps changing. Imagine writing a calculator program where you hardcode every number — it would be useless. Variables let us store values temporarily, reuse them, perform calculations, and make our programs dynamic and flexible. Without variables, we would have to write the same value again and again, and any change would require rewriting the entire code. They also make the code readable and maintainable because names like `salary` or `temperature` tell us exactly what the data represents.

---

### Question 3: What is the difference between a variable name and its value?

The variable name is just a label or identifier that the programmer uses to refer to a memory location. It is fixed once declared (unless you change the code). The value, on the other hand, is the actual data stored inside that memory location, and it can change during program execution. For example, in `int score = 90;`, `score` is the variable name (the label), and `90` is the value (the actual data). Later in the program, you can write `score = 95;` — the name remains `score`, but the value changes from 90 to 95.

---

### Question 4: Which of the following is a valid variable name? a) 2num b) total_marks c) for d) my marks

The correct answer is **b) total_marks**.

Here is why the others are invalid:
- **a) 2num**: Variable names cannot start with a digit. They must begin with a letter or an underscore.
- **c) for**: This is a reserved keyword in C/C++. You cannot use keywords like `for`, `if`, `while`, `int`, etc. as variable names because they already have special meanings in the language.
- **d) my marks**: Variable names cannot contain spaces. If you need multiple words, use underscores (`my_marks`) or camelCase (`myMarks`).

---

### Question 5: Why is Age different from age?

C and C++ are case-sensitive languages. This means the compiler treats uppercase and lowercase letters as completely different characters. So `Age` and `age` are two entirely different variables as far as the compiler is concerned. You could declare `int Age = 25;` and `int age = 30;` in the same program, and they would occupy different memory locations. This is why it is important to be consistent with naming conventions — many programmers prefer lowercase or camelCase to avoid confusion and bugs caused by accidental case mismatches.

---

### Question 6: Can a variable name contain spaces? Why?

No, a variable name cannot contain spaces. The reason is simple: the compiler reads code by separating tokens using spaces. If you write `int my marks = 50;`, the compiler sees `int`, `my`, `marks`, and gets confused because it expects only one identifier after the data type. It would throw a syntax error. To combine multiple words into a single variable name, programmers use underscores (`student_marks`) or camelCase (`studentMarks`), which makes it readable without breaking the compiler's tokenization logic.

---

### Question 7: Can a variable name start with an underscore (_) ?

Yes, a variable name can start with an underscore. In C and C++, identifiers can begin with a letter (a-z, A-Z) or an underscore (_). However, starting variable names with an underscore is generally discouraged in normal user code because names beginning with an underscore followed by a capital letter or double underscore are reserved for compiler and standard library implementations. For example, `_Value` or `__count` might conflict with internal system variables. So while it is technically allowed, it is better to avoid it unless you have a specific naming convention or are writing low-level system code.

---

### Question 8: What happens if two variables have the same name in the same scope?

If you declare two variables with the same name in the same scope, the compiler will throw a redeclaration error. It cannot figure out which variable you are referring to when you use that name. For example:

```cpp
int main() {
    int x = 10;
    int x = 20;  // ERROR: redeclaration of 'int x'
    return 0;
}
```

However, if the variables are in different scopes (like one inside a function and one inside a loop, or one global and one local), the inner variable will shadow the outer one. The compiler will use the closest one, but this can lead to confusion and bugs, so it is best avoided.

---

### Question 9: Write three meaningful variable names for storing student information.

Here are three meaningful and descriptive variable names:

1. `studentName` — to store the full name of the student (as a string or character array).
2. `rollNumber` — to store the unique enrollment or roll number of the student.
3. `totalMarks` — to store the aggregate marks obtained by the student in all subjects.

These names are self-explanatory. Anyone reading the code immediately understands what data they hold, which is the whole point of good naming.

---

### Question 10: Which naming convention is better and why: studentMarks or sm?

`studentMarks` is definitely the better choice. While `sm` is shorter and faster to type, it is cryptic and meaningless. If someone else reads your code (or even you, after a few months), they will have no idea what `sm` stands for. It could mean "student marks," "subject marks," "something else," or anything. On the other hand, `studentMarks` clearly describes its purpose. In professional programming, readability and maintainability are far more important than saving a few keystrokes. The only time short names like `sm` are acceptable is in very small, temporary contexts like loop counters or mathematical formulas where the meaning is obvious.

---

### Question 11: What is a data type?

A data type tells the compiler what kind of data a variable will hold and how much memory it needs. It defines the range of possible values and the operations that can be performed on that data. For example, an `int` is meant for whole numbers, a `float` is for decimal numbers, and a `char` is for single characters. The data type is crucial because the compiler uses it to allocate the right amount of memory and to interpret the binary representation correctly. Without data types, the computer would not know whether a sequence of bits represents a number, a character, or something else entirely.

---

### Question 12: Which data type is used to store whole numbers?

The `int` (integer) data type is used to store whole numbers. It can hold positive numbers, negative numbers, and zero, but no fractional part. For example, `int count = 100;` or `int temperature = -5;`. If you need to store very large whole numbers, you can use `long` or `long long`, and for smaller ranges, you can use `short`. But `int` is the standard go-to type for whole numbers in most programs.

---

### Question 13: Which data type is used to store decimal values?

The `float` and `double` data types are used to store decimal (floating-point) values. `float` is a single-precision floating-point type, while `double` is double-precision. For most general purposes where you need decimal accuracy, `float` works fine. However, if you need higher precision (more digits after the decimal point), `double` is preferred because it uses more memory (8 bytes vs 4 bytes) and can represent numbers with greater accuracy.

---

### Question 14: What is the difference between float and double?

The main difference lies in precision and memory usage:

- **float**: Occupies 4 bytes of memory. It provides about 6-7 decimal digits of precision. It is suitable when memory is limited and you do not need extreme accuracy.
- **double**: Occupies 8 bytes of memory. It provides about 15-16 decimal digits of precision. It is the default choice for scientific calculations, financial computations, and anywhere accuracy matters.

For example, if you store 3.1415926535 in a `float`, it might only keep 3.141593, whereas a `double` would retain much more of the original value. In most modern systems, the speed difference is negligible, so `double` is generally recommended unless you specifically need to save memory.

---

### Question 15: Which data type stores a single character?

The `char` data type stores a single character. It occupies 1 byte of memory and can hold any single character from the ASCII set, such as letters, digits, punctuation marks, or special symbols. You write character literals inside single quotes. For example:

```cpp
char grade = 'A';
char symbol = '$';
char digit = '7';
```

Note that `'7'` is a character, not the integer 7. If you need to store a sequence of characters (a word or sentence), you use a string (in C++, `std::string` or a character array).

---

### Question 16: Which data type stores True/False values?

The `bool` (boolean) data type stores True/False values. It can only hold two possible values: `true` or `false`. In memory, `true` is typically stored as 1 and `false` as 0, but you work with the keywords. Booleans are essential for decision-making in programs — they are used in conditions, loops, and flags. For example:

```cpp
bool isPassed = true;
bool isRaining = false;
```

---

### Question 17: What data type is suitable for storing a person's name?

A person's name is a sequence of characters (a string), so you should use the `string` data type in C++. In C++, you can use `std::string` after including the `<string>` header. For example:

```cpp
#include <string>
using namespace std;

string name = "Rahul Sharma";
```

In pure C, you would use a character array like `char name[50];`, but in C++, `string` is much safer and easier because it handles memory automatically and provides useful functions like `length()`, `substr()`, etc.

---

### Question 18: Predict the output: int age=18; cout<<age;

The output will be:

```
18
```

Explanation: The variable `age` is initialized with the value 18. When we use `cout << age;`, the insertion operator sends the value stored in `age` to the standard output stream (the console). It does not print the word "age" — it prints the actual value, which is 18. There is no newline after it, so if another output follows, it would appear on the same line.

---

### Question 19: Identify the data type: 25, 3.14, 'A', true.

| Literal | Data Type | Explanation |
|---------|-----------|-------------|
| 25 | `int` | A whole number without a decimal point. |
| 3.14 | `double` | A decimal number. By default, decimal literals in C++ are treated as `double`. If you want `float`, you write `3.14f`. |
| 'A' | `char` | A single character enclosed in single quotes. |
| true | `bool` | A boolean literal representing the true condition. |

---

### Question 20: What happens if you store a decimal number in an int variable?

If you try to store a decimal number in an `int` variable, the fractional part gets truncated (cut off), not rounded. Only the integer part is kept. For example:

```cpp
int x = 9.7;
cout << x;  // Output: 9
```

The compiler may also issue a warning about possible loss of data, but the program will still compile and run. The value 9.7 becomes 9, not 10. This is called implicit type conversion or narrowing conversion. To avoid accidental data loss, it is better to use the appropriate data type (`float` or `double`) or explicitly cast the value if you truly intend to truncate it.

---

### Question 21: What is the purpose of cin?

`cin` stands for "character input" and is an object of the `istream` class. Its purpose is to read input from the standard input device, which is usually the keyboard. It allows the program to accept data from the user while the program is running, making the program interactive. Without `cin`, every value would have to be hardcoded, and the program would not be able to respond to different inputs. For example, `cin >> age;` pauses the program, waits for the user to type a number and press Enter, and then stores that number in the variable `age`.

---

### Question 22: What is the purpose of cout?

`cout` stands for "character output" and is an object of the `ostream` class. Its purpose is to send data to the standard output device, which is usually the monitor or console. It is used to display text, variable values, calculation results, and messages to the user. `cout` makes it possible to communicate with the user by showing what is happening inside the program. For example, `cout << "Hello";` prints the text "Hello" on the screen, and `cout << result;` prints the value of the variable `result`.

---

### Question 23: Which symbol is used with cin?

The **extraction operator** `>>` (two greater-than signs) is used with `cin`. It is called the extraction operator because it extracts data from the input stream and stores it into the variable on its right. The direction of the arrows points from the input stream toward the variable, indicating the flow of data. For example: `cin >> num;` extracts a value from the keyboard input and puts it into `num`.

---

### Question 24: Which symbol is used with cout?

The **insertion operator** `<<` (two less-than signs) is used with `cout`. It is called the insertion operator because it inserts data into the output stream. The direction of the arrows points from the data toward the output stream, indicating that the data is being sent to the console. For example: `cout << num;` inserts the value of `num` into the output stream, which then appears on the screen.

---

### Question 25: Explain: cin >> age;

This statement reads a value from the keyboard and stores it in the variable `age`. Here is the breakdown:
- `cin` is the standard input stream object.
- `>>` is the extraction operator.
- `age` is the variable where the extracted value will be stored.

When this line executes, the program pauses and waits for the user to type something and press Enter. The input is then converted to the data type of `age` (if compatible) and stored in that variable. If the user types something that cannot be converted (like text when `age` is an `int`), the input fails and the variable may be left in an invalid state.

---

### Question 26: Explain: cout << age;

This statement prints the value stored in the variable `age` to the screen. Here is the breakdown:
- `cout` is the standard output stream object.
- `<<` is the insertion operator.
- `age` is the variable whose value is being inserted into the output.

The output will be whatever number or character is currently stored in `age`. It will not print the word "age". If `age` contains 25, the screen will show `25`. This is one of the most basic ways to display variable contents in C++.

---

### Question 27: What is the purpose of endl?

`endl` stands for "end line" and is a manipulator used with `cout`. Its purpose is to insert a newline character into the output stream and flush the buffer. When you use `endl`, the cursor moves to the beginning of the next line, so the next output appears on a new line. For example:

```cpp
cout << "Hello" << endl;
cout << "World" << endl;
```

Output:
```
Hello
World
```

There is also `\n`, which inserts a newline but does not force a buffer flush. `endl` is slightly slower because of the flush, but for beginner programs, the difference is unnoticeable.

---

### Question 28: Write a statement to input a student's marks.

```cpp
int marks;
cin >> marks;
```

Or, if you want to be more descriptive and prompt the user:

```cpp
int marks;
cout << "Enter student's marks: ";
cin >> marks;
```

The first line declares an integer variable `marks`. The second line uses `cin` with the extraction operator to read an integer value from the keyboard and store it in `marks`. The prompt message helps the user understand what to type.

---

### Question 29: Write a statement to display 'Welcome to C++'.

```cpp
cout << "Welcome to C++";
```

Or, if you want it on its own line:

```cpp
cout << "Welcome to C++" << endl;
```

The text inside the double quotes is a string literal. `cout` sends it to the console. The `endl` (or `\n`) ensures the next output starts on a new line, which is usually good practice.

---

### Question 30: Predict the output: cout << 'Programming';

This code will actually cause a **compilation error** or at least a serious warning. The reason is that `'Programming'` is written with single quotes, but it contains multiple characters. In C++, single quotes are for single character literals (`char`), and double quotes are for string literals. A multi-character constant like `'Programming'` is non-standard and its behavior is undefined. The compiler might try to cram it into an integer (since `char` is promoted to `int`), but it will definitely not print the word "Programming". The correct way is:

```cpp
cout << "Programming";  // Using double quotes
```

---

### Question 31: What is an operator?

An operator is a special symbol or keyword that tells the compiler to perform a specific mathematical, logical, or relational operation on one or more operands (values or variables). Operators are the building blocks of expressions. For example, in `a + b`, `+` is the addition operator, and `a` and `b` are the operands. C++ has many types of operators: arithmetic (`+`, `-`, `*`, `/`, `%`), relational (`>`, `<`, `==`), logical (`&&`, `||`, `!`), assignment (`=`), bitwise, and more. Without operators, we could not perform calculations or make decisions in our programs.

---

### Question 32: Which operator is used for addition?

The **plus sign** `+` is the arithmetic operator used for addition. It adds two numbers together and returns the sum. For example:

```cpp
int sum = 10 + 5;  // sum becomes 15
int total = a + b; // adds values of a and b
```

It works with integers, floating-point numbers, and even character types (where it adds their ASCII values). It is one of the most fundamental operators in any programming language.

---

### Question 33: What is the result of 10 % 3?

The result is **1**.

The `%` symbol is the **modulo operator** (or modulus operator). It returns the remainder after dividing the left operand by the right operand. When you divide 10 by 3, you get 3 as the quotient and 1 as the remainder because 3 × 3 = 9, and 10 − 9 = 1. The modulo operator is very useful for checking divisibility, extracting digits, cycling through arrays, and determining even or odd numbers.

---

### Question 34: What is the result of 8 % 2?

The result is **0**.

Since 8 is perfectly divisible by 2 (2 × 4 = 8), there is no remainder left. The modulo operator returns 0 whenever the first number is exactly divisible by the second number. This is why `num % 2 == 0` is a common way to check if a number is even.

---

### Question 35: Which operator checks equality?

The **equality operator** `==` (two equal signs) checks whether two values are equal. It compares the operands and returns `true` if they are the same, and `false` if they are different. For example:

```cpp
if (a == b) {
    cout << "a and b are equal";
}
```

It is very important not to confuse `==` with `=`. The single `=` is assignment, not comparison. Using `=` in a condition is a common bug that changes the value instead of comparing it.

---

### Question 36: What is the difference between = and == ?

| Operator | Name | Purpose | Example |
|----------|------|---------|---------|
| `=` | Assignment Operator | Assigns the value on the right to the variable on the left. | `x = 5;` stores 5 in x. |
| `==` | Equality Operator | Compares two values and returns true if they are equal, false otherwise. | `if (x == 5)` checks if x is 5. |

The assignment operator `=` changes the value of a variable. The equality operator `==` does not change anything; it only evaluates a condition. Mixing them up is one of the most common mistakes beginners make. For example, `if (x = 5)` will always be true because it assigns 5 to x (and the expression evaluates to 5, which is non-zero), whereas `if (x == 5)` only checks if x is already 5.

---

### Question 37: What is the result of 5 > 3?

The result is **true** (which is represented as **1** in C++).

`>` is a relational operator that checks if the left operand is greater than the right operand. Since 5 is indeed greater than 3, the expression evaluates to the boolean value `true`. If you print this in C++, it will display `1` because `bool` values are printed as 1 for true and 0 for false. Relational operators are mostly used in `if` statements and loops to control the flow of the program.

---

### Question 38: What does && represent?

`&&` is the **logical AND operator**. It returns `true` only if both of its operands are true. If either operand is false, the entire expression becomes false. It is used to combine multiple conditions. For example:

```cpp
if (age >= 18 && age <= 60) {
    cout << "You are eligible to work.";
}
```

Here, both conditions must be satisfied: the person must be at least 18 AND at most 60. `&&` also uses short-circuit evaluation: if the first condition is false, the second one is not checked at all because the result is already determined to be false.

---

### Question 39: What does || represent?

`||` is the **logical OR operator**. It returns `true` if at least one of its operands is true. It only returns `false` when both operands are false. It is used when you want to check if any one of multiple conditions is satisfied. For example:

```cpp
if (day == "Saturday" || day == "Sunday") {
    cout << "It is a weekend!";
}
```

Here, if the day is either Saturday OR Sunday, the message prints. Like `&&`, `||` also uses short-circuit evaluation: if the first condition is true, the second one is skipped because the result is already true.

---

### Question 40: What does ! represent?

`!` is the **logical NOT operator**. It is a unary operator (works on a single operand) that inverts the boolean value. If the operand is true, `!` makes it false, and vice versa. For example:

```cpp
bool isRaining = false;
if (!isRaining) {
    cout << "You can go outside without an umbrella.";
}
```

`!isRaining` is true because `isRaining` is false. It is commonly used to check for negation or to ensure something is NOT the case, like `if (!file.open())` to check if a file failed to open.

---

### Question 41: Write a program to print 'Hello World'.

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello World" << endl;
    return 0;
}
```

**Input:** (No input required)

**Output:**
```
Hello World
```

**Explanation:** We include the `<iostream>` header for input/output operations. In `main()`, we use `cout` to print the string "Hello World" and `endl` to move to a new line. `return 0;` indicates the program ended successfully.

---

### Question 42: Write a program to input two numbers and display their sum.

```cpp
#include <iostream>
using namespace std;

int main() {
    int num1, num2, sum;

    cout << "Enter first number: ";
    cin >> num1;

    cout << "Enter second number: ";
    cin >> num2;

    sum = num1 + num2;

    cout << "The sum is: " << sum << endl;

    return 0;
}
```

**Sample Input:**
```
Enter first number: 15
Enter second number: 25
```

**Sample Output:**
```
The sum is: 40
```

**Explanation:** We declare three integer variables. We prompt the user and read two numbers using `cin`. We calculate the sum using the `+` operator and store it in `sum`. Finally, we display the result using `cout`.

---

### Question 43: Write a program to calculate the area of a rectangle.

```cpp
#include <iostream>
using namespace std;

int main() {
    float length, width, area;

    cout << "Enter length of rectangle: ";
    cin >> length;

    cout << "Enter width of rectangle: ";
    cin >> width;

    area = length * width;

    cout << "Area of rectangle = " << area << endl;

    return 0;
}
```

**Sample Input:**
```
Enter length of rectangle: 12.5
Enter width of rectangle: 8.0
```

**Sample Output:**
```
Area of rectangle = 100
```

**Explanation:** We use `float` because length and width can be decimal values. We multiply length by width to get the area and print it. The formula is straightforward: Area = Length × Width.

---

### Question 44: What formula is used to calculate Simple Interest?

The formula for Simple Interest is:

**Simple Interest = (Principal × Rate × Time) / 100**

Or in short:

**SI = (P × R × T) / 100**

Where:
- **P** = Principal amount (the initial sum of money)
- **R** = Rate of interest per annum (in percentage)
- **T** = Time period (in years)
- **SI** = Simple Interest earned

This formula assumes the interest is calculated uniformly over the entire time period without compounding.

---

### Question 45: Write a program to calculate Simple Interest.

```cpp
#include <iostream>
using namespace std;

int main() {
    float principal, rate, time, simpleInterest;

    cout << "Enter Principal amount: ";
    cin >> principal;

    cout << "Enter Rate of interest (per year): ";
    cin >> rate;

    cout << "Enter Time (in years): ";
    cin >> time;

    simpleInterest = (principal * rate * time) / 100;

    cout << "Simple Interest = " << simpleInterest << endl;

    return 0;
}
```

**Sample Input:**
```
Enter Principal amount: 10000
Enter Rate of interest (per year): 5
Enter Time (in years): 3
```

**Sample Output:**
```
Simple Interest = 1500
```

**Explanation:** We declare float variables because monetary values and interest rates can have decimal parts. We apply the formula SI = (P × R × T) / 100 and display the result. Using float ensures we do not lose precision if the user enters decimal values.

---

### Question 46: Why is a temporary variable used while swapping two numbers?

A temporary variable is used because if you directly overwrite one variable with another, you lose the original value. For example, if you have `a = 10` and `b = 20`, and you write `a = b;`, then `a` becomes 20, but the original value of `a` (which was 10) is gone forever. Now when you try `b = a;`, `b` gets 20 again, so both variables end up as 20. The swap fails.

A temporary variable acts like a backup. You store the value of `a` in `temp`, then copy `b` into `a`, and finally copy `temp` (the original `a`) into `b`. This way, both values are preserved and exchanged correctly. It is the simplest and most reliable method for swapping.

---

### Question 47: Swap the values: a=10, b=20.

Here is the step-by-step swapping using a temporary variable:

**Step 1:** Store `a` in `temp`
- `temp = a` → `temp` becomes 10

**Step 2:** Copy `b` into `a`
- `a = b` → `a` becomes 20

**Step 3:** Copy `temp` into `b`
- `b = temp` → `b` becomes 10

**Final values:** `a = 20`, `b = 10`

Here is the complete program:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 10, b = 20, temp;

    cout << "Before swapping: a = " << a << ", b = " << b << endl;

    temp = a;
    a = b;
    b = temp;

    cout << "After swapping: a = " << a << ", b = " << b << endl;

    return 0;
}
```

**Output:**
```
Before swapping: a = 10, b = 20
After swapping: a = 20, b = 10
```

---

### Question 48: What formula is used to convert Celsius into Fahrenheit?

The formula to convert Celsius to Fahrenheit is:

**F = (C × 9/5) + 32**

Or equivalently:

**F = (C × 1.8) + 32**

Where:
- **C** = Temperature in degrees Celsius
- **F** = Temperature in degrees Fahrenheit

For example, if C = 0, then F = (0 × 9/5) + 32 = 32°F. If C = 100, then F = (100 × 9/5) + 32 = 180 + 32 = 212°F.

---

### Question 49: What is the Fahrenheit value of 0°C?

Using the formula **F = (C × 9/5) + 32**:

F = (0 × 9/5) + 32 = 0 + 32 = **32°F**

So, 0 degrees Celsius is equal to 32 degrees Fahrenheit. This is the freezing point of water on the Fahrenheit scale. It is one of the most commonly known reference points for temperature conversion.

---

### Question 50: Why can integer division give incorrect results in the Celsius-to-Fahrenheit program?

Integer division can give incorrect results because in C/C++, if both operands of the division operator `/` are integers, the result is also an integer, and the decimal part is truncated (cut off). 

For example, in the expression `9/5`, both 9 and 5 are integers, so the result is `1`, not `1.8`. If you then write:

```cpp
int f = (c * 9 / 5) + 32;
```

For c = 37, you would get:
- `37 * 9 = 333`
- `333 / 5 = 66` (not 66.6)
- `66 + 32 = 98` (instead of the correct 98.6)

To fix this, you should make at least one operand a floating-point number, like `9.0/5` or `9/5.0`, or use `float`/`double` variables. This forces the compiler to perform floating-point division and preserve the decimal accuracy.

**Correct approach:**
```cpp
float f = (c * 9.0 / 5.0) + 32;
```

---

*End of Assignment 1*
