# Given a number n then print n terms of fibonacci series in reverse order.

Examples: 
```
Input : n = 5
Output : 3 2 1 1 0

Input : n = 8
Output : 13 8 5 3 2 1 1 0
```

C Code:
```C
#include <stdio.h>

int main() {
    int n;

    printf("Enter the number: ");
    scanf("%d", &n);

    if (n <= 0) {
        printf("Invalid input.\n");
        return 1;
    }

    int fib[n];
    fib[0] = 0;
    fib[1] = 1;

    // Generate the Fibonacci series
    for (int i = 2; i < n; i++) {
        fib[i] = fib[i - 1] + fib[i - 2];
    }

    // Reverse the Fibonacci series
    printf("Reversed Fibonacci series: ");
    for (int i = n - 1; i >= 0; i--) {
        printf("%d ", fib[i]);
    }
    printf("\n");

    return 0;
}
```
