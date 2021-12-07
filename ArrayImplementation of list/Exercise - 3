#include <stdio.h>
#include <stdlib.h>
#include"list.h"
int main()
{
int N,val,index,oddCount=0,evenCount=0;
scanf("%d",&N);
for(index=0;index<N;index++)
{
    scanf("%d",&val);
    append(val);
    if(val%2==0)
    {
        evenCount++;
        oddCount=0;
    }
    else if(val%2!=0)
    {
        oddCount++;
        evenCount=0;
    }
    if(evenCount==3||oddCount==3)
    {
        removeLast();
        removeLast();
        removeLast();
        evenCount=0;
        oddCount=0;
        
    }
}
    for(index=0; index < getSize(); index++)
    {
        printf("%d ",array[index]);
    }
    return 0;
}
