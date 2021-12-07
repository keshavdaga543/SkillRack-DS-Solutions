#include <stdio.h>
#include <stdlib.h>
#include "insert.h"

/* Structure Definition is as below and root is the pointer to root Node
struct Node
{
    int data;
    struct Node *left, *right;
};

struct Node *root = NULL;
*/

void printPreorder(struct Node *node){
    if(node!=NULL){
        printf("%d ", node->data);
        printPreorder(node->left);
        printPreorder(node->right);
    }
}
int main()
{
    int N, data, ctr;
    scanf("%d", &N);
    for(ctr=1; ctr<= N; ctr++)
    {
        scanf("%d", &data);
        insert(root, data); //code in insert.h
    }
    printPreorder(root);
    return 0;
}
