#include<stdio.h>
#include<stdlib.h>
void dfs(int roads[],int visited[],int city){
    visited[city]=1;
    int nextCity=roads[city];
    if(roads[city]!=-1){
        dfs(roads,visited,nextCity);
    }
}

int main()
{
    int src,from,to,R,N;
    scanf("%d %d %d",&N,&R,&src);
    int roads[N+1],index,visited[N+1];
    for(index=1;index<=N;index++){
        visited[index]=0;
        roads[index]=-1;
    }
    for(index=0;index<R;index++){
        scanf("%d %d",&from,&to);
        roads[from]=to;
    }
    dfs(roads,visited,src);
    for(index=1;index<=N;index++){
        if(visited[index]==0){
            printf("no");
            return 0;
        }
    }
    printf("yes");
    return 0;

}
