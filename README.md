#include <stdio.h>
#include <math.h>
int main()
{
	int ch,i;
	float a,b,c;
	char g;
	do{
		printf("Please enter the operation type:\n---------------------------------------------\n");
	printf("1 to add\n2 to substract\n3 to multiply\n4 to divide\n5 to power\n6 to square root\n---------------------------------------------\n");
	scanf("%d",&ch);
	for(i=1;i<=6;i++){
		if(i==ch) break;
	}
	
	if(i==7) {
	printf("You've entered the wrong number !\n");
	return 0;
	}
	
	if(ch!=6) {
	printf("Please enter the numbers:"); scanf("%f%f",&a,&b);
	}
	else{
	printf("please enter the number:"); scanf("%f",&c);
	}
 
	switch(ch){
		case 1:printf("%.2f + %.2f=%.2f\n",a,b,a+b);
				 break;
		case 2:printf("%.2f - %.2f=%.2f\n",a,b,a-b);
				 break;
		case 3:printf("%.2f * %.2f=%.2f\n",a,b,a*b);
				 break;
		case 4:if(b==0)printf("You cannot divide any number to 0 !\n");
				 else printf("%.2f / %.2f=%.2f\n",a,b,a/b);
				 break;
		case 5:printf("%.2f's %.2f. power is %.2f\n",a,b,pow(a,b));
				 break;
		case 6:if(c>=0) printf("square root of %.2f is %.2f\n",c,sqrt(c));
				 else printf("invalid number(negative number)\n");
				 break;
	}
	printf("Do you want to start again? Y/N\n");
	g=getch();
	}
	while(g=='y'||g=='Y');
}
