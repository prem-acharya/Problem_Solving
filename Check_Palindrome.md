# C Program to Check Whether a Number is Palindrome or Not

```C Code

#include <stdio.h>
int main() {
  int n, reversed = 0, remainder, original;
    printf("Enter an integer: ");
    scanf("%d", &n);
    original = n;

    // reversed integer is stored in reversed variable
    while (n != 0) {
        remainder = n % 10;
        reversed = reversed * 10 + remainder;
        n /= 10;
    }

    // palindrome if orignal and reversed are equal
    if (original == reversed)
        printf("%d is a palindrome.", original);
    else
        printf("%d is not a palindrome.", original);

    return 0;
}
```

Output:

![image](https://github.com/prem-acharya/Problem_Solving/assets/102874190/8b9fef2b-8d8d-4dd7-839d-209fa2a2081f)
