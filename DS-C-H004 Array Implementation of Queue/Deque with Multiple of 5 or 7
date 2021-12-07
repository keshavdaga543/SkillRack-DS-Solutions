#include<stdio.h>
int deque[1000], size=0;
void addFirst(int data){
    for(int index=size;index>0;index--){
        deque[index]=deque[index-1];
    }
    deque[0]=data;
    size++;
}
void addLast(int data)
{
    deque[size++]=data;
}
int pollLast()
{
    return deque[size--];
}
int pollFirst()
{
    int data=deque[0];
    for(int index=0;index<size;index++){
        deque[index]=deque[index+1];
    }
    size--;
    return data;
}
int main()
{
    int N, num, index;
    scanf("%d",&N);
    while(N--)
    {
        scanf("%d",&num);
        if(num%5==0 && num%7==0)
        {
            pollLast();
        }
        else if(num%5==0)
        {
            addFirst(num);
        }
        else if(num%7==0)
        {
            addLast(num);
        }
        else
        {
            pollFirst();
        }
    }
    for(index=0; index<size; index++)
    {
        printf("%d ", deque[index]);
    }
}
