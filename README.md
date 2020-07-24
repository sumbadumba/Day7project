# Day7project

//pointer

#include<stdio.h>
#include<iostream>

using namespace std;


//void Function(int * value)//인트형 포인터에 상수를 받는다.
//{
//	*value += 10;
//
//}
//
//
//
//int main()
//{
//	int value = 10;
//	printf("vlaue 의 값 : %d\n", value);
//
//	Function(&value);//주소를 보내야 한다.
//
//
//	printf("Function 실행 후 value 의 값 : %d \n", value);
//
//	
//	return 0;
//}

//void Swap(int * a, int * b)//정렬을 할 때(sort버블)를 구현 할 때 사용함.
//{
//	int temp = *a;
//	*a = *b;
//	*b = temp;
//
//
//
//}
//
//int main()
//{
//	int a = 10;
//	int b = 20;
//
//	printf("a = %d, b = %d\n", a, b);
//
//	Swap(&a, &b);
//
//	printf("after\na = %d, b = %d \n", a, b);
//
//	//ubt
//
//}


//int main()
//{
//
//	char arr[] = { 'a','b','c','d','e' };//char형은 1byte이다.
//	char * ptr = arr;
//
//	//int arr[] = { 1,2,3,4,5 };
//	//int * ptr = arr;
//
//	printf("arr = %X \n", arr);
//	printf("&arr[0]의 값 : %X \n", &arr[0]);//%x를 소문자로 쓰면 16진수도 소문자로 나온다.
//
//	printf("ptr + 0 : %x\n", ptr + 0);//주소를 찍는다.
//	printf("ptr + 1 : %x\n", ptr + 1);//주소를 나오게하는..
//	printf("ptr + 2 : %x\n", ptr + 2);
//	printf("ptr + 3 : %x\n", ptr + 3);
//	printf("ptr + 4 : %x\n", ptr + 4);
//	printf("\n");
//
//
//	printf("*(ptr + 0) : %c\n", *(ptr + 0));
//	printf("*(ptr + 1) : %c\n", *(ptr + 1));
//	printf("*(ptr + 2) : %c\n", *(ptr + 2));//값을 나오게 한다.
//	printf("*(ptr + 3) : %c\n", *(ptr + 3));
//	printf("*(ptr + 4) : %c\n", *(ptr + 4));//메모리가 샌다는 말은 해제를 해야 할 메모리를 해제안해서 나온 말이다.
//	//pointer는 동적할당이 어렵다.
//
//
//
//
//}

//main 1
//#include<stdio.h>
//#include<time.h>
//#include<math.h>
//#include<stdlib.h>
//
//
////배열의 주소를 
//void PrintArray(int * arr, int width,int height)//배열을 함수로 받을 때 pointer를 받는 방법이다. : int * arr
//{//pointer에 주소를 넘긴 것이다.
//	printf("\n");
//
//	for (int i = 0; i < height; i++)
//	{
//		for (int j = 0; j < width; j++)
//		{
//			printf("%d\t", arr[i * 5 + j]);//인덱스 5부터 찍는다.그러니 총 5번 찍는거임.
//			
//		}
//		printf("\n");
//	}
//
//}
//int main()
//{
//	// 5X5
//	const int numCount = 25;
//	int arr[numCount];
//	//배열초기화
//	for (int i = 0; i < numCount; i++)
//	{
//		arr[i] = i + 1;
//
//	}
//	//배열을 출력
//
//
//
//	//랜덤씨드
//	srand(time(NULL));
//
//	//srand((unsigned int)time(NULL));
//
//	//램덤과 스왑을 이용해서 마구 섞는다.
//	for (int i = 0; i < 100; i++)
//	{
//		int rndIndex1 = rand() % numCount;// 0 ~ 24
//
//		int rndIndex2 = rand() % numCount;// 0 ~ 24
//		//스왑
//		int temp = arr[rndIndex1];
//		arr[rndIndex1] = arr[rndIndex2];
//		arr[rndIndex2] = temp;
//
//	}
//	//섞인 배열을 출력
//	PrintArray(arr, 5, 5);
//
//
//
//	while (true)
//	{
//		int input = 0;
//		printf("\n숫자를 입력하세요. ");
//		scanf("%d", &input);// scanf의 input 은 &주소값을 받는다.
//		
//		PrintArray(arr, 5, 5);
//		system("cls");
//		for (int i = 0; i < numCount; i++)//입력된 숫자를 0으로 초기화 한다.
//		{
//			if (arr[i] == input)
//			{
//				arr[i] = 0;
//			}
//		}
//
//		for (int i = 0; i < 5; i++)
//		{
//			for (int j = 0; j < 5; j++)
//			{
//				if (arr[i * 5 + j] != 0)
//				{
//					printf("%d\t", arr[i * 5 + j]);
//				}
//				else
//					printf("# \t");//0으로 초기화 한 숫자를 #으로 만들어 버린다.
//			}
//			printf("\n");
//
//		}
//		//PrintArray(arr, 5, 5);
//
//	}
//	return 0;
//
//}

