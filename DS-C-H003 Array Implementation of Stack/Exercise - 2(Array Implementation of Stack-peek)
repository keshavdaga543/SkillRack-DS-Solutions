#include <stdio.h>
#include <stdlib.h>
#include "stack.h"
int main()
{
    int N,data;
    scanf("%d",&N);
    for(int index=0; index<N; index++)
    {
        scanf("%d",&data);
        if(data%3==0)
        {
            pop();
            pop();
            pop();
            printf("%d ",peek());
        }
        else
        {
            push(data);
        }
    }
    return 0;
}
