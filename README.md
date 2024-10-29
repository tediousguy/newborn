# newborn
#include<stdio.h>
int main()
{
int n,a,count=0,sum=0;
scanf("%d",&n);
while(n!=0){
a=n%10;
n=n/10;
sum+=a;
count++;
}
printf("%d %d",count,sum);
return 0;
}
