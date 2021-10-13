
# Pattern 2 Solution


**Difficulty: Easy**

## Explanation
 
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
