#include<stdio.h>
#include<conio.h>
#include<math.h>
int main()
{
	double a,x,sum=0.0; int n,i,fact,sign;
	printf("Enter the angle in degree:\n");
	scanf("%d",&a);
	x=a*22/7/180;
	printf("Enter the time of iteration:\n");
	scanf("%d",&n);
	sign=-1;fact=1;
	for(i=1;i<=2*n-1;i+=2)
	{
		sign=sign*(-1);
		if(i>1)
		{
		fact=fact*(i-1)*i;
		}
		sum=sum+sign*pow(x,i)/fact;
	}
	printf("The sine value of given angle is: %f",sum);
}
