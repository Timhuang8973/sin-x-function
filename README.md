# sin-x-function
first project on Github
#include<stdio.h>
int main(void){
	double rad,n=0,up=1,down=1,x,sum;
	printf("please intput angle x in radius:");
	scanf("%lf",&rad);
	x=rad;
	while((x/down)>=1e-8||((-1)*x/down)>=1e-8)
	{
		sum+=(up/down)*x;
		n++;
		up*=(-1);
		down*=(2*n)*(2*n+1);
		x*=rad*rad;
	}
	printf("sin(x)=%.10lf",sum);
	return 0;
}
