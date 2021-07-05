# c
#include<stdio.h>
int main()
{
	int a[]={1,2,3,4,5,6,7,8,9,10};
	int x;             
	int sz = sizeof(a)/sizeof(a[0]);  //数组长度
	int left = 0;              //起始的左下标 
	int right = sz-1;          //起始的右下标  
	printf("请输入要找的元素\n");
	scanf("%d",&x);          //输入要找的元素 
	while(left<=right)
	{
		int mid = (right+left)/2;  //中间元素下标
		
		if(a[mid]>x)
		{
			right = mid-1;    //设定新的范围下标 
		}
		else if(a[mid]<x)
		{
			left = mid+1;    //设定新的范围下标 
		}
		else
		{
			printf("找到了,数组下标是%d",mid);
			break;
		}
	}
	if(left>=right)
	{
		printf("找不到\n");
	}
	return 0;
}
