# KBG_2021DS
#include <stdio.h>
int main()
{
    int i; //정수형 변수 i 선언
    int *ptr; //1차원 포인터 배열 ptr 선언
    int **dptr; //2차원 포인터 배열 dptr 선언
    i = 1234; //i에 1234값 할당
    printf("[checking values before ptr = &i] \n"); 
    printf("value of i == %d\n", i); //i 값 출력, 1234
    printf("address of i == %p\n", &i); // i의 주소값 출력
    printf("value of ptr == %p\n", ptr); //ptr의 값 출력(할당을 받지 않아 0으로 나옴)
    printf("address of ptr == %p\n", &ptr); // ptr의 주소 출력
    ptr = &i; /* ptr is now holding the address of i */  // i의 주소를 ptr에 할당
    printf("\n[checking values after ptr = &i] \n");
    printf("value of i == %d\n", i); //i의 값 출력, 여전히 1234
    printf("address of i == %p\n", &i); //i의 주소 출력
    printf("value of ptr == %p\n", ptr); // ptr의 값에 i주소를 할당 받았으므로 위와 출력 동일
    printf("address of ptr == %p\n", &ptr); // 위의 ptr주소와 출력값 같음
    printf("value of *ptr == %d\n", *ptr); // 역참조로 i값이 출력이 됨

    dptr = &ptr; /* dptr is now holding the address of ptr */ //ptr의 주소값을 dptr에 할당
    printf("\n[checking values after dptr = &ptr] \n");
    printf("value of i == %d\n", i); //i값 출력
    printf("address of i == %p\n", &i); //위 i 주소값과 동일
    printf("value of ptr == %p\n", ptr); // i 주소값과 동일
    printf("address of ptr == %p\n", &ptr); //ptr의 주소값 출력
    printf("value of *ptr == %d\n", *ptr); //역참조로 i값 출력
    printf("value of dptr == %p\n", dptr); // dptr의 값 출력 = ptr의 주소값
    printf("address of dptr == %p\n", &dptr); // dptr의 주소값 출력 
    printf("value of *dptr == %p\n", *dptr); //역참조, i의 주소, ptr의 값과 동일 
    printf("value of **dptr == %d\n", **dptr); // 역참조로 i값 출력 (주소 기반 값이므로 i값)
    *ptr = 7777; /* changing the value of *ptr */ //ptr에 7777값 할당
    printf("\n[after *ptr = 7777] \n");
    printf("value of i == %d\n", i); //i의 주소가 ptr에 할당되었으므로 1234가 아닌 바뀐 7777값 출력
    printf("value of *ptr == %d\n", *ptr); //7777 출력
    printf("value of **dptr == %d\n", **dptr); //dptr이 ptr의 주소를 참조하므로 7777값 출력
    **dptr = 8888; /* changing the value of **dptr */
    printf("\n[after **dptr = 8888] \n");
    printf("value of i == %d\n", i);  // ptr에 할당되었던 값이 다시 8888로 변경, 따라서 i도 8888값이 출력 됨
    printf("value of *ptr == %d\n", *ptr); // dptr의 값이 ptr의 주소이므로, ptr의 값은 8888이 됨
    printf("value of **dptr == %d\n", **dptr); //8888출력

    printf("-----------[Kim Beom Gyu]  [2019062022]------------");
    return 0;
}
