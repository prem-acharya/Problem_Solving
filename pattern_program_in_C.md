# 1) Character Patterns

```c
#include<stdio.h>
#include<conio.h>
int main()
{
int n, x, y;
printf("Enter number of rows to show character pattern: ");
scanf("%d",&n);
for(x = 1; x <= n; x++)
{
for(y = 1; y <= x; y++)
{
printf("%c",'A' + y -1);
}
printf("\n");
}
return 0;
}
```
 - Output:-
   
   ![image](https://github.com/prem-acharya/Problem_Solving/assets/102874190/71ccbaa5-d3ee-45f1-9471-b7f801586967)

---

# 2) Right Half Pyramid Pattern in C

```c
#include <stdio.h>

int main()
{
int stars,i, j;;

printf("Enter the number of stars : ");
scanf("%d", &stars);

for (i = 1; i <= stars; i++)

{
	for (j = 1; j <= i; j++)
	{	
    	    printf("*");
	}
	printf("\n");
}

return 0;
}
```

- Output:-

  ![image](https://github.com/prem-acharya/Problem_Solving/assets/102874190/18bd79a5-6347-49d0-a51a-c43d1514e556)

