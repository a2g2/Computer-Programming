# Lab 4
Q1: Write a C program that reads in an integer denoting number of days. It prints 
the number of years, number of months and the number of days that constitute 
the input number of days. For example, if the input number is 403, it should 
print 1(year), 1(month), 13(days). For simplicity: there is no need to consider 
leap years and assume all months have 30 days. [Hint: Use modulus (%) and 
division (/) operators. End of Hint]

Soln:
```c
#include <stdio.h>
#include <math.h>

int main (){
int a, years, months, days;
scanf("%d", &a);
years = a/365;
a %= 365;
months = a/30;
a %= 30;
days = a;
printf("Years: %d\tMonths: %d\tDays: %d", years, months, days);
return 0;
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

int main () {
	int a, b;
	scanf("%d%d", &a,&b);
	a = a-b;
	b = a+b;
	a = b-a;
	printf("Swapped: %d\t%d", a,b);
	return 0;
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

Soln: `computer_sales.c`
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
return 0;
}
```

Q5: Write a C program, “ascii_test.c”, which takes two character as input and 
returns the sum of their ASCII as output. For instance, input is A and B, the 
output should be 131 (sum of the ASCII of A and B). [Hint: Use explicit typecast 
to covert character to integer values. End of Hint].

Soln: `ascii_test.c`
```c
#include <stdio.h>
#include <math.h>

int main(){
	char a,b;
	printf("Enter the Characters:\n");
	scanf("%c %c", &a,&b);
	int sum = (int)a+(int)b;
	/*Type casting byte, short, int , long (char and byte -> int) explicit(char->int) implicit is done by default by system */
	printf("%d\n", sum);
}

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

Soln: `math_ops.c`
```c
#include <stdio.h>
#include <math.h>

int main(){
	float x, y;
	printf("Enter Floating Point Numbers: ");
	scanf("%f %f", &x,&y);
	/*Expression 1*/
	float a = sin(60);
	float expr1 = ((exp(x)*a) + (5.6*pow(10,-5)))/(3*a);
	printf("Expression 1: %f\n", expr1);

	/*Expression 2*/
	float pi = 3.142;
	float b = atan(0.33);
	float c = (b + pi)/(2*y);
	float expr2 = sin(c);
	printf("Expression 2: %f\n", expr2);
	return 0;
}
```

Q8: As you know, the roots x1 and x2 of a quadratic equation ax2 + bx + c = 0 are 
calculated by: 
x1 = (–b + √ (b2 – 4ac))/2a,
x2 = (–b – √ (b2 – 4ac))/2a
Write a C program named “quadroots.c”, which should take a, b and c as 
inputs, and output the values of x1 and x2.

Soln: `quadroots.c`
```c
#include <stdio.h>
#include <math.h>

int main(){
	/*Roots of Quadratic Questions*/
	float a, b, c;
	printf("Enter values of a, b & c: \n");
	scanf("%f%f%f", &a,&b,&c);
	float D = (pow(b,2)-(4*a*c))/(2*a);
	float x1 = ((-1*b) + sqrt(D));
	float x2 = ((-1*b) - sqrt(D));
	printf("Roots are: %f\t%f", x1,x2);
	return 0;
}
```
