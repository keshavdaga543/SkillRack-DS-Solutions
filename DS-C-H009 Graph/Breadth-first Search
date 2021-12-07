#include<stdio.h>
#include<stdlib.h>
int queue[10000];
int front=-1,rear=-1;
void add(int val){
    if(rear==-1){
        front=rear=0;
        queue[rear]=val;
    }
    else{
        queue[++rear]=val;
    }
}
int poll(){
    front++;
    return queue[front-1];
}
int main()
{
    int N,row,col,source;
    scanf("%d %d",&N,&source);
    int adjMatrix[N+1][N+1];
    for(row=1;row<=N;row++){
        for(col=1;col<=N;col++){
            scanf("%d",&adjMatrix[row][col]);
        }
    }
    int visited[N+1];
    for(col=1;col<=N;col++){
        visited[col]=0;
    }
    visited[source]=1;
    add(source);
    while(rear>=front){
        int curr=poll();
        printf("%d ",curr);
        for(col=1;col<=N;col++){
            if(adjMatrix[curr][col]==1&&visited[col]==0){
                add(col);
                visited[col]=1;
            }
        }
    }
    return 0;

}
