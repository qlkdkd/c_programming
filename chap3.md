1. 사용자로부터 소수점 표기 형식으로 실수를 읽어서 지수 형식으로 출력하는 프로그램을 작성하여라
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	double num;
	printf("실수 입력: ");
	scanf("%lf", &num);

	printf("지수 형식으로는 %le\n", num);
	return 0;
}
```
![image](https://github.com/user-attachments/assets/868fe7c0-fac6-48f0-b3f6-00cdf538712b)


2. 사용자로부터 지수형식으로 실수를 읽어서 소수점 표기 형식으로 출력하는 프로그램을 작성하라.
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	double num;
	printf("지수형식으로 실수를 입력하시오: ");
	scanf("%le", &num);

	printf("소수점 표시 형식으로는 %lf 입니다.\n", num);
	return 0;
}
```
![image](https://github.com/user-attachments/assets/a602f786-8dcb-4b45-b12f-b105d3f0c6d2)


3. 사용자로부터 반지름이 주어지면 구의 표면과 부피를 계산하는 프로그램을 작성해보자. 파이는 기호상수 PI로 정의해서 사용해 보자.
```c
int main() {
	const double PI = 3.14;
	double radius;
	printf("반지름 입력: ");
	scanf("%lf", &radius);

	printf("구의 표면적: %lf\n", 4.0 * PI * (radius * radius));
	printf("구의 부피: %lf\n", 4.0 / 3.0 * PI * (radius * radius * radius));
	return 0;
}
```
![image](https://github.com/user-attachments/assets/789624bb-1de2-4e4e-8328-5d30f7094894)


4. 사용자로부터 x의 값을 실수로 입력받아서 다음과 같은 다항식의 값을 계산하는 프로그램을 작성하여라
$$3x^3-7x^2+9$$
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	double x;
	printf("x값을 입력하시오: ");
	scanf("%lf", &x);
	double result = 3 * x * x * x - 7 * x * x + 9;
	printf("다항식의 값: %lf", result);
	return 0;
}
```
![image](https://github.com/user-attachments/assets/c11cbe34-cbf8-404f-aa80-764f27a06123)


5. 사용자로부터 문자를 받아서 아스키코드로 출력하는 프로그램을 작성하여라
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	char a;
	printf("문자 입력: ");
	scanf("%s", &a);
	printf("아스키코드: %d", a);
	return 0;
}
```
![image](https://github.com/user-attachments/assets/20e90d7f-a180-4ff5-a43f-ccfc9dc0bee9)


6. 사용자에게 받은 문자 3개를 저장하였다가 역순으로 출력해보자. 반복 구문과 배열은 사용하지 않는다.
``` c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	char a, b, c;
	printf("문자를 입력하시오: ");
	scanf("%c %c %c", &a, &b, &c);

	printf("문자: %c, %c, %c", c, b, a);
	return 0;
}
```
![image](https://github.com/user-attachments/assets/00a6234c-b576-4bc1-8610-7913fc83e12d)

7. 이번 장에서 학습한 모든 자료형의 크기를 sizeof 연산자를 사용하여 출력하는 프로그램을 작성하라
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	printf("char형의 크기는 %d입니다.\n", sizeof(char));
	printf("short형의 크기는 %d입니다.\n", sizeof(short));
	printf("int형의 크기는 %d입니다.\n", sizeof(int));
	printf("long형의 크기는 %d입니다.\n", sizeof(long));
	printf("long long형의 크기는 %d입니다.\n", sizeof(long long));
	printf("float형의 크기는 %d입니다.\n", sizeof(float));
	printf("double형의 크기는 %d입니다.\n", sizeof(double));
	printf("long double형의 크기는 %d입니다.\n", sizeof(long double));
	return 0;
}
```
![image](https://github.com/user-attachments/assets/e8631957-84be-4719-84c6-4b3caf62be89)


8. 사용자에게 자동차로 움직인 거리(미터)와 소요 시간(시간, 분, 초)을 입력받는다. 자동차의 속도를 시간당 킬로미터로 출력해보자. 기호상수도 사용해보자.
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	//속도: 거리/시간
	int meter, hour, minute, second;
	printf("거리를 미터로 입력하시오: ");
	scanf("%d", &meter);
	printf("시간을 입력하시오: ");
	scanf("%d", &hour);
	printf("분을 입력하시오: ");
	scanf("%d", &minute);
	printf("초를 입력하시오: ");
	scanf("%d", &second);

	double speed;
	speed = (double)(meter/1000) / ((double)hour + (double)minute / 60 + (double)second / 3600);
	printf("속도: %lf", speed);
	return 0;
}
```
![image](https://github.com/user-attachments/assets/10881de4-8f77-45b8-9f41-a42af5252f20)
