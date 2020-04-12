# prime-checker
Developed by Gunjan Narkhede
#include<stdio.h>
int prime_helper(int n,int r)
{
	int p=0,m;
	p=n%r;
    while(r>1)
	{	
	if(p==0)
	{
		m=0;
	    break;
	}		
    else if(p!=0)
	{
		m=prime_helper(n,r-1);
	}
	}
	
	 	return m;
    
}
int main()
{
	int n,z=0;
	printf("enter the number");
	scanf("%d",&n);
	if(n==1)
	{
		printf("%d is not a prime number",n);
	}
	z=prime_helper(n,n-1);
	if(z==1)
	{
		printf("%d is a prime number",n);
	}
	if(z==0)
	{
		printf("%d is not a prime number",n);
	}
	return 0;
}
