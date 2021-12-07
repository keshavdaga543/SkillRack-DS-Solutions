#include<stdio.h>
struct Node
{
    int price;
    struct Node *next;
};
struct Node *head=NULL, *tail=NULL;
void prepend(int price)
{
    struct Node *newNode = malloc(sizeof (struct Node));
    newNode->price=price;
    newNode->next=head;
    head=newNode;
    if(tail==NULL)
    {
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
        prepend(price);
    }
    struct Node *ptr = head;
    while(ptr != NULL)
    {
        printf("%d->", ptr->price);
        ptr = ptr->next;
    }
    printf("NULL");
}
