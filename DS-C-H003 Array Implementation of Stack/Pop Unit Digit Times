#include <stdio.h>
#include "stack.h"
int main()
{
int N,val;
scanf("%d",&N);
for(int ctr=1;ctr<=N;ctr++)
{
    scanf("%d",&val);
    if(val%10==0)
    {
        push(val);
    }
    else{
        int unitDigit=val%10;
        while(unitDigit--){
            pop();
        }
    }
}
    while(getSize()>=0)
    {
        printf("%d ", pop());
    }
    return 0;
}
