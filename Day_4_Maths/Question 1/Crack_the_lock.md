# Problem Statement 1

You will be provided with the current state and the required state(password) of a combination lock. The password will be an alphanumeric sequence, provided by the user. The transition from current to required state can be achieved by rotation of each dial to match the required state, in either clockwise or anticlockwise sense. Task is to find out the minimum number of rotations required, for all dials combined, to reach the required state.

**Input**

x -> length of the combination lock

c[x] -> current state of the combination lock

r[x] -> password of the combination lock

```
where c[x] and r[x] can both contain a sequence with letters from 
a,b,c........x,y,z and digits from 0,1,2.....7,8,9.
```

**Output**

Single integer returning the minimum number of rotations to reach the password

## Testcases

**Input:**

    3
    a9z
    z1a

**Output:**

    4
    
**Explanation:**

> a -> z (In 1 step) 
> 
> 9 -> 1 (First step 0, Second step 9 ; total 2 step)
> 
> z -> a (In 1 step)

**Input :**

    5
    a1z3c
    z9p9z

**Output :**

    20

**Explanation :**

As a->z requires 1 rotations anticlockwise;

1->9 requires 2 rotations anticlockwise;

z->p requires 10 rotations anticlockwise; 

3->9 requires 4 rotations minimum and 

c->z requires 3 rotations

Total 20 Rotations Minimum
