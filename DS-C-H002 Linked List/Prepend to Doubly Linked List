#include<stdio.h>
struct Node
{
    int price;
    struct Node *prev, *next;
};
struct Node *head=NULL, *tail=NULL;
void prepend(int price){
    struct Node *newNode = malloc(sizeof (struct Node));
    newNode->price=price;
    newNode->next=head;
    newNode->prev=NULL;
    if(head!=NULL){
        head->prev=newNode;
    }
    head=newNode;
    if(tail==NULL)
    {
        tail=newNode;
        tail->next=NULL;
    }
}
int main()
{
    int N, counter, price;
    scanf("%d", &N);
    for(counter=1; counter<=N; counter++)
    {
        scanf("%d", &price);
        prepend(price);
    }
    struct Node *ptr = tail;
    while(ptr != NULL)
    {
        printf("%d <=> ", ptr->price);
        ptr = ptr->prev;
    }
    printf("NULL");
}
