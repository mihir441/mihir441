#include<stdio.h>
#include<stdlib.h>
int n,m,alloc[10][10],avail[10],max[10][10],need[10][10],i,j;

void input()
{
        printf("enter the no of processes and no of resources");
        scanf("%d%d",&n,&m);

        printf("enter max matrix:");
        for(i=0;i<n;i++)
        {
        for(j=0;j<m;j++)
                        {
                        scanf("%d",&max[i][j]);
                        printf("\t");
                        }
        }
        
        printf(" enter the allocation matrix:");
        for(i=0;i<n;i++)
        {
                for(j=0;j<m;j++)
                {
                scanf("%d",&alloc[i][j]);
                printf("\t");
                }
        }

        printf("need matrix:");
        for(i=0;i<n;i++)
        {
                for(j=0;j<m;j++)
                {
                need[i][j]=max[i][j]-alloc[i][j];
                printf("%d",need[i][j]);
                printf("\t");
                }
                printf("\n");
        }

        printf("enter the available matrix:");
for(i=0;i<m;i++)
        {
           scanf("%d",&avail[i]);
        }
}


void display()
        {
                printf("allocation matrix:");
                for(i=0;i<n;i++)
                {
		for(j=0;j<m;j++)
	       {
                printf("%d",alloc[i][j]);
	       }        
        printf("\n");
        }
printf("\n");


        printf("max matrix");
        for(i=0;i<n;i++)
        {
                for(j=0;j<m;j++)
                {
                printf("%d",max[i][j]);
                }

        printf("\n");
        }


printf("need matrix");
        for(i=0;i<n;i++)
        {
                for(j=0;j<m;j++)
                {
                printf("%d",need[i][j]);
                 }
        printf("\n");
        }


printf("available");
for(i=0;i<m;i++)
        {
        printf("%d",avail[i]);
        }
}



int main()
{
        int choice;
        do
        {
                printf("enter your choice:");
                scanf("%d",&choice);
                switch (choice)
        {       
                case 1: input();
                        break;
                case 2: display();
                        break;
        }
}
        while(choice!=3);
}
