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


/*用switch写五级制成绩*/
int score;
scanf("%d",&score);
switch(score/10){
		case 10:printf("A");break;
		case 9:printf("A");break;
		case 8:printf("B");break;
		case 7:printf("C");break;
		case 6:printf("D");break;
		case 5:
		case 4:
		case 3:
		case 2:
		case 1:
		case 0:printf("E");break;

	}
			return 0;
}
