C Code:
```c
#include<stdio.h>
int main(){
    int a[50], i,j,n,t;
    printf("enter the No. of elements :\n");
    scanf("%d", &n);
    for(i=0; i<n; i++){
        scanf ("%d", &a[i]);
    }
    for (i=0; i<n-1; i++){
        for (j=i+1; j<n; j++){
            if (a[i] > a[j]){
                t = a[i];
                a[i] = a[j];
                a[j] = t;
            }
        }
    }
    printf ("after bubble sorting the elements are:\n");
    for (i=0; i<n; i++)
        printf("%d\t", a[i]);
    return 0;
}
```
