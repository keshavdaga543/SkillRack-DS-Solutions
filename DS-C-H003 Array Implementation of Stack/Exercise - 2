#include <stdio.h>
#include <stdlib.h>
#include "stack.h"
int main()
{
int N,data;
scanf("%d",&N);
for(int ctr=1;ctr<=N;ctr++){
    scanf("%d",&data);
    if(data%3==0){
        pop();
        pop();
        pop();
    }
    else
    {
        push(data);
    }
}
    while(getSize()>=0)
    {
        printf("%d ",pop());
    }
    return 0;
}
