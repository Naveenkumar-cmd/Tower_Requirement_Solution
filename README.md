# c-programm
C program for finding number of towers required by taking its height as a stack.
#include <stdio.h>

int T(int n)
{
    if (n == 1 || n == 0)
        return 1;
    else if (n == 2)
        return 2;

    else
        return T(n - 3) +
               T(n - 2) +
               T(n - 1);
}

int main()
{
    int n;
    printf("Enter the height of Tower Needed \n");
    scanf("%d",&n);
    if(n>=0){
    printf("No of towers=%d\n", T(n));
    }
    else{
        printf("No of tower=0");
    }
    return 0;
}
