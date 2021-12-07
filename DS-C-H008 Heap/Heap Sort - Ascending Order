#include<stdio.h>

void swap(int *a, int *b)
{
    int temp = *a;
    *a = *b;
    *b = temp;
}

int extractMin(int arr[],int *size){
    int minVal = arr[1];
    arr[1] = arr[*size];
    (*size)--;
    buildMinHeap(arr, *size, 1);
    return minVal;
}

int minIndex(int arr[],int x, int y){
    return arr[x] <= arr[y] ? x:y;
}
void buildMinHeap(int arr[],int size,int curIndex){
    int minChildIndex=minIndex(arr,curIndex*2, curIndex*2+1 > size ? curIndex*2:curIndex*2+1);
    if(arr[minChildIndex] < arr[curIndex]){
        swap(&arr[minChildIndex], &arr[curIndex]);
        curIndex = minChildIndex;
        if(curIndex<=size/2){
            buildMinHeap(arr, size, curIndex);
        }
    }
    
}
int main()
{
    int size, index;
    scanf("%d", &size);
    int heapArray[size+1];
    for(index=1; index <= size; index++){
        scanf("%d", &heapArray[index]);
    }

    for(index = size/2; index >= 1; index--)
    {
        buildMinHeap(heapArray, size, index);
    }

    while(size>=1){
        printf("%d ", extractMin(heapArray, &size));
    }
    return 0;
}
