# FIND_X&Y Solution

**Problem Statement 1:** 

**Difficulty:** Easy

**Pre-Requisites:** Euclid's Algorithm: GCD

## Brief Explanation: 

This problem is an extension of Euclidean algorithm: GCD which is also known as the Extended Euclidean Algorithm.</br>
The idea is to make the use of following fact from Euclid's algorithm.</br>

> GCD(p,q) = GCD(q,p%q)

By using the base condition
> when b = 0; </br>
> x = 1, y = 0

Calculate the values of x and y backwards as 
> x = y'
> 
> y = x' - y'×floor(a/b)

where x' and y' are the coefficients for q and q%p 
> [x'×q +y'×(q%p) = GCD(q,p%q) = GCD(p,q)]

and x and y are the coefficients for p and q 
> [x×p +y×q = GCD(p,q)]

**Explanation:**

A detailed explanation of this Extended Euclidean algorithm can be found at:
> https://cp-algorithms.com/algebra/extended-euclid-algorithm.html


## Code:
Recursive Solution: This returns a pair of required x and y values
```
struct pair_xy
{
	int x,y;
};


pair_xy extendedGCD(int p, int q)
{
	pair_xy t1, t2;
	
	if(q==0)
	{
		t1.x=1;
		t1.y=0;
		return t1;
	}
	
	t1 = extendedGCD(q,p%q);
	t2.x = t1.y;
	t2.y = t1.x - (p/q)*t1.y;
	
	return t2;
}
```
> Note: Have a look at the iterative solution as well given in the explanation link.

**Time Complexity:**

>  O(log<sub>2</sub>(N)), where N is the upper limit of p & q.
