
# Pattern 2 Solution


**Difficulty: Easy**
**Pre-Requisites: Basic Functions**
## Explanation
 In the given question we have to print the time of clock in 7-segment format. 
We can write 7 different functions for each line of the output. The first function will take in the number as parameter and print the pattern corresponding to that number on first line. Rest of the functions also have a similar working.

## Example
If the input is "1900", then we will pass in 1,9,0,0 to first function. It will print "   ." corresponding to "1", then it will print "...." corresponding to 9 and then "...." again for 0. 
Then we will repeat this step for rest of the lines by passing the number as parameter to remaining functions.
**Example input:**

> 1900

**Example Output:**

```
   .  ....   ....  ....
   .  .  .   .  .  .  .
   .  .  .   .  .  .  .
   .  ....   .  .  .  .
   .     .   .  .  .  .
   .     .   .  .  .  .
   .  ....   ....  ....  

```

```
Code:
void s1(int num)
{
	if(num==1)
		cout<<"   . ";
	else if(num==4||num==6)
		cout<<".    ";
	else	
		cout<<".... "; 
}

void s23(int num)
{
	if(num==0||num==8||num==9)
		cout<<".  . ";
	else if(num==2||num==3||num==7||num==1)
		cout<<"   . ";
	else
		cout<<".    ";
}

void s4(int num)
{
	if(num==1||num==7)
		cout<<"   . ";
	else if(num==0)
		cout<<".  . ";
	else
		cout<<".... "; 
}

void s56(int num)
{
	if(num==2)
		cout<<".    ";
	else if(num==6||num==8||num==0)
		cout<<".  . ";
	else
		cout<<"   . ";
}

void s7(int num)
{
	if(num==1||num==4||num==7||num==9)
		cout<<"   . ";
	else 
		cout<<".... ";
}

int main()
{
	#ifndef ONLINE_JUDGE
	// for getting input from input.txt
	freopen("input.txt", "r", stdin);
	// for writing output to output.txt
	freopen("output.txt", "w", stdout);
	#endif

	ios::sync_with_stdio(false);
  	cin.tie(0);

  	string str;
  	cin>>str;
  	for(int i=0;i<str.size();i++)
  		s1(str[i]-'0');
  	cout<<endl;
  	for(int i=0;i<str.size();i++)
  		s23(str[i]-'0');
  	cout<<endl;
  	for(int i=0;i<str.size();i++)
  		s23(str[i]-'0');
  	cout<<endl;
  	for(int i=0;i<str.size();i++)
  		s4(str[i]-'0');
  	cout<<endl;
  	for(int i=0;i<str.size();i++)
  		s56(str[i]-'0');
  	cout<<endl;
  	for(int i=0;i<str.size();i++)
  		s56(str[i]-'0');
  	cout<<endl;
  	for(int i=0;i<str.size();i++)
  		s7(str[i]-'0');
}
```
