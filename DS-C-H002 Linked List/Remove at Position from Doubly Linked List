#include<stdio.h>
#include "DLLAppend.h"
/* Structure Definition
struct Node
{
    int price;
    struct Node *prev, *next;
};
*/
struct Node *head=NULL, *tail=NULL;
void removeAt(int position){
    int counter=1;
    struct Node *ptr = head;
    if(position==1){
        head=head->next;
        if(head->next!=NULL){
            head->next->prev=head;
        }
        head->prev=NULL;
        free(ptr);
    }
    else{
        while(counter<position-1){
            ptr=ptr->next;
            counter++;
        }
        struct Node *temp = ptr->next;
        if(ptr->next==tail){
            tail=tail->prev;
        }
        ptr->next=ptr->next->next;
        if(ptr->next!=NULL){
            ptr->next->prev=ptr;
        }
        
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
    struct Node *ptr = tail;
    while(ptr != NULL)
    {
        printf("%d <=> ", ptr->price);
        ptr = ptr->prev;
    }
    printf("NULL");
}
