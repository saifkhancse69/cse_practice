# cse_practice
Here,I will be dumping all the code I did while learning C programming!

Date: 9/16/2022

1. 1+11+111+... series
Code:
#include <stdio.h>
int main()
{
    int n,i,sum=0,t=1;
    printf("Terms= ");
    scanf("%d", &n);
    for(i=1; i<=n; i++)
        {
        printf("%d ",t);
        if(i<n)
            {
            printf(" + ");
            }
        sum=sum+t;
        t=(t*10)+1;
        }
    printf("\nSum: %d", sum);
}

2. Simple calculator (with switch case)
Code:
#include<stdio.h>
int main()
{
    int x,y;
    char c ;
    printf(" Enter in (x + y) format. (+,-,*,/)\n => ");
    scanf(" %d %c %d", &x, &c, &y);
    switch(c)
        {
        case '+':
            printf(" => %d",x+y);
            break;
        case '-':
            printf(" => %d",x-y);
            break;
        case '*':
            printf(" => %d",x*y);
            break;
        case '/':
            printf(" => %0.2f",(float)x/y);
            break;
        default :
            printf(" PlEASE ENTER INPUT IN CORRECT FORMAT !", c);
        }
}

3. Number pyramid (Maintaining serial)
Code:
#include<stdio.h>
int main()
{
    int i,j,k,l=1, row,spc;
    row= 5;
    spc=row+3;
    for (i=1; i<=row; i++)
        {
        for(k=spc; k>=1; k--)
            {
            printf(" ");
            }
        for( j=1; j<=i; j++)
            {
            printf("%d ", l++);
            }
        printf("\n");
        spc--;
        }
}

4. Hollow square (Pattern)
Code: 
#include<stdio.h>
int main()
{
    int i,j,row;
    printf("Rows: ");
    scanf("%d", &row);
    for (i=0; i<row ; i++)
        {
        for(j=0; j<row; j++)
            {
            if(i==0 || i==row-1 || j==0 || j==row-1)
                {
                printf("*");
                }
            else
                {
                printf(" ");
                }
            }
        printf("\n");
        }
}

5. Grade verification and counter (Switch Case)
Code:
#include<stdio.h>
int main()
{
    int i, marks, pass, f=0, Ap=0,A=0,Am=0,Bp=0,B=0,Bm=0,Cp=0,C=0,Cm=0,D=0 ;
    for(i=1; i!=-1; i++)
        {
        printf(" -> Marks (-1 to end)= ");
        scanf("%d", &marks);
        switch(marks)
            {
            case 97 ... 100 :
                printf(" => Grade: A+ \n");
                Ap++;
                break;
            case 90 ... 96 :
                printf(" => Grade: A\n ");
                A++;
                break;
            case 87 ... 89 :
                printf(" => Grade: A- \n");
                Am++;
                break;
            case 83 ... 86 :
                printf(" => Grade: B+\n ");
                Bp++;
                break;
            case 80 ... 82 :
                printf(" => Grade: B \n");
                B++;
                break;
            case 77 ... 79 :
                printf(" => Grade: B-\n ");
                Bm++;
                break;
            case 73 ... 76 :
                printf(" => Grade: C+ \n");
                Cp++;
                break;
            case 70 ... 72 :
                printf(" => Grade: C\n ");
                C++;
                break;
            case 67 ... 69 :
                printf(" => Grade: C- \n");
                Cm++;
                break;
            case 60 ... 66 :
                printf(" => Grade: D\n ");
                D++;
                break;
            case 0 ... 59 :
                printf(" => Grade: Fail \n");
                f++;
                break;
            case -1 :
                printf(" A+:  %d\n", Ap);
                printf(" A:   %d \n ", A);
                printf("A-:  %d\n ", Am);
                printf("B+:  %d\n ", Bp);
                printf("B:   %d \n ", B);
                printf("B-:  %d\n ", Bm);
                printf("C+:  %d\n ", Cp);
                printf("C:   %d \n ", C);
                printf("C-:  %d\n ", Cm);
                printf("D:   %d \n ", D);
                printf("Pass:%d\n ", pass=Ap+A+Am+Bp+B+Bm+Cp+C+Cm+D);
                printf("Fail:%d\n \n", f);
                return 0;
                break;
            default :
                printf("Please input 1-100.\n");
                break;
            } //switch
        } //for
}

6. Pyramid (Pattern)
Code:
#include<stdio.h>
int main()
{
    int i,j, row=5, spc;
    spc=row+3;
    for(i=1; i<=row; i++)
        {
        for(j=spc; j>=1; j--)
            {
            printf(" ");
            }
        for (j=1; j<=2*i-1; j++)
            {
            printf("*");
            }
        printf("\n");
        spc--;
        }
}

7. Diamond (Pattern)
Code:
#include<stdio.h>
int main()
{
    int row,star,spc;
    for(row=1; row<=5; row++)
        {
        for(spc=1; spc<=5-row; spc++)
            {
            printf(" ");
            }
        for(star=1; star<=2*row-1; star++)
            {
            printf("*");
            }
            printf("\n");
        }
    for(row=4; row>=1; row--)
        {
        for(spc=1; spc<=5-row; spc++)
            {
            printf(" ");
            }
        for(star=1; star<=2*row-1; star++)
            {
            printf("*");
            }
            printf("\n");
        }

}

Lab Assignment:
8. Write a C program which takes two integer values X and Y as inputs and determines which quadrant the point lies. 
Code:

9. Write a C program which takes two integer values X and Y as inputs and determines which quadrant the point lies. 
Code:

10. Generate a grade report based on the number given by the user.
Code:

11. Write a program to print odd numbers between 1 and 50 in reverse order. 
Code:

12. Generate the following pattern using nested while loops.
1
2 3
4 5 6
7 8 9 10
11 12 13 14 15
Code:


13. Find out the average of the given numbers from the user. Assume that user will input -1 to terminate the number series. 
Code:

14. Print Hello World 10 times along with the serial number and skip the 7th Hello World. Your program would only print a total of 9 ‘Hello world’s along with the serial number. 
Code:

15. You will take an integer number from the user. You have to find the summation of all the digits. 
Code:

16. In this problem, you will develop a program that can find how many times an integer number can be divided by Two (2).
Code:

17. You will take several integer numbers as inputs until the user enters -1. Then calculate the difference between the Highest and Lowest number.
Code:

18. 
