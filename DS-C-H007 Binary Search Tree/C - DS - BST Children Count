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
int countChildren(struct Node *current, int data){
    if(current->data==data){
        int count=0;
        if(current->left){
            count++;
        }
        if(current->right){
            count++;
        }
        return count;
    }
    if(current->data <data)
    {
        return countChildren(current->right, data);
    }
    return countChildren(current->left, data);
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
    scanf("%d", &data);
    printf("%d", countChildren(root,data));
    return 0;
}
