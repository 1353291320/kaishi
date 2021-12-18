# kaishi
#include "stdafx.h"
#include "string.h"

void sushu()//判断是否为素数
{
	int i,m;
	printf("请输入数字\n");
	scanf("%d",&m);
	
	for(i=2;i<=m-1;i++)
	{
		if(m%i==0)
			break;
	}
	if(i<m)
		printf("%d不是素数。\n",m);
	else
		printf("%d是素数。\n",m);
	return;
}
void zifuchuan()//进行字符串数组的链接
{
	char str1[50],str2[50];
	printf("请输入两个字符串\n");
	gets(str1);
	gets(str2);
	strcat(str1,str2);
	printf("最后的字符串为%s\n",str1);
	
}
void oushu()//判断是否为偶数
{
	int a;
	printf("请输入数字\n");
	scanf("%d",&a);
	if(a%2==0)
		printf("%d是偶数",a);
	else
		printf("%d不是偶数",a);


}
void runnian()//判断是否是闰年
{
	int m;
	printf("请输入年份：\n");
	scanf("%d",&m);
	if((m/4==0)&&(m/100!=0)||(m/400==0))
		printf("%d是闰年",m);
}
int main()
{
	int number;
	printf("进行字符数组链接请输入1，判断是否是素数请输入2，判断是否是偶数请输入3，判断书否是闰年请输入4,结束请输入5。\n");
	scanf("%d",&number);
	if(number==1)
	{
		zifuchuan();
	}
	else
		if(number==2)
		{
			sushu();
		}
		else
			if(number==3)
			{
				oushu();
			}
			else
				if(number==4)
				{
					runnian();
				}
				else
					if(number==5)
						printf("结束程序。");
	return 0;
}
