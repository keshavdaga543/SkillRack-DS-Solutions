#include <stdio.h>
#include <stdlib.h>
int queue[1000], front = -1, rear = -1;
void insert(int val)
{
    queue[++rear] = val;
}
void poll()
{
    front++;
}
void display()
{
    int index;
    for(index=front+1; index <= rear; index++)
    {
        printf("%d ", queue[index]);
    }
}
int main()
{
    int N, X;
    scanf("%d", &N);
    int vehicleRegNum, ctr;
    for(ctr=1; ctr <= N; ctr++)
    {
        scanf("%d", &vehicleRegNum);
        insert(vehicleRegNum);
    }
    scanf("%d", &X);
    for(ctr=1; ctr <= X; ctr++)
    {
        poll();
    }
    display();
    return 0;
}
