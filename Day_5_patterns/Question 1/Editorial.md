# Problem Statement 1


**Difficulty: Easy**

## Explanation
 
We have to find out number of times fun appears in the subsequence.
Which means u should appear after f and n should appear after u.

So we will count how many times f appears when we are at ith index.
So when a u appears we will count how many combinations of fu can we make.
Using this u, which is at ith position we can combine it will all previous f. 
For example : In fuffu at i = 4 there is u. we have the count of f, which is 3. We can combine any with the u at ith position. So our total fu will be fu += f;
Same thing we will do with n, for every n at ith position it will make fu combinations, so we will do fun += fu.

```
Pseudo Code:
void solve(){
    string s;
    cin >> s;

    int n = s.length();

    int ans = 0;
    int f = 0;
    int fu = 0;
    int fun = 0;

    for(int i = 0;i < n;i++){
        if(s[i] == 'f')f++;
        else if(s[i] == 'u')fu += f;
        else if(s[i] == 'n')fun += fu;
    }

    if(fun == 0){
        cout << '😶';
    }
    else{
        for(int i = 0;i < fun;i++){
            cout << '😂';
        }
    }
}
```
**Time Complexity:**

> O(N)
