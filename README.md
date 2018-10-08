//Christie Carranza
#include<stdio.h>
#include<stdlib.h>
#include<time.h>
#include<math.h>

int main()
{
int i, a[100], n=100;
float sum = 0, avg, std, var, standdev;


srand(time(NULL));

printf("Array[%d] with random numbers displayed from 17 and 42: \n",n);

for(i=0;i<n;i++)
{
a[i] = rand()%25+17;
printf("%d ",a[i]);
}

printf("\n");
for(i=0;i<n;i++)
{
sum = sum + a[i];
}
avg = sum/n;

for(i=0;i<n;i++)
{
std = std + pow(a[i] - avg, 2);
}

var=std/n;

standdev=sqrt(var);

printf("Average is: %0.2f\n", avg);

printf("Standard deviation is: %0.2f\n",standdev);

return 0;

}
