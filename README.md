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





﻿// 7-74 三角形判断 
//给定平面上任意三个点的坐标(x​1,y1)、(x2,y2)、(x3,y3)，检验它们能否构成三角形。

//输入格式:
//输入在一行中顺序给出六个[−100,100]范围内的数字，即三个点的坐标x

//输出格式:
//若这3个点不能构成三角形，则在一行中输出“Impossible”；若可以，则在一行中输出该三角形的周长和面积，格式为“L = 周长, A = 面积”，输出到小数点后2位。

//输入样例1:
//4 5 6 9 7 8
  
//输出样例1:
//L = 10.13, A = 3.00

#include <stdio.h>
#include <math.h>
double pd(double x1, double y1, double x2, double y2) {
	double d = pow(pow(x2 - x1, 2) + pow(y2 - y1, 2), 0.5);
	return d;
}
int main() {
	double x1, y1, x2, y2, x3, y3, a, b, c;
	scanf("%lf %lf %lf %lf %lf %lf", &x1, &y1, &x2, &y2, &x3, &y3);
	a = pd(x1, y1, x2, y2);
	b = pd(x1, y1, x3, y3);
	c = pd(x3, y3, x2, y2);
	if (a + b <= c) goto END;
	if (a + c <= b) goto END;
	if (b + c <= a) goto END;
	double s, l;
	l = a + b + c;
	double m = 0.5 * l;
	s = pow(m * (m - a) * (m - b) * (m - c), 0.5);
	printf("L = %.2lf, A = %.2lf", l, s);
	return 0;
END:printf("Impossible");
	return 0;
}
