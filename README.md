# bug
#define _CRT_SECURE_NO_WARNINGS 1
#define _CRT_SECURE_NO_WARNINGS 1

#include<stdio.h>
#include<stdlib.h>

//int main()
//{
//	int i = 0;
//	for (i = 0; i < 100; i++)
//	{
//		printf("%d ", i);
//	}
//	system("pause");//暂停
//	return 0;
//}

//F5-启动调试-和F9配合使用的

//int main()
//{
//	int i = 0;
//	int arr[10] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
//	for (i = 0; i <= 12; i++)
//	{
//		printf("hehe\n");
//		arr[i] = 0;
//	}
//	system("pause");
//	return 0;
//}

//断点 F9切换断点
//int main()
//{
//	int i = 0;
//	for (i = 0; i < 100; i++)
//	{
//		printf("%d ", i);
//	}
//
//	for (i = 0; i < 100; i++)
//	{
//		printf("%d ", 10-i);
//	}
//	system("pause");//暂停
//	return 0;
//}

//int Add(int x, int y)
//{
//	int z = 0;
//	z = x + y;
//	return z;
//}
//
//int main()
//{
//	printf("hehe\n");
//	int a = 20;
//	int b = 10;
//	int c = Add(a, b);
//	return 0;
//}

//int main()
//{
//	{
//		int tmp = 0;
//		printf("tmp=%d\n", tmp);
//	}
//	int arr[10] = { 0 };
//	int i = 0;
//	for (i = 0; i < 10; i++)
//	{
//		arr[i] = i;
//	}
//	return 0;
//}

//void test2()
//{
//	printf("hehe\n");
//}
//void test1()
//{
//	test2();
//}
//void test()
//{
//	test1();
//}
//
//int main()
//{
//	test();
//	return 0;
//}

//实例一，实现代码:求1！+2！+……+n!;不考虑溢出
// int main()
//{
//	int i = 0;
//	int sum = 0;//保存最终结果
//	int n = 0;
//	int ret = 1;//保存n的阶乘
//	scanf("%d", &n);//3  1!+2!+3!=1+2+6=9   n=3
//	for (i = 1; i <= n; i++)// i 1 2 3
//	{
//		int j = 0;
//		ret = 1;
//		for (j = 1; j <= i; j++)//  j 1 2 3
//		{
//			ret *= j;  //ret  1*1  1*1*2 1*1*2*3
//		}
//		sum += ret;  //sum 1  1+2
//	}
//	printf("%d\n", sum);
//	return 0;
//}

//int main()
//{
//	int i = 0;
//	int arr[10] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
//	for (i = 0; i < 12; i++)
//	{
//		printf("hehe\n");
//		arr[i] = 0;
//	}
//	system("pause");
//	return 0;
//}

//int main()
//{
//	int i = 0;
//	int arr[10] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
//	for ( int i = 0; i < 12; i++)//C++  C陷阱和缺陷
//	{
//		printf("hehe\n");
//		arr[i] = 0;
//	}
//	system("pause");
//	return 0;
//}

//int main()
//{
//	int i = 0;
//	int arr[10] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
//
//	printf("%p\n", arr);
//	printf("%p\n", &i);
//
//	system("pause");
//
//	for (i = 0; i < 12; i++)
//	{
//		printf("hehe\n");
//		arr[i] = 0;
//	}
//	return 0;
//}


//示范：模拟一个库函数strcpy

//版本一
//int main()
//{
//	//strcpy
//	//字符串拷贝
//	char arr1[] = "#####################";
//	char arr2[] = "bit";
//	strcpy(arr1, arr2);
//	printf("%s\n",arr2);
//	return 0;
//}

//版本二
//void my_strcpy(char* dest, char* src)
//{
//	while (*src!='\0')
//	{
//		*dest = *src;
//		src++;
//		dest++;
//	}
//	*dest = *src;//'\0'
//}
//int main()
//{
//	//strcpy
//	//字符串拷贝
//	char arr1[] = "#####################";
//	char arr2[] = "bit";
//	my_strcpy(arr1, arr2);
//	printf("%s\n", arr1);
//	return 0;
//}

//版本三
//void my_strcpy(char* dest, char* src)
//{
//	if (dest != NULL&&src != NULL)
//	{
//		while (*dest++ = *src++)
//		{
//			;
//		}
//	}
//	
//}

//版本四
#include<assert.h>

//void my_strcpy(char* dest, char* src)
//{
//	assert(dest!=NULL);//断言
//	assert(src != NULL);//断言
//
//	while (*dest++ = *src++)
//		{
//			;
//		}
//}
//
//int main()
//{
//	//strcpy
//	//字符串拷贝
//	char arr1[] = "#####################";
//	char arr2[] = "bit";
//	my_strcpy(arr1, NULL);
//	printf("%s\n", arr1);
//	return 0;
//}


//版本五
//void my_strcpy(char* dest, const char* src)//const
//{
//	assert(dest != NULL);//断言
//	assert(src != NULL);//断言
//
//	while (*dest++ = *src++)
//	{
//		;
//	}
//}
//
//int main()
//{
//	//strcpy
//	//字符串拷贝
//	char arr1[] = "###";
//	char arr2[] = "bit";
//	my_strcpy(arr1, NULL);
//	printf("%s\n", arr1);
//	return 0;
//}

//int main()
//{
//	const int num = 10;
//
//	/*const int* p = &num;
//	*p = 20;*///err    const放在指针变量的*左边时，修饰的是*p，也就是说：不能通过p来改变*p(num)的值
//	
//	/*int * const p = &num;
//	*p = 20;*///right    const放在指针变量的*右边时，修饰的是指针变量p本身，p不能被改变了
//
//	/*int n = 100;
//	p = &n;*/
//
//	printf("%d\n", num);
//
//	return 0;
//}

//版本六
//char* my_strcpy(char* dest, const char* src)//const
//{
//	char* ret = dest;
//	assert(dest != NULL);//断言
//	assert(src != NULL);//断言
//	//把src指向的字符串拷贝到dest指向的空间，包含'\0'字符	
//	while (*dest++ = *src++)
//	{
//		;
//	}
//	return ret;
//}
//
//int main()
//{
//	//strcpy
//	//字符串拷贝
//	char arr1[] = "###";
//	char arr2[] = "bit";
//
//	printf("%s\n", my_strcpy(arr1, arr2));
//
//	return 0;
//}

//int my_strlen(const char *str)
//{
//	int count = 0;
//	assert(str != NULL);//保证指针的有效性
//	while (*str != '\0')
//	{
//		count++;
//		str++;
//	}
//	return count;
//}
//int main()
//{
//	char arr[] = "abcdef";
//	int len=my_strlen(arr);
//	printf("%d\n", len);
//	return 0;
//}

//int main()
//{
//	int a = 0;
//	int *p = &a;
//	assert(p != NULL);
//	return 0;
//}

//int main()
//{
//	int a = 10;
//	int b = 20;
//	int sum = Add(a, b);
//	printf("%d\n", sum);
//	return 0;
//}//链接错误

int Add(int x, int y)
{
	return x + y;
}

int main()
{
	int a = 10;
	int b = 20;
	int sum = Add(a, b);
	printf("%d\n", sum);
	return 0;
}
