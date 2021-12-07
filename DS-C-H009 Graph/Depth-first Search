#include<stdio.h>
#include<stdlib.h>
int N;
void dfs(int adjMatrix[N+1][N+1], int curr, int visited[N+1]){
    int col;
    printf("%d ", curr);
    visited[curr]=1;
    for(col=1;col<=N;col++){
        if(adjMatrix[curr][col]==1&&visited[col]==0){
            dfs(adjMatrix, col,visited);
        }
    }
}

int main()
{
    int row, col, source;
    scanf("%d %d", &N, &source);
    int adjMatrix[N+1][N+1];
    for(row=1;row<=N;row++){
        for(col=1;col<=N;col++){
            scanf("%d",&adjMatrix[row][col]);
        }
    }
    int visited[N+1];
    for(col=1;col<=N;col++)
    {
        visited[col]=0;
    }
    dfs(adjMatrix,source,visited);
    return 0;

}
