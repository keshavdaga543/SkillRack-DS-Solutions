#include <stdio.h>
#include <stdlib.h>
struct Node{
    int data;
    struct Node *left, *right;
    
};
struct Node*head=NULL;
int height=0;
void insert(struct Node *currentNode, struct Node *newNode){
    if(newNode->data < currentNode->data){
        if(currentNode->left!=NULL)
        {
            insert(currentNode->left, newNode);
        }
        else{
            currentNode->left=newNode;
        }
    }
    else{
        if(currentNode->right!=NULL)
        {
            insert(currentNode->right, newNode);
        }
        else{
            currentNode->right=newNode;
        }
    }
}
struct Node* createNode(int data){
    struct Node *node = malloc(sizeof(struct Node));
    node->data=data;
    node->left=node->right=NULL;
    return node;
};
void traverse(struct Node *node, int level){
    if(node!=NULL){
        if(level>height){
            height=level;
        }
    
    traverse(node->left, level+1);
    traverse(node->right, level+1);
}
}
int main(){
    int N,data,ctr;
    scanf("%d",&N);
    scanf("%d",&data);
    head=createNode(data);
    for(ctr=1;ctr<=N-1;ctr++)
    {
        scanf("%d",&data);
        insert(head, createNode(data));
    }
    traverse(head, 0);
    printf("%d", height);
    return 0;
}
