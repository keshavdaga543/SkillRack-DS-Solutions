#include<stdio.h>

void swap(int *a, int *b)
{
    int temp = *a;
    *a = *b;
    *b = temp;
}

int maxIndex(int arr[],int x, int y){
    return arr[x] >= arr[y] ? x:y;
}

void buildMaxHeap(int arr[], int size, int curIndex)
{
    int maxChildIndex=maxIndex(arr,curIndex*2, curIndex*2+1 > size ? curIndex*2:curIndex*2+1);
    if(arr[maxChildIndex] > arr[curIndex]){
        swap(&arr[maxChildIndex], &arr[curIndex]);
        //Now swapped. So change
        curIndex = maxChildIndex;
        if(curIndex <= size/2){
           buildMaxHeap(arr, size, curIndex);
        }
    }
}


int extractMax(int arr[],int *size){
    int maxVal=arr[1];
    arr[1]=arr[*size];
    (*size)--;
    buildMaxHeap(arr,*size,1);
    return maxVal;
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
        buildMaxHeap(heapArray, size, index);
    }

    while(size>=1){
        printf("%d ", extractMax(heapArray, &size));
    }
    return 0;
}
