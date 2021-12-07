#include <stdio.h>
#include <stdlib.h>
#include "preorder.h"
/* Structure definition
struct Node
{
    int data;
    struct Node *left, *right;
};
*/
struct Node *root = NULL;
struct Node* createNode(int data)
{
    struct Node *node=malloc(sizeof(struct Node));
    node->data=data;
    node->left=node->right=NULL;
    return node;
};
void insert(struct Node *currentnode, int data){
    if(currentnode==NULL){
        root=createNode(data);
        return;
    }
    if(data<currentnode->data)
    {
        if(currentnode->left!=NULL)
        {
            insert(currentnode->left, data);
        }
        else{
            currentnode->left=createNode(data);
        }
    }
    else
    {
        if(currentnode->right!=NULL){
            insert(currentnode->right, data);
            
        }
        else{
            currentnode->right=createNode(data);
        }
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
    printPreorder(root);
    return 0;
}
