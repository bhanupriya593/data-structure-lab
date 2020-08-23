Write a program that implements the following sorting methods to sort a given list of
integers in ascending order
i) Bubble sort  
#include<stdio.h>
void bubblesort(int a[100],int n)
{
       int i,j,t;
       for(i=0;i<n-1;i++)
       {
              for(j=0;j<n;j++)       
              {
                      if(a[j]>a[j+1])
                      {
                               t=a[j];
                               a[j]=a[j+1]; 
                               a[j+1]=t;
                       }
               }  
        }        
 }
int main()
{
       int n,i;
       scanf("%d",&n);
       int a[n];
       for(i=0;i<n;i++)
       {
                scanf("%d",&a[i]);
       }
       bubblesort(a,n);  
       printf("elements after sorting:\n");
       for(i=0;i<n;i++)
       {
                printf("%d\n",a[i]);
       }
}
     
  

ii) Selection sort  
#include<stdio.h>
void selectionsort(int a[100],int n)
{
       int i,j,t,min;
       for(i=0;i<n-1;i++)
       {
              min=i;
              for(j=i+1;j<n;j++)       
              {
                      if(a[j]>a[min])
                      {
                               min=j;
                               t=a[j];
                               a[j]=a[min]; 
                               a[min]=t;
                       }
               }  
        }        
 }
int main()
{
       int n,i;
       scanf("%d",&n);
       int a[n];
       for(i=0;i<n;i++)
       {
                scanf("%d",&a[i]);
       }
       selectionsort(a,n);  
       printf("elements after sorting:\n");
       for(i=0;i<n;i++)
       {
                printf("%d\n",a[i]);
       }
}


iii) Insertion sort
#include<stdio.h>
void insertionsort(int a[100],int n)
{
       int i,j,index;
       for(i=0;i<n-1;i++)
       {
              index=a[i];
              j=i;
              while((j>0)&&(a[j-1]>index))      
              {
                      a[j]=a[j-1]; 
                      j=j-1;
               } 
               a[j]=index; 
        }        
 }
int main()
{
       int n,i;
       scanf("%d",&n);
       int a[n];
       for(i=0;i<n;i++)
       {
                scanf("%d",&a[i]);
       }
       insertionsort(a,n);  
       printf("elements after sorting:\n");
       for(i=0;i<n;i++)
       {
                printf("%d\n",a[i]);
       }
}
  






