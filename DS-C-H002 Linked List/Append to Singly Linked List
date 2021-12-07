#include<stdio.h>
struct Node
{
    int price;
    struct Node *next;
};
struct Node *head=NULL, *tail=NULL;
void append(int price){
    struct Node *newNode = malloc(sizeof *newNode);
    newNode->price=price;
    newNode->next=NULL;
    if(head==NULL){
        head=tail=newNode;
    }
    else{
        tail->next=newNode;
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
    struct Node *ptr = head;
    while(ptr != NULL)
    {
        printf("%d->", ptr->price);
        ptr = ptr->next;
    }
    printf("NULL");
}
