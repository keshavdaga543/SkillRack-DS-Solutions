#include <stdio.h>
#include <stdlib.h>
struct node
{
    int val;
    struct node* nextNode;
};

struct node* createNode()
{
    struct node* newNode=malloc(sizeof(*newNode));
    newNode->nextNode=NULL;
    return newNode;
}
struct node *top;
void push(int value){
    struct node* nextNode = createNode();
    nextNode->val=value;
    if(top==NULL){
        top=nextNode;
    }
    else{
        nextNode->nextNode=top;
        top=nextNode;
    }
}
void pop()
{
    printf("%d ", top->val);
    top=top->nextNode;
}
int main()
{
    int currBookId, N, ctr;
    scanf("%d",&N);
    top=NULL;
    for(ctr=1; ctr<=N; ctr++)
    {
        scanf("%d",&currBookId);
        push(currBookId);
    }
    for(ctr=1; ctr<=N; ctr++)
    {
        pop();
    }
    return 0;
}
