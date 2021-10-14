# LCM & HCF Solution


**Difficulty: Easy**

**Pre-Requisites:** Basic Mathematics, HCF, LCM

## Explanation
 
**Mathematical Formulae** 

> For any two numbers  m,n
>  M*N = hcf(m,n)*lcm(m,n)

**In our question** 

> X = lcm(a,b) 
> Y = Hcf(a,b) 
> Z = a+b

Now in our solution we will loop  from 1 to z and for every number i in the range 1 to z 
	A = i
	B = z-i

Because A+B  = Z
We will check if lcm and hcf of A and B are equal to X and Y if it is so we will push it in our array and then break the loop and return it 

```
Pseudo Code:
void printNumbers(int x,int y, int z)
{
  for(int i = 1; i<=z/2;i++)
  {
    int first = i;
    int second = z-i;
    int hcf = __gcd(first,second);
    long long mult = first*second;
    int lcm  = mult/hcf;
    if(lcm==x && hcf==y)
    {
      cout<<i<<” ”<<z-i;
      break;
    }
  }
}
```
**Time Complexity:**

> O(Z*log2N), where N is the upper limit of A & B.
