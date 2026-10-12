# Rotate-n-numbers-of-an-array
#include<stdio.h>
#include<stdlib.h>
void reverse (int arr[] , int si , int ei){
for(int i=si,j=ei;i<j;i++,j--){
     int temp = arr[i];
     arr[i] = arr[j];
     arr[j] = temp; } 
     }
int main()
{   int n;
    printf("enter total index number ");
    scanf("%d",&n);     
    int arr [n];
    for(int i = 0; i<=n-1; i++){
       printf("enter index no %d ",i);
       scanf("%d",&arr[i]);
    }
    int k;
    printf("enter no of changing indexes ");
    scanf("%d",&k);
    k=k%n;
    reverse(arr,0,n-1);
    reverse(arr,0,k-1);
    reverse(arr,k,n-1);
    printf("afetr changing \n");
    for(int i = 0; i<n; i++)
     { printf("%d ",arr[i]);}
    return 0;
}