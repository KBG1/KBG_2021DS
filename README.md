# KBG_2021DS
#include <stdio.h>
int main()
{
    char charType;
    int integerType;
    float floatType;
    double doubleType;  // 각각 문자, 정수, 실수 형으로 변수 선언
    printf("Size of char: %ld byte\n",sizeof(charType));   //문자형 변수의 크기 출력 ( 1 바이트 )
    printf("Size of int: %ld bytes\n",sizeof(integerType)); //정수형 변수의 크기 출력 ( 4 바이트 )
    printf("Size of float: %ld bytes\n",sizeof(floatType)); //실수형 변수의 크기 출력 ( 4 바이트 )
    printf("Size of double: %ld bytes\n",sizeof(doubleType)); //실수형 변수의 크기 출력 ( 8 바이트 )
    printf("-----------------------------------------\n");
    printf("Size of char: %ld byte\n",sizeof(char)); 
    printf("Size of int: %ld bytes\n",sizeof(int));
    printf("Size of float: %ld bytes\n",sizeof(float));
    printf("Size of double: %ld bytes\n",sizeof(double)); //~형 변수이기 때문에 "----------------" 위의 코드와 결과 똑같음
    printf("-----------------------------------------\n");
    printf("Size of char*: %ld byte\n",sizeof(char*)); //문자형 변수의 포인터 크기 출력 ( 4 바이트 )
    printf("Size of int*: %ld bytes\n",sizeof(int*)); //정수형 변수의 포인터 크기 출력 ( 4 바이트 )
    printf("Size of float*: %ld bytes\n",sizeof(float*)); // 실수형 변수의 포인터 크기 출력 ( 4 바이트 )
    printf("Size of double*: %ld bytes\n",sizeof(double*)); // 실수형 변수의 포인터 크기 출력 ( 4 바이트 )

    printf("-----------[Kim Beom Gyu]  [2019062022]------------");
    return 0;
}
