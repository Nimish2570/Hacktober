#include <stdio.h>
int elmntSrch(int arr[], int size, int x) {
    int rec;
    size--;
    if (size >= 0) {
        if (arr[size] == x)
            return size;
        else
            rec = elmntSrch(arr, size, x);
    }
    else
        return -1;
 
    return rec;
}
 
int main(void) {
    int arr[100];
    int size = sizeof(arr) / sizeof(arr[0]);
    int x ,n,i=0;
    int indx;
    printf("enter number of elements in array: ");
    scanf("%d",&n);
    while (i<n){
    printf("enter number to enter");
    scanf("%d",&arr[i]);
        i++;
    };
    printf("enter number you want to search:");
    
    scanf("%d",&x);
    
 
    indx = elmntSrch(arr, size, x);
 
    if (indx != -1)
        printf("Element %d is present at index %d", x, indx);
    else
        printf("Element %d is not present", x);
    return 0;
