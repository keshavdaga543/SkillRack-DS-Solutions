#include<stdio.h>
struct Node
{
    int price;
    struct Node *prev, *next;
};
struct Node *head=NULL, *tail=NULL;
void append(int price){
    struct Node *newNode = malloc(sizeof *newNode);
    newNode->price=price;
    newNode->next=NULL;
    if(head==NULL){
        head=tail=newNode;
        newNode->prev=NULL;
    }
    else{
        tail->next=newNode;
        newNode->prev=tail;
        tail=newNode;
    }
}
int main()
{
    int N, counter, price;
    scanf("%d", &N);
    for(counter=1; counter<=N; counter++)
    {
        scanf("%d", &price);
        append(price);
    }
    struct Node *ptr = tail;
    while(ptr != NULL)
    {
        printf("%d <=> ", ptr->price);
        ptr = ptr->prev;
    }
    printf("NULL");
}
