#include <stdio.h>
#include <stdlib.h>
struct node
{
    int vehicleRegNum;
    struct node* nextNode;
}*front, *rear;
struct node* createNode()
{
    struct node* newNode=malloc(sizeof(*newNode));
    newNode->nextNode=NULL;
    return newNode;
}
void add(int val){
    struct node* newNode=createNode();
    newNode->vehicleRegNum=val;
    if(rear==NULL && front==NULL){
        rear=front=newNode;
    }
    else{
        rear->nextNode=newNode;
        rear=newNode;
    }
}
void poll()
{
    struct node *temp=front;
    front=front->nextNode;
    free(temp);
}
void display()
{
    while(front->nextNode!=NULL)
    {
        printf("%d ", front->vehicleRegNum);
        front=front->nextNode;
    }
    printf("%d ", front->vehicleRegNum);
}
int main()
{
    int vehicleRegNum, N, X;
    scanf("%d",&N);
    front=rear=NULL;
    for(int ctr=1; ctr<=N; ctr++)
    {
        scanf("%d",&vehicleRegNum);
        add(vehicleRegNum);
    }
    scanf("%d",&X);
    for(int ctr=1; ctr<=X; ctr++)
    {
        poll();
    }
    display();
    return 0;
}
