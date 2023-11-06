# Bash Script operators
Write a minimum of 15 Bash script operators and there meaning/usage.

This README provides an overview of common Bash operators and their typical usages.

It will be very important to practice some of the examples on the terminal while reading this.

## Description
The following Bash script operators below are listed while some of the Arithmetic operators are further explain with examples.

### 1. Arithmetic Operators:

+, -, *, /, %: Basic arithmetic operators for addition, subtraction, multiplication, division, and modulo operations, respectively.

+=, -=, *=, /=, %=: Assignment operators for performing arithmetic operations and assigning the result back to a variable.


### 2. Comparison Operators:

 ==: Equal to (used for string or numeric comparisons).

 !=: Not equal to.

 <: Less than.

`>`: Greater than.

-eq: Numeric equal to.

-ne: Numeric not equal to.

-lt: Numeric less than.

-gt: Numeric greater than.

-le: Numeric less than or equal to.

-ge: Numeric greater than or equal to.

<: String less than.

`>`: String greater than.


### 3.Logical Operators:

&&: Logical AND operator.

||: Logical OR operator.

!: Logical NOT operator.

### 4.String Operators:

=: String equal to.

!=: String not equal to.

-z: Checks if a string is empty.

-n: Checks if a string is not empty.

str1 < str2: Checks if str1 is less than str2.

str1 > str2: Checks if str1 is greater than str2.

### 5.File Operators:

-e: Checks if a file exists.

-f: Checks if a file is a regular file.

-d: Checks if a file is a directory.

-s: Checks if a file is not empty.

-r: Checks if a file is readable.

-w: Checks if a file is writable.

-x: Checks if a file is executable.

### 6.Bitwise Operators:

&: Bitwise AND operator.

|: Bitwise OR operator.

^: Bitwise XOR operator.

~: Bitwise NOT operator.

<<: Left shift.

>>: Right shift.

### 7.Assignment Operators:

=: Assigns a value to a variable.

+=: Appends a value to a variable.

### 8.Miscellaneous Operators:

:: Null command or no operation.

;: Command separator.

&: Run a command in the background.

|: Pipe operator for command chaining.

&&: Execute the second command only if the first one succeeds.

||: Execute the second command only if the first one fails.

$(command): Command substitution for capturing the output of a command.

$((expression)): Arithmetic expansion for evaluating mathematical expressions.

*: Wildcard character for matching filenames.

?: Wildcard character for matching a single character in filenames.

[]: Used for character class matching in regular expressions.

{}: Used for brace expansion, especially in generating sequences.



## Further Explanation

### ‘+’ Integer Operator

‘+’ is an arithmetic operator to add the numeric values in bash.

The following example shows the addition of two integer numbers by using `expr` command. 

Here, you have to provide space before and after the ‘+’ operator otherwise, it will combine the values in place of addition.

$ echo `expr 5 + 25`

### += Integer Operator

‘+=’ is a shorthand arithmetic operator that adds an integer value with the value of a variable and store the result in that variable. 

In the following example, the value of $n will be added with 30 and store the result in $n.

$ n=20

$ echo $((n += 30))

### – Integer Operator

‘-‘ is an arithmetic operator that is used to subtraction value of two numbers. 

The following example shows the use of this operator that will subtract 15 from 35.

$ echo `expr 35 - 15`

### -= Integer Operator

‘-=’ is a shorthand arithmetic operator that subtract numeric value from a variable and store the result in that variable. 

The following example will subtract 100 from the variable $n and store the result in $n.

$ n=120

$ echo $((n -= 100))

### * Integer Operator
‘*’ operator is used to multiply number values. The following command shows the use of this operator that will multiply 5 by 7 and print 35 as output.

$ echo $((5 * 7))

### *= Integer Operator

‘*=’ is a shorthand arithmetic operator that multiplies the numeric value with the value of a variable and store that result in that variable. 

The following command will multiply 50 with the variable $n and store the result in $n.

$ n=10

$ echo $((n * 50))

### ** Integer Operator

‘**’ operator is used to calculate the xy. ‘**’ is used to print the value of 5^3 in the following command.

$ echo $((5 ** 3))

### / Integer Operator

‘/’ is an arithmetic operator to divide two numeric values in bash. The following commands show the division of two integer numbers by using `let` command.

$ let n=30/6

$ echo $n

### /= Integer Operator

‘/=’ is a shorthand arithmetic operator that divides a variable by a number and store the result into that variable. The following commands will divide $n by 10 and store the result in $n.

$ n=50

$ let n=n/10

$ echo $n

### % Integer Operator

‘%’ operator is used to calculate the remainder of the division of two numbers. The remainder value of 89/5 will be printed after executing the following command.

$ echo `expr 89 % 5`

### %= Integer Operator

‘%=’ is a shorthand arithmetic operator that calculates the remainder after dividing the values of a variable by a number and store the remainder value into that variable. 

The following commands show the use of this operator.

$ n=150

$ echo `expr $n % 7`

