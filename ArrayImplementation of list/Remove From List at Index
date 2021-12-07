#include<stdio.h>
#define MAX 1000
int list[MAX], size = 0;
void removeAt(int removeIndex){
    int index;
    for(index=removeIndex;index<size;index++)
    {
        list[index]=list[index+1];
    }
    size--;
}
int main()
{
    int N, counter, M, indexToRemove;
    int totalScore=0, score, index;
    scanf("%d", &N);
    for(index=0; index < N; index++)
    {
        scanf("%d", &list[index]);
        size++;
    }
    scanf("%d", &M);
    for(counter=1; counter<=M; counter++)
    {
        scanf("%d", &indexToRemove);
        removeAt(indexToRemove);
    }
    for(index=0; index < size; index++)
    {
        totalScore += list[index];
    }
    printf("%d", totalScore);
}
