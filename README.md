1.QUESTION


1. Write a c program to print all prime numbers between two limits.


CODE:

#include <stdio.h>
int main() 

int start, end, i, j, isPrime;

    printf("Enter two numbers: ");
    scanf("%d %d", &start, &end);

    printf("Prime numbers between %d and %d are:\n", start, end);

    for(i = start; i <= end; i++) {
        if(i < 2) continue;   // skip numbers less than 2

        isPrime = 1;

        for(j = 2; j <= i/2; j++) {
            if(i % j == 0) {
                isPrime = 0;
                break;
            }
        }

        if(isPrime == 1) {
            printf("%d ", i);
        }
    }

    return 0;
}

OUTPUT:

Enter two numbers: 10 30

Prime numbers between 10 and 30 are:
11 13 17 19 23 29


2.QUESTION

Write a c program to count the number of digits in a number.


CODE:



#include <stdio.h>
int main()

{

      int num, count = 0;

    printf("Enter a number: ");
    scanf("%d", &num);

    // Handle negative numbers
    if(num < 0) {
        num = -num;
    }

    // Count digits
    while(num != 0) {
        num = num / 10;
        count++;
    }

    // If number is 0
    if(count == 0) {
        count = 1;
    }

    printf("Number of digits = %d", count);

    return 0;
}
   
    


OUTPUT:

Enter a number: 12345

Number of digits = 5

3.QUESTION

Write a c program to print the alphabet S in n x n matrix.

CODE:

#include <stdio.h>
int main() 
    {
    
    int n, i, j;

    printf("Enter size (n): ");
    scanf("%d", &n);

    for(i = 0; i < n; i++) {
        for(j = 0; j < n; j++) {

            // Conditions to print 'S'
            if(i == 0 || i == n/2 || i == n-1 || 
               (j == 0 && i < n/2) || 
               (j == n-1 && i > n/2)) {
                printf("* ");
            } else {
                printf("  ");
            }

        }
        printf("\n");
    }

    return 0;
}
    
OUTPUT:

Example (n=7)

* * * * * * *
*            
*            
* * * * * * *
            *
            *
* * * * * * *


4.QUESTION

Write a c program to print the pyramid pattern.

    *

  ***

 *****

*******


CODE:

#include <stdio.h>
int main() {

    int i, j, n = 4;

    for(i = 1; i <= n; i++) {

        // print spaces
        for(j = 1; j <= n - i; j++) {
            printf(" ");
        }

        // print stars
        for(j = 1; j <= 2*i - 1; j++) {
            printf("*");
        }

        printf("\n");
    }

    return 0;
}
    
OUTPUT:


   *
  ***
 *****
*******

   


5.QUESTION

Write a c program to find GCD of two numbers using loop.

CODE:

#include <stdio.h>
int main() {


  
     int a, b, i, gcd;

    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);

    // Find GCD using loop
    for(i = 1; i <= a && i <= b; i++) {
        if(a % i == 0 && b % i == 0) {
            gcd = i;
        }
    }

    printf("GCD = %d", gcd);

     return 0;
}


OUTPUT:

Enter two numbers: 12 18

GCD = 6