### ++ (Pre) Increment Operator

‘++` operator is used to increment the value of a variable by 1. When the operator is used before the variable then it will act as a pre-increment operator 

that means the value of the variable will be incremented first and will do other operation later. 

The value of $i will be incremented before adding with the number 10 in the following example.

$ i=39

$  echo $((++i+10))

### (Post) ++ Increment Operator

When ‘++’ operator is used after the variable then it will act as post-increment operator and it increments the value of the variable by 1 after doing another task. 

In this example, the current value of $i will be printed first and incremented by 1 in the second command that is 10. 

The last command will print the value of $i , which is 11.

$ i=10

$ echo $((i++))

$ echo $i

### – – (Pre) Decrement Operator

‘–` operator is used to decrement the value of a variable by 1. When the operator is used before the variable then it will act as a pre-decrement operator 

that means the value of the variable will be decremented first and the other operation will be done later. 

The value of $i will be decremented before adding with the number 15 in the following example.

$ i=36

$ echo $((--i+15))

### (Post) – – Decrement Operator

If ‘–‘ operator is used after the variable, then it will act as a post-decrement operator and it decrements the value of the variable by 1 after doing another task. 

In this example, the current value of $i will be printed first and decremented by 1 in the second command that is 6. 

The last command will print the value of $i after decrement, which is 5.

$ i=6

$ echo $((i--))

$ echo $i

### , comma Operator

‘,’ operator is used to execute multiple statements in a line. 

The following command shows the use of this operator: 

The value of $n is assigned to 10, 30 is added with $n and the value of $n is printed.

$ echo "$(( n=10, n=n+30 ))"

### ?: Ternary Operator

‘?:’ operator can be used as an alternative of if statement. 

The logical condition is defined before ‘?’  and if the condition returns true then it will execute the statement that is defined before ‘:’ 

otherwise it will execute the statement that is defined after ‘:’. The following script shows the use of this operator.

n=20

v1=100

v2=200

echo $(( n>=20 ? v1 : v2 ))

### comma Operator

‘,’ operator is used to execute multiple statements in a line. 

The following command shows the use of this operator. 

The value of $n is assigned to 10, 30 is added with $n and the value of $n is printed.

$ echo "$(( n=10, n=n+30 ))"

### & Bitwise Operator

‘&’ operator is used to perform bitwise AND operation that works on binary data.  The following command shows the use of this operator.

$ echo $((3 & 6))

### &= Bitwise Operator

‘&=’ operator is used to perform bitwise AND operation with the value of a variable and store the result in the variable. 

Run the following commands to show the use of this operator.

$ var=3

$ ((var&=7))

$ echo $var

### | Bit-wise Operator

‘|’ operator is used to perform bit-wise OR operation that works on binary data. 

The following command shows the use of this operator.

$ echo $((3 | 6))

### |= Bitwise Operator

‘|=’ operator used is to perform bitwise OR operation with the value of a variable and store the result in the variable. 

Run the following commands to show the use of this operator.

$ var=4

$ ((var|=2))

$ echo $var

### ^ Bitwise Operator

‘^’ operator is used to perform bitwise XOR operation that works on binary data.  

The following command shows the use of this operator.

$ echo $((3 ^ 6))

### ^= Bitwise Operator

‘^=’ operator is used to perform bitwise XOR operation with the value of a variable and store the result in the variable. 

Run the following commands to show the use of this operator.

$ var=5

$ ((var^=2))

$ echo $var

### ~ Bitwise Operator

‘~’ operator is used to complement the value. 

The following command shows the use of this operator. 

The complement of 7 is -8.

$ echo $(( ~7 ))

### << Bitwise Operator

‘<<‘ operator is used to left-shift the binary value. The following command shows the use of this operator.

$ echo $(( 6<<1 ))

### <<= Bitwise Operator

‘<<=’ operator is used to left shift the binary value of any variable and store the value in that variable. 

The following command shows the use of this operator.

$ var=5

$ ((var <<= 1))

$ echo $var

### >> Bitwise Operator

‘>>’ operator is used to right-shift the binary value. The following command shows the use of this operator.

$ echo $(( 8>>1 ))

### >>= Bitwise Operator

‘>>=’ operator is used to right-shift the binary value of any variable and store the value in that variable. 

The following command shows the use of this operator.

$ var=7

$ ((var >>= 1))

$ echo $var

### Conclusion

Thank you for taking the time to explore this project/repository. I hope you find it helpful and that you'll consider 

contributing to its further development. 

If you have any , suggestions, or feedback on our i can get better please don't hesitate to contact me at tajudeenadedejir2@gmail.com .

Please it will be great to practice more on the terminal for easy understanding.

Happy to be learning coding!

[Adedeji Tajudeen]


### Contact
tajudeenadedejir2@gmail.com

### Acknowledgement

https://linuxhint.com/bash_operator_examples

https://chat.openai.com

https://www.google.com

https://www.geeksforgeeks.org/basic-operators-in-shell-scripting/




































































