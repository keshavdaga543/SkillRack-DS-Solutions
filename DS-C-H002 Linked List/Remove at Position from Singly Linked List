#include<stdio.h>
#include "SLLAppend.h"
/* Structure Definition
struct Node
{
    int price;
    struct Node *next;
};
*/
struct Node *head=NULL, *tail=NULL;

void removeAt(int position)
{
    int counter=1;
    struct Node *ptr=head;
    if(position==1){
        head=head->next;
        free(ptr);
        
    }
    else{
        while(counter<=position-2)
        {
            ptr=ptr->next;
            counter++;
        }
        struct Node *temp = ptr->next;
        ptr->next = ptr->next->next;
        free(temp);
    }
}
int main()
{
    int N, counter, price, position;
    scanf("%d", &N);
    for(counter=1; counter<=N; counter++)
    {
        scanf("%d", &price);
        append(&head, &tail, price);
    }
    int M;
    scanf("%d", &M);
    while(M--)
    {
        scanf("%d", &position);
        removeAt(position);
    }
    struct Node *ptr = head;
    while(ptr != NULL)
    {
        printf("%d->", ptr->price);
        ptr = ptr->next;
    }
    printf("NULL");
}
