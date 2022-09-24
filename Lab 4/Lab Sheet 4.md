# Lab 4
Q1: Create a directory “lab4” inside “myprogs” directory that you have created in the 
last week’s lab session. This week, we will write a bit more advanced C programs.
We will also learn how to use <math.h> library for evaluating various mathematical 
expressions. You shall need to use the basics that were covered in the previous lab 
session. I hope that you are now familiar with the following arithmetic operations:
Addition: 
num3 = num1 + num2
Subtraction:
num3 = num1 - num2
Multiplication:
num3 = num1 + num2
Integer Division:
num3 = num1 / num2
Modulus (or remainder after division)
num3 = num1 % num2
Let us write a few more C programs using the fundamentals covered in the 
previous lab session

Soln:
```c
#include <stdio.h>
#include <math.h>

void main (){

}
```

Q2: 
Signed Range (-32,32)
Unsigned Range (0,64) -> int, char, short and long.


Q3: Write a C program, “swap.c”, to swap the values of two integer numbers a and 
b entered by the user, and display the new numbers to the user. Do this with 
and without using a third variable.

Soln: `swap.c`
```c
#include<stdio.h>
#include<math.h>

int main (void){
int a, b;
scanf("%d%d", &a,&b);

}
```

Q4: A computer manufacturing company has the following monthly compensation 
policy to their salespersons: 
Minimum base salary : 1500.00 
Bonus for every computer sold : 200.00 
Commission on the total monthly sales : 2 per cent 
Since the prices of computers are changing, the sale price of each computer is 
fixed at the beginning of every month. Write a C program, “computer_sales.c”,
to compute a sales-person's bonus, commission and gross salary. Your program 
should take the number of computers sold (in a month) and the sale price of a 
computer as user input.

Soln:`computer_sales.c`
```c
#include<stdio.h>
#include<math.h>

int main (void){
float bs = 1500.00;
float bonus = 200.00;
float a , b, bp1, cp1, gp1;
printf("Enter computers sold (in a month) and the sale price of a 
computer");
scanf("%h%h", a,b);
bp1 = a * bonus;
cp1 = 0.02 * a *b;
gp1 = bp1 + cp1;
printf("Sales-person's bonus, Commission and Gross salary are respectively:");
printf("%h\t%h\t%h\t", bp1, cp1, gp1); 
}
```

Q5: Write a C program, “ascii_test.c”, which takes two character as input and 
returns the sum of their ASCII as output. For instance, input is A and B, the 
output should be 131 (sum of the ASCII of A and B). [Hint: Use explicit typecast 
to covert character to integer values. End of Hint].

Soln:`ascii_test.c`
```c
char a,b;
scanf("%c%c", a,b);
int sum = (int)a+(int)b;
/*Type casting byte, short, int , long (char and byte -> int) explicit(char->int) implicit is done by default by system */
printf("%d", sum);
```
Q6: 
```c
#include <stdio.h>
#include <math.h>
int main()
{
int a = 4;
double b = sqrt((double)a);
/* Computes square root of “a” after converting it into a 
double variable */
/*double input and double output*/
printf(“Printing the value of square root of a: %lf \n”, b);
double angle = 2.3; // angle in radians
double c = sin(angle);
printf(“Sin %lf is: %lf \n”, angle, c);
return 0;
}
```
Q7:Write a C program in “math_ops.c” that evaluates and prints the values of the 
following arithmetic expressions. Here x and y are floating point numbers to be 
taken as input from the user. The value of pi is 3.142. Use exp, sin, cos and 
tan functions from math.h library. It is now your task to figure out how to use 
the above functions, what is their syntax. Take help of GOOGLE!

Soln:`math_ops.c`
