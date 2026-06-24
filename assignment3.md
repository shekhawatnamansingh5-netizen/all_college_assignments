# Assignment 3 - C Programming Error Analysis Sheet

| Question No. | Error | Line No. | Error Type | Error Correction |
|-------------|-------|----------|------------|-----------------|
| 1 | Missing semicolon after int x = 10 | 8 | Syntax Error | `int x = 10;` |
| 1 | Assignment operator = instead of comparison == in if | 13 | Logical Error | `if(x == 10)` |
| 1 | String assigned to int variable | 18 | Type Error | `int marks = 90;` |
| 1 | Undefined variable z | 20 | Semantic Error | `int z = 0; printf("%d\n", z);` |
| 1 | Lvalue required - 100 = x is invalid | 22 | Syntax Error | `x = 100;` |
| 1 | Array index out of bounds (arr[10] for size 5) | 26 | Runtime Error | `arr[4] = 50;` |
| 1 | Incompatible pointer type - float* to int* | 28 | Type Error | `int *ptr = &x;` |
| 1 | Wrong format specifier %f for int | 30 | Type Error | `printf("%d\n", x);` |
| 1 | Division by zero | 35 | Runtime Error | `Check if b != 0 before division` |
| 1 | Multi-character constant 'AB' | 37 | Type Error | `char ch = 'A';` |
| 1 | Same message in if and else (logical error) | 39 | Logical Error | `if(x > y) printf("X is greater"); else printf("Y is greater");` |
| 1 | sqrt() return value unused (warning) | 44 | Logical Error | `int result = sqrt(25);` |
| 1 | Undefined function show() | 46 | Semantic Error | `Define show() or remove call` |
| 1 | Semicolon after while makes empty loop | 48 | Logical Error | `while(x < 15) { x++; }` |
| 1 | continue outside loop | 53 | Syntax Error | `Remove or place inside loop` |
| 1 | break outside loop/switch | 55 | Syntax Error | `Remove or place inside loop/switch` |
| 1 | Function calculate() called with 1 argument instead of 2 | 57 | Semantic Error | `int result = calculate(10, 20);` |
| 2 | Missing semicolon after int num2 = 20 | 9 | Syntax Error | `int num2 = 20;` |
| 2 | Missing closing parenthesis in if | 21 | Syntax Error | `if(choice == 1)` |
| 2 | Extra closing parenthesis in else if | 33 | Syntax Error | `else if(choice == 3)` |
| 2 | Missing closing parenthesis in for loop | 50 | Syntax Error | `for(int i=0; i<5; i++)` |
| 2 | Missing closing parenthesis in while | 57 | Syntax Error | `while(choice > 0)` |
| 2 | Missing semicolon after do-while | 66 | Syntax Error | `while(choice > 5);` |
| 2 | Missing colon after case 2 | 74 | Syntax Error | `case 2:` |
| 2 | Missing closing quote in char literal | 101 | Syntax Error | `char grade = 'A';` |
| 2 | Missing closing bracket in array declaration | 105 | Syntax Error | `int arr[5];` |
| 2 | Missing closing brace for block | 126 | Syntax Error | `Add } before printf("Still Running")` |
| 2 | Missing semicolon after printf | 133 | Syntax Error | `printf("End of Program\n");` |
| 3 | String assigned to int variable | 8 | Type Error | `int age = 20;` |
| 3 | String assigned to char (should be single quotes) | 14 | Type Error | `char grade = 'A';` |
| 3 | Wrong format specifier %d for float | 16 | Type Error | `printf("%f\n", salary);` |
| 3 | Wrong format specifier %f for int | 18 | Type Error | `printf("%d\n", marks);` |
| 3 | Undefined variable score | 22 | Semantic Error | `int score = 0;` |
| 3 | Variable x redeclared | 25 | Semantic Error | `x = 20;` |
| 3 | Lvalue required - 100 = x | 27 | Syntax Error | `x = 100;` |
| 3 | Wrong format specifier %s for int | 31 | Type Error | `printf("%d\n", num);` |
| 3 | Wrong format specifier %d for float | 35 | Type Error | `printf("%f\n", pi);` |
| 3 | Floating point array index | 39 | Type Error | `arr[2] = 100;` |
| 3 | Float assigned to char (truncation) | 41 | Type Error | `char ch = 'A';` |
| 3 | Function add() called with 1 argument instead of 2 | 45 | Semantic Error | `result = add(10, 20);` |
| 3 | Function average() called with 2 arguments instead of 3 | 51 | Semantic Error | `avg = average(10, 20, 30);` |
| 3 | String assigned to int | 55 | Type Error | `int temperature = 35;` |
| 3 | String assigned to float | 59 | Type Error | `float discount = 10.5;` |
| 3 | Float subtracted from int (implicit conversion) | 61 | Type Error | `amount = amount - (int)discount;` |
| 3 | Array name cannot be assigned directly | 65 | Syntax Error | `strcpy(name, "Robil");` |
| 3 | Undefined variable totalMarks | 71 | Semantic Error | `int totalMarks = 0;` |
| 3 | Wrong format specifier %c for int | 75 | Type Error | `printf("%d\n", number);` |
| 3 | Wrong format specifier %d for float | 79 | Type Error | `printf("%f\n", rate);` |
| 3 | Function add() called with 3 arguments instead of 2 | 86 | Semantic Error | `sum = add(a, b);` |
| 3 | Float result stored in int (truncation) | 92 | Type Error | `float area; area = 3.14 * radius * radius;` |
| 3 | Assignment = instead of comparison == in if | 100 | Logical Error | `if(studentMarks == 100)` |
| 3 | String assigned to int | 105 | Type Error | `int size = 10;` |
| 3 | Wrong format specifier %d for float | 111 | Type Error | `printf("%f\n", percentage);` |
| 3 | String used as array index | 115 | Type Error | `arr2[5] = 100;` |
| 3 | String literal in case label | 125 | Type Error | `case 2:` |
| 3 | Undefined function multiply() | 132 | Semantic Error | `Define multiply() or remove call` |
| 3 | Wrong format specifier %d for float | 141 | Type Error | `printf("%f\n", areaRect);` |
| 3 | Float returned but stored in int | 151 | Type Error | `float avgMarks; avgMarks = average(...);` |
| 3 | Undefined variable value | 157 | Semantic Error | `int value = 0;` |
| 3 | String assigned to int | 159 | Type Error | `char employeeId[] = "EMP101";` |
| 4 | Function declared but not defined: calculateSalary | 3 | Semantic Error | `Define calculateSalary()` |
| 4 | Function declared but not defined: printStudentDetails | 6 | Semantic Error | `Define printStudentDetails()` |
| 4 | Function declared but not defined: showResult | 9 | Semantic Error | `Define showResult()` |
| 4 | Function declared but not defined: calculateAverage | 10 | Semantic Error | `Define calculateAverage()` |
| 4 | Extern variable totalStudents declared but not defined (extern needs definition elsewhere) | 12 | Semantic Error | `Remove extern or define in another file` |
| 4 | Extern variable companyProfit declared but not defined | 13 | Semantic Error | `Remove extern or define in another file` |
| 4 | Undefined function generateReport() | 47 | Semantic Error | `Define generateReport()` |
| 4 | Undefined function displayEmployee() | 49 | Semantic Error | `Define displayEmployee()` |
| 4 | Undefined function processData() | 51 | Semantic Error | `Define processData()` |
| 4 | Undefined function saveRecord() | 53 | Semantic Error | `Define saveRecord()` |
| 4 | Undefined function loadRecord() | 55 | Semantic Error | `Define loadRecord()` |
| 4 | Undefined function printInvoice() | 57 | Semantic Error | `Define printInvoice()` |
| 4 | Undefined function calculateTax() | 59 | Semantic Error | `Define calculateTax()` |
| 4 | Undefined function validateUser() | 61 | Semantic Error | `Define validateUser()` |
| 4 | Undefined function sendNotification() | 63 | Semantic Error | `Define sendNotification()` |
| 4 | Undefined function generateCertificate() | 65 | Semantic Error | `Define generateCertificate()` |
| 5 | Division by zero | 10 | Runtime Error | `Check if b != 0 before division` |
| 5 | Dereferencing NULL pointer | 13 | Runtime Error | `if(ptr1 != NULL) *ptr1 = 50;` |
| 5 | Array index out of bounds | 18 | Runtime Error | `arr[4] = 100;` |
| 5 | Dereferencing uninitialized pointer | 21 | Runtime Error | `int *ptr2 = malloc(sizeof(int)); *ptr2 = 200;` |
| 5 | Buffer overflow - strcpy into small array | 25 | Runtime Error | `char name[20]; strcpy(name, "Programming");` |
| 5 | Dereferencing uninitialized pointer | 29 | Runtime Error | `int *ptr3 = malloc(sizeof(int)); printf("%d\n", *ptr3);` |
| 5 | File not found - fopen returns NULL | 33 | Runtime Error | `if(fp != NULL) { fscanf(...); fclose(fp); }` |
| 5 | Buffer overflow in malloc'd memory | 38 | Runtime Error | `char *ptr4 = malloc(20); strcpy(ptr4, "Computer Science");` |
| 5 | Use after free | 43 | Runtime Error | `Don't access memory after free` |
| 5 | Double free | 48 | Runtime Error | `Free only once` |
| 5 | Modulo by zero | 53 | Runtime Error | `Check if y != 0 before x % y` |
| 5 | Buffer overflow - strcat into small array | 57 | Runtime Error | `char str1[30]; strcat(str1, "WorldProgramming");` |
| 5 | Array out of bounds in malloc'd memory | 62 | Runtime Error | `numbers = malloc(10 * sizeof(int));` |
| 5 | 2D array index out of bounds | 68 | Runtime Error | `matrix[2][2] = 100;` |
| 5 | Dereferencing NULL pointer | 71 | Runtime Error | `if(ptr6 != NULL) printf("%d\n", ptr6[0]);` |
| 5 | Using gets() - unsafe function | 75 | Runtime Error | `Use fgets(password, sizeof(password), stdin);` |
| 5 | Use after free | 80 | Runtime Error | `Don't access ptr7 after free` |
| 5 | Using uninitialized variable age | 84 | Runtime Error | `int age = 0;` |
| 5 | Negative array index | 87 | Runtime Error | `if(index >= 0) arr[index] = 50;` |
| 5 | Dereferencing uninitialized pointer | 90 | Runtime Error | `Initialize ptr8 before dereferencing` |
| 5 | Dereferencing NULL string pointer | 94 | Runtime Error | `if(text != NULL) printf("%s\n", text);` |
| 5 | Potential memory allocation failure | 99 | Runtime Error | `if(hugeArray != NULL) hugeArray[0] = 1;` |
| 5 | Infinite loop - pointer arithmetic on NULL | 104 | Runtime Error | `Remove infinite loop` |
| 6 | Wrong logic - odd printed as even | 13 | Logical Error | `if(num % 2 == 0) printf("Number is Even\n"); else printf("Number is Odd\n");` |
| 6 | Wrong grade logic - 90+ should be A not B | 23 | Logical Error | `if(marks >= 90) printf("Grade A\n"); else if(marks >= 80) printf("Grade B\n");` |
| 6 | Incomplete leap year logic | 33 | Logical Error | `if((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0))` |
| 6 | Wrong logic - age > 18 should be eligible | 43 | Logical Error | `if(age >= 18) printf("Eligible for Voting\n"); else printf("Not Eligible for Voting\n");` |
| 6 | Wrong logic - smaller number logic reversed | 53 | Logical Error | `if(a < b) printf("Smaller Number = %d\n", a); else printf("Smaller Number = %d\n", b);` |
| 6 | Wrong logic for largest - using < instead of > | 63 | Logical Error | `if(y > largest) largest = y; if(z > largest) largest = z;` |
| 6 | Integer division instead of float division | 73 | Logical Error | `average = (float)totalMarks / subjects;` |
| 6 | Wrong formula - area uses 2 (circumference formula) | 83 | Logical Error | `area = 3.14 * radius * radius;` |
| 6 | Wrong bonus calculation - 0.02 should be 0.20 and vice versa | 93 | Logical Error | `if(salary > 30000) bonus = salary * 0.20; else bonus = salary * 0.02;` |
| 6 | Wrong month names - case 1 is January not February | 103 | Logical Error | `case 1: printf("January\n"); case 2: printf("February\n"); ...` |
| 6 | Wrong prime logic - isPrime set to 1 when divisible | 115 | Logical Error | `isPrime = 0; break;` |
| 6 | Wrong discount logic - adding instead of subtracting | 126 | Logical Error | `finalAmount = purchaseAmount - discount;` |
| 6 | Wrong sum logic - sum overwritten instead of accumulated | 136 | Logical Error | `sum += i;` |
| 6 | Wrong temperature logic - < 40 is hot not cold | 146 | Logical Error | `if(temperature > 35) printf("Hot Weather\n"); else printf("Cold Weather\n");` |
| 6 | Wrong grade logic - A should be excellent not average | 156 | Logical Error | `if(grade == 'A') printf("Excellent Performance\n"); else printf("Average Performance\n");` |
| 6 | Wrong area formula - using + instead of * | 166 | Logical Error | `rectangleArea = length * width;` |
| 6 | Wrong pass/fail logic - >= 60 should be pass | 176 | Logical Error | `if(percentage >= 60) printf("Pass\n"); else printf("Fail\n");` |
| 7 | Array index out of bounds - i<=5 for size 5 | 10 | Runtime Error | `for(int i=0; i<5; i++)` |
| 7 | Integer division for average - should be float | 20 | Logical Error | `average = (float)total / 5;` |
| 7 | Array index out of bounds - i starts at 1, misses 0 | 27 | Runtime Error | `for(int i=0; i<10; i++) numbers[i] = i * 10;` |
| 7 | Buffer overflow - strcpy into small array | 37 | Runtime Error | `char name[20]; strcpy(name, "ComputerScience");` |
| 7 | Array name cannot be assigned directly | 42 | Syntax Error | `strcpy(city, "Delhi");` |
| 7 | String comparison using == instead of strcmp | 49 | Logical Error | `if(strcmp(str1, str2) == 0)` |
| 7 | Using gets() - unsafe function | 56 | Runtime Error | `Use fgets(password, sizeof(password), stdin);` |
| 7 | Buffer overflow - strcat may exceed array size | 64 | Runtime Error | `char firstName[40]; strcat(firstName, lastName);` |
| 7 | String not null-terminated - grade array too small | 71 | Runtime Error | `char grade[3] = "A+";` |
| 7 | Negative array index | 76 | Runtime Error | `arr[0]` |
| 7 | Buffer overflow - email array too small | 87 | Runtime Error | `char email[30] = "student@gmail.com";` |
| 7 | Array index out of bounds - scores[3] for size 3 | 96 | Runtime Error | `int scores[4];` |
| 7 | String comparison using == instead of strcmp | 107 | Logical Error | `if(strcmp(username, "admin") == 0)` |
| 7 | Buffer overflow - strcpy into small array | 114 | Runtime Error | `char mobile[15]; strcpy(mobile, "987654321012");` |
| 7 | Array index out of bounds - i<=5 for size 5 | 121 | Runtime Error | `for(int i=0; i<5; i++)` |
| 7 | Array index out of bounds - course[20] for size 20 | 128 | Runtime Error | `course[0] to course[19] only` |
| 7 | String not null-terminated - college array | 135 | Runtime Error | `char college[20]; college[0]='A';... college[5]='\0';` |
| 7 | Buffer overflow - section array too small | 149 | Runtime Error | `char section[5] = "IT-A";` |
| 8 | Function add() called with 1 argument instead of 2 | 14 | Semantic Error | `result = add(num1, num2);` |
| 8 | Function average() called with 2 arguments instead of 3 | 20 | Semantic Error | `avg = average(70, 80, 90);` |
| 8 | Factorial of 0 returns 0 instead of 1 | 26 | Logical Error | `if(n == 0) return 1;` |
| 8 | Swap by value - doesn't actually swap x and y in main | 35 | Logical Error | `Use pointers: void swap(int *a, int *b)` |
| 8 | Maximum returns wrong value (returns smaller) | 45 | Logical Error | `if(a > b) return a; else return b;` |
| 8 | Fibonacci recursion wrong - fibonacci(n) instead of fibonacci(n-1) | 55 | Logical Error | `return fibonacci(n-1) + fibonacci(n-2);` |
| 8 | Undefined function calculateGrade() | 62 | Semantic Error | `Define calculateGrade()` |
| 8 | Undefined function circleArea() | 67 | Semantic Error | `Define circleArea()` |
| 8 | Undefined function sumArray() | 72 | Semantic Error | `Define sumArray()` |
| 8 | Undefined function displayResult() | 77 | Semantic Error | `Define displayResult()` |
| 8 | Wrong percentage formula - integer division first | 102 | Logical Error | `return (marks * 100) / total;` |
| 8 | Function returns float but no return value | 108 | Semantic Error | `return si;` |
| 8 | Power function loop starts at 1 instead of 0 | 121 | Logical Error | `for(int i=0; i<exp; i++)` |
| 8 | reverseNumber doesn't return the reversed number | 130 | Semantic Error | `return rev;` |
| 8 | isPrime returns 1 for non-prime, 0 for prime (inverted) | 145 | Logical Error | `return 0; // for non-prime, return 1 for prime` |
| 8 | printArray uses <=size causing out of bounds | 160 | Runtime Error | `for(int i=0; i<size; i++)` |
| 8 | Infinite recursion - recursiveDemo(n+1) never stops | 165 | Runtime Error | `Add base case` |
| 8 | Rectangle area returns sum instead of product | 175 | Logical Error | `return length * width;` |
| 8 | cube function returns n*n instead of n*n*n | 180 | Logical Error | `return n * n * n;` |
| 9 | Dereferencing uninitialized pointer | 10 | Runtime Error | `int *ptr1 = malloc(sizeof(int)); *ptr1 = 0;` |
| 9 | Dereferencing NULL pointer | 14 | Runtime Error | `if(ptr2 != NULL) *ptr2 = 100;` |
| 9 | Pointer arithmetic out of bounds | 22 | Runtime Error | `Don't increment ptr3 beyond array` |
| 9 | Array index out of bounds via pointer | 27 | Runtime Error | `*(ptr4 + 4)` |
| 9 | Use after free | 37 | Runtime Error | `Don't access *ptr5 after free` |
| 9 | Array out of bounds in malloc'd memory | 46 | Runtime Error | `ptr7 = malloc(10 * sizeof(int));` |
| 9 | Array out of bounds - ptr8[3] for malloc(3) | 55 | Runtime Error | `ptr8 = malloc(4 * sizeof(int));` |
| 9 | Double free | 62 | Runtime Error | `Free only once` |
| 9 | Dereferencing uninitialized malloc'd memory | 67 | Runtime Error | `*ptr10 = 0; before printf` |
| 9 | Array out of bounds - numbers[5] for malloc(5) | 73 | Runtime Error | `for(int i=0; i<5; i++)` |
| 9 | Swap function swaps pointers, not values | 82 | Logical Error | `Use int temp = *a; *a = *b; *b = temp;` |
| 9 | Double pointer used incorrectly - pptr should be int** | 89 | Type Error | `int **pptr = &value_ptr; int *value_ptr = &value;` |
| 9 | Buffer overflow - strcpy into small malloc | 95 | Runtime Error | `name = malloc(20);` |
| 9 | Pointer arithmetic out of bounds after increment | 102 | Runtime Error | `Don't access *ptr11 after ptr11++` |
| 9 | Dereferencing NULL pointer | 107 | Runtime Error | `if(ptr12 != NULL && *ptr12 > 0)` |
| 9 | Array out of bounds - ptr13[100] for malloc(100) | 116 | Runtime Error | `ptr13[99] = 500;` |
| 9 | Use after free | 122 | Runtime Error | `Don't access *ptr14 after free` |
| 9 | 2D array accessed via pointer with wrong offset | 129 | Runtime Error | `Use matrix[row][col] syntax` |
| 9 | Memory leak - ptr15 malloc'd twice without freeing first | 135 | Runtime Error | `free(ptr15); before second malloc or use realloc` |
| 10 | Missing semicolon after int choice = 1 | 8 | Syntax Error | `int choice = 1;` |
| 10 | String assigned to int | 10 | Type Error | `int marks = 90;` |
| 10 | Function add() called with 1 argument instead of 2 | 16 | Semantic Error | `result = add(a, b);` |
| 10 | Assignment = instead of comparison == in if | 20 | Logical Error | `if(a == b)` |
| 10 | Undefined variable score | 23 | Semantic Error | `int score = 0;` |
| 10 | Array index out of bounds | 28 | Runtime Error | `arr[4] = 100;` |
| 10 | Negative array index | 30 | Runtime Error | `if(index >= 0) arr[index] = 50;` |
| 10 | Buffer overflow - strcpy into small array | 34 | Runtime Error | `char name[25]; strcpy(name, "ProgrammingLanguage");` |
| 10 | Array name cannot be assigned directly | 39 | Syntax Error | `strcpy(city, "Delhi");` |
| 10 | String comparison using == instead of strcmp | 44 | Logical Error | `if(strcmp(user, "admin") == 0)` |
| 10 | Division by zero | 50 | Runtime Error | `if(y != 0) printf("%d\n", x/y);` |
| 10 | Dereferencing NULL pointer | 54 | Runtime Error | `if(ptr1 != NULL) *ptr1 = 500;` |
| 10 | Dereferencing uninitialized pointer | 58 | Runtime Error | `int *ptr2 = malloc(sizeof(int));` |
| 10 | Use after free | 64 | Runtime Error | `Don't access *ptr3 after free` |
| 10 | Double free | 68 | Runtime Error | `Free only once` |
| 10 | Array out of bounds in malloc'd memory | 72 | Runtime Error | `ptr4 = malloc(5 * sizeof(int));` |
| 10 | Memory leak - ptr5 malloc'd twice | 80 | Runtime Error | `free(ptr5); before second malloc` |
| 10 | Function average() called with 2 arguments instead of 3 | 86 | Semantic Error | `avg = average(70, 80, 90);` |
| 10 | Wrong age logic - > 18 should be eligible | 94 | Logical Error | `if(age >= 18) printf("Eligible\n"); else printf("Not Eligible\n");` |
| 10 | Wrong prime logic - isPrime set to 1 when divisible | 104 | Logical Error | `isPrime = 0; break;` |
| 10 | Undefined function displayReport() | 116 | Semantic Error | `Define displayReport()` |
| 10 | Undefined function calculateSalary() | 118 | Semantic Error | `Define calculateSalary()` |
| 10 | File not found - fopen returns NULL | 122 | Runtime Error | `if(fp != NULL) { fscanf(...); fclose(fp); }` |
| 10 | Missing colon after case 1 | 129 | Syntax Error | `case 1:` |
| 10 | Missing break in case 2 | 137 | Logical Error | `Add break after case 2` |
| 10 | Multi-character constant 'AB' | 142 | Type Error | `char grade = 'A';` |
| 10 | Array index out of bounds - scores[3] for size 3 | 149 | Runtime Error | `int scores[4];` |
| 10 | Array index out of bounds - i<=3 for size 3 | 153 | Runtime Error | `for(int i=0; i<3; i++)` |
| 10 | Wrong area formula - uses 2 (circumference) | 162 | Logical Error | `area = 3.14 * radius * radius;` |
| 10 | Semicolon after while makes empty loop | 170 | Logical Error | `while(choice > 0) { choice--; }` |
| 10 | continue outside loop | 174 | Syntax Error | `Remove or place inside loop` |
