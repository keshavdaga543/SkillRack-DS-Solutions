#include <stdio.h>
#include <stdlib.h>
#include "insert.h"

/*
struct Node
{
    int data;
    struct Node *left, *right;
};

struct Node *root = NULL;
*/
void printPostorder(struct Node *node)
{
    if(node!=NULL)
    {
        printPostorder(node->left);
        printPostorder(node->right);
        printf("%d ", node->data);
    }
}
int main()
{
    int N, data, ctr;
    scanf("%d", &N);
    for(ctr=1; ctr<= N; ctr++)
    {
        scanf("%d", &data);
        insert(root, data); //invokes code in insert.h to form the BST
    }
    printPostorder(root);
    return 0;
}
