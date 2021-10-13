
# Pattern 1 Solution


**Difficulty: Easy**

## Explanation
 
**Pattern in our question** 
```
1*2*3*4*17*18*19*20
--5*6*7*14*15*16
----8*9*12*13
------10*11
```
The input in the question represents the number of lines to be printed
Each hyphen represents a space

Let's split the trapezium into two parts
>LHS
```
1*2*3*4*
--5*6*7*
----8*9*
------10*
```
>RHS
```
17*18*19*20
14*15*16
12*13
11
```
```
Pseudo Code:
void pattern(int n)
{
	int space;
	 int i, j, leftpattern, rightpattern;
	 leftpattern = 1;
	 rightpattern = n * n + 1;
	 for(i = num; i > 0; i--) 
	 {
			for(space = n; space > i; space--)
			cout <<" ";
			for(j = 1; j <= i; j++) 
			{
				cout << leftpattern;
				cout <<"*";
				leftpattern++;
			}
			for(j = 1; j <= i; j++) 
			{
				cout << rightpattern;
				if(j < i)
				cout	<<"*";
				rightpattern++;
			}
			rightpattern = rightpattern - (i - 1) * 2 - 1;
			cout << endl;
	}	
}
```
