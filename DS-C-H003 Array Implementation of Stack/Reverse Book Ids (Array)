#include <stdio.h>
#include <stdlib.h>
int stack[1000], top= -1;
void push(int val){
    stack[++top]=val;
    
}
int pop()
{
    return stack[top--];
}
int main()
{
    int N;
    scanf("%d", &N);
    int index, currBookId, ctr;
    for(index=0; index < N; index++)
    {
        scanf("%d", &currBookId);
        push(currBookId);
    }
    for(ctr=1; ctr <= N; ctr++)
    {
        printf("%d ", pop());
    }
    return 0;
}
