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
    if(head==NULL){
        head=tail=newNode;
    }
    else{
        tail->next=newNode;
        newNode->prev=tail;
        tail=newNode;
    }
    tail->next=head;
    head->prev=tail;
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
    int position;
    scanf("%d", &position);
    struct Node *ptr = head, *start;
    while(position > 1)
    {
        ptr = ptr->next;
        position--;
    }
    start = ptr;
    do
    {
        printf("%d <=> ", ptr->price);
        ptr = ptr->next;
    }
    while(ptr != start);
    printf("\n");
    start = ptr;
    do
    {
        printf("%d <=> ", ptr->price);
        ptr = ptr->prev;
    }
    while(ptr != start);
}
