#include <stdio.h> //program to create a pascal triangle.

int factorial(int x)
{
    int ans = 1;
    for (int i = 1; i <= x; i++)
    {
        ans = ans * i;
    }
    return ans;
}

int main()
{
    int i, j, num;
    printf("enter the number of roes you want to print the pascal triangle\n");
    scanf("%d", &num);

    for (i = 0; i < num; i++)
    {

        for (int k = (num - i); k >= 1; k--)
        {
            printf(" ");
        }
        for (j = 0; j <= i; j++)
        {
            int ncr = factorial(i) / (factorial(j) * factorial(i - j));
            printf("%d ", ncr);
        }
        printf("\n");
    }
    return 0;
} 
