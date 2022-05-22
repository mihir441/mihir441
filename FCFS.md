#include <stdio.h>
#include <stdlib.h>

int main()
{
	int RQ[100],i,n,TotalHeadMoment=0,initial;
 	printf("Enter the number of Request\n");
	scanf("%d",&n);
	printf("Enter Request Sequence\n");

 	for(i=0;i<n;i++)
		scanf("%d",&RQ[i]);
	printf("Enter initial Head Position\n");
	scanf("%d",&initial);
	
	for(i=0;i<n;i++)
	{
		TotalHeadMoment=TotalHeadMoment+abs(RQ[i]-initial);
		initial=RQ[i];
	}

	printf("Total head moment is %d",TotalHeadMoment);
	return 0;

	}

