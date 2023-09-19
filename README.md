# Determines-the-prime-sum-and-outputs-the-factor
Determines the prime sum and outputs the factor

#define _CRT_SECURE_NO_WARNINGS 1

#include<stdio.h>

char gudge(int x)
{
	int t = 0;
	int arr[1000] = {0};
	int w = 0;
	int index = 0;//变量创造
	for (int a=2; a < x; a++)
	{
		if (x % a == 0)
		{
			w++;
			arr[index] = a;
			if (index < 999)//防止因数过多超过数组的最大容量
			{
				index++;
			}
			else
			{
				printf("所选的数过大，无法确定所有因数，以下是部分因数");
			}
		}
	}
	if (w == 0)//判断素和
	{
		printf("%d是素数", x);
	}
	else
	{
		printf("%d是和数.", x);
		printf("其因数分别为");
		for (; t < index; t++)//输出所有因数
		{
			printf("%d,",arr[t]);
		}
	}
	return 0;
}

int main()
{
	int num1 = 0;
	printf("请输入一个数");
	scanf("%d", &num1);
	gudge(num1);
	return 0;
}
