# Problem Statement 2


**Difficulty: Easy**

## Explanation
 
In the given pattern we can see that we have to put * at left boundary, right boundary and along both diagonals.
For left boundary condition will be j == 0, for right j == n-1. 
For one diagonal you can see that at every point on the diagonal i == j property is followed and for other diagonal i+j == n-1 property is followed.

```
Pseudo Code:
void solve()
{
   int n;
   cin >> n;

   for(int i = 0;i < n;i++){
       for(int j = 0;j < n;j++){
           if(j == 0 || j == n-1){
               cout << "* ";
           }
           else if(i == j){
               cout << "* ";
           }
           else if(i+j == n-1){
               cout << "* ";
           }
           else cout << "  ";
       }
       cout << endl;
   } 

}
```
**Time Complexity:**

> O(N^2)
