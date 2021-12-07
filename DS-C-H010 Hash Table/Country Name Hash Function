#include <stdio.h>
#define ARRAY_SIZE 10000
struct Bucket
{
    char value[1001];
}table[10000];
unsigned long int hash(char key[]){
    unsigned long int hash=5381;
    int index=0;
    while(key[index])
    {
        hash=hash*33+key[index];
        index++;
    }
    return hash;
}
void put(char key[], char value[])
{
    strcpy(table[hash(key)%ARRAY_SIZE].value, value);
}

char* get(char key[])
{
    return table[hash(key)%ARRAY_SIZE].value;
}

int main()
{
    int M,N, ctr;
    char name[1001], country[1001];
    scanf("%d", &M);
    for(ctr=1; ctr<=M; ctr++)
    {
        scanf("%s %s", name, country);
        put(name, country);
    }
    scanf("%d", &N);
    for(ctr=1; ctr<=N; ctr++)
    {
        scanf("%s", name);
        printf("%s\n", get(name));
    }
}