//main2

//#include<stdio.h>
//
//
//int main()
//{
//
//	const int Width = 3;
//	const int Height = 5;
//
//	int arr[Width][Height];
//
//	for (int i = 0; i < Height; i++)
//	{
//		for (int j= 0; j < Width; j++)
//		{
//			arr[i][j] = (i * Width )+ (j + 1);
//
//		}
//	}
//
//	for (int i = 0; i < Height; i++)
//	{
//		for (int j = 0; j < Width; j++)
//		{
//			printf(" %d\t",arr[i][j]);
//		}
//		printf("\n");
//
//	}
//	printf("\n");
//
//
//	int * ptr = arr[1];
//
//	printf("arr의 값 : %d\n", arr);
//	printf("&arr[0]의 값 : %d\n", &arr[0]);
//	printf("&arr[1]의 값 : %d\n", &arr[1]);
//	printf("&arr[2]의 값 : %d\n", &arr[2]);
//
//	printf("\n");
//
//	printf("ptr + 0 : %d\n", ptr + 0);
//	printf("ptr + 1 : %d\n", ptr + 1);
//	printf("ptr + 2 : %d\n", ptr + 2);
//	printf("\n");
//
//	ptr = arr[1];
//
//	printf("ptr = %d\n", ptr);
//	printf("ptr의 값 : %d\n", *ptr);
//	printf("*(ptr+1)의 값 %d\n", *(ptr + 1));
//	printf("*(ptr+2)의 값 %d\n", *(ptr + 2));
//
//
//	return 0;
//
//}

//doublepointer.cpp

#include<stdio.h>

int main()
{
	int a = 45;
	int * ptr = &a;
	int **pptr = &ptr;//포인터형 변수에 주소를 넣을때 쓰인다.


	printf("a = %d\n",a);
	printf("&a = %d\n", &a);
	printf("ptr = %d\n", ptr);
	printf("*ptr = %d\n",*ptr);
	printf("pptr = %d\n", pptr);//이중포인터에 별을 안쓰면 이중포인터의 주소가 나온다.
	printf("*pptr = %d\n", *pptr);//이중포인터에 별하나를 붙이면 ptr의 주소(a의 주소가 나온다.)
	printf("**pptr = %d\n", **pptr);

	// # 숙제 1
	// 1차원 배열에 1~30(30개)까지 숫자를 입력
	// 출력 후 홀수 짝수의 배열상의 위치를 바꾸어 출력
	
	// # 숙제 2
	// 컴퓨터가 가위/바위/보 중 하나를 선택
	// 사용자로부터 가위/바위/보 중 하나를 입력받을 것
	// 사용자가 컴퓨터를 이길때 까지 게임으 지속
	// (사용자가 이기면 바로 종료)
	// 20회의 게임 중 사용자가 컴퓨터를 못이기면 게임 종료

	// # 조사 숙제 3
	// 시프트 연산자를 이용한 Swap 함수를 찾을것
	// link를 따가지고 텍스트파일에 복사해도되는데
	// 프로그램을 짜는게 좋음
}
