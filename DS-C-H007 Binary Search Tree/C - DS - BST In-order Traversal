#include <stdio.h>
#include <stdlib.h>
#include "insert.h"
/* Structure definition
struct Node
{
    int data;
    struct Node *left, *right;
};
struct Node *root = NULL;
*/
void printInorder(struct Node *node){
    if(node!=NULL){
        printInorder(node->left);
        printf("%d ", node->data);
        printInorder(node->right);
    }
}
int main()
{
    int N, data, ctr;
    scanf("%d", &N);
    for(ctr=1; ctr<= N; ctr++)
    {
        scanf("%d", &data);
        insert(root, data);
    }
    printInorder(root);
    return 0;
}
