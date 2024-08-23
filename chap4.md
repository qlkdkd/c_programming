1. 사용자로부터 체중(kg)과 신장(m)를 받아서 BMI를 계산하여 출력하는 프로그램을 작성하라. BMI는 체중을 신장의 제곱으로 나눈 값이다. 이때 신장의 단위는 미터여야 한다.
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int weight;
	double height;
	printf("체중을 입력하시오: ");
	scanf("%d", &weight);
	printf("신장을 입력하시오(단위: 미터): ");
	scanf("%lf", &height);

	double BMI = (double)weight / (height * height);
	printf("BMI: %lf", BMI);
	return 0;
}
```
![image](https://github.com/user-attachments/assets/41158bd5-b21f-460e-a468-8d9d433c65f4)


2. 사용자로부터 3개의 정수를 받아서 변수 x, y, z에 저장하고 다음과 같은 수식의 결과를 출력하는 프로그램을 작성하라. 예를 들어서 사용자가 1, 2, 3을 입력하였다면, 1*2-3=-1을 출력하면 된다.
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int x, y, z;
	printf("정수 3개를 입력하시오: ");
	scanf("%d %d %d", &x, &y, &z);
	int result = x * y - z;
	printf("%d*%d-%d=%d\n", x, y, z, result);
	return 0;
}
```
![image](https://github.com/user-attachments/assets/65c46d75-f455-4e79-8b02-8c60bf82e2e3)


3. 사용자로부터 상품가격(정수)와 할인율(부동소수점수)를 받아서 할인된 가격을 출력하는 프로그램을 작성하라.
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int price;
	int disc_rate;
	printf("상품 가격을 입력하시오: ");
	scanf("%d", &price);
	printf("할인율을 입력하시오: ");
	scanf("%d", &disc_rate);

	double disc_price = (double)price - ((double)price * (double)disc_rate*0.01);
	printf("할인된 가격은 %.2lf 입니다.\n", disc_price);
	return 0;
}
```
![image](https://github.com/user-attachments/assets/f9f89bfe-9d02-4ac7-91db-4e78c44fa628)

4. 한 학생의 국어, 영어, 수학 점수를 입력하는 c프로그램을 작성하고 모든 과목의 합계, 평균 점수를 계산한다. 총점과 평균의 소수점 2번째 자리까지만 출력한다.
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int kor, eng, math;
	printf("3과목의 점수를 입력한다.");
	scanf("%d %d %d", &kor, &eng, &math);
	printf("총점: %.2lf\n", (double)(kor + eng + math));
	printf("평균: %.2lf\n", (double)((kor + eng + math) / 3));
	return 0;
}
```
![image](https://github.com/user-attachments/assets/6cd9dd6f-70e9-4d46-8fa8-2fffc5367c9a)


5. 사용자로부터 2개의 정수를 받아서 첫 번째 정수를 두 번째 정수로 나누었을 떄의 몫과 나머지를 계산하는 프로그램을 작성하라.
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int a, b;
	printf("첫 번째 정수를 입력하시오: ");
	scanf("%d", &a);
	printf("두 번째 정수를 입력하시오: ");
	scanf("%d", &b);

	printf("몫은 %d이고 나머지는 %d입니다.\n", a / b, a % b);
	return 0;
}
```
![image](https://github.com/user-attachments/assets/8adc97a5-e272-43dc-81d9-26ec15b7058c)

6. 세 자리로 이루어진 숫자를 입력받은 후에 각각의 자리수를 분리하고 이 자리수를 출력하는 프로그램을 작성하라
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int num;
	printf("정수를 입력하시오: ");
	scanf("%d", &num);

	int hundred = num / 100;
	int ten = num % 100 / 10;
	int one = num % 10;
	printf("백의자리수: %d\n", hundred);
	printf("십의자리수: %d\n", ten);
	printf("일의자리수: %d\n", one);
	return 0;
}
```
![image](https://github.com/user-attachments/assets/108b8d5d-c883-4dfb-bb85-919fafa2f3ee)


7. 다음 수식의 값을 계산하여 화면에 출력하라. x의 값은 사용자로부터 입력받는다.
$$f(x)=(x^3-20)/(x-7)$$
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

double f(double x) {
	return (x * x * x - 20) / (x - 7);
}

int main() {
	double x;
	printf("x값 입력: ");
	scanf("%lf", &x);

	printf("수식의 값: %lf", f(x));
	return 0;
}
```
![image](https://github.com/user-attachments/assets/adbdd0cc-6b6a-49fa-9b3b-7fa1d012185d)

8. 사용자에게 2개의 실수를 받아서 정수부를 더한 값을 출력하는 프로그램을 작성해보자.
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	double a, b;
	printf("두 개의 실수를 입력하시오: ");
	scanf("%lf %lf", &a, &b);

	int int_a = (int)a;
	int int_b = (int)b;
	int result = int_a + int_b;
	printf("합의 정수부: %d\n", result);
	return 0;
}
```
![image](https://github.com/user-attachments/assets/a726ad3e-e061-4aae-bdd4-63734cf7bb16)


9. 사용자로부터 임의의 숫자 num을 입력받아서 num의 최하위 비트(LSB)를 출력하는 프로그램을 작성하라
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int num;
	printf("숫자를 입력하시오: ");
	scanf("%d", &num);

	int LSB = num % 2;
	printf("LSB: %d\n", LSB);
	return 0;
}
```

10. 사용자로부터 임의의 숫자 num과 n을 입력받아서 num의 n번째 비트를 1로 설정하는 프로그램을 작성하라. 최하위 비트는 0번째 비트라고 하자.
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int num, n;
	printf("숫자를 입력하시오: ");
	scanf("%d", &num);
	printf("n을 입력하시오: ");
	scanf("%d", &n);

	printf("새로운 값: %d", (1 << n) | num);
	return 0;
}
```
![image](https://github.com/user-attachments/assets/08866936-1dfd-4d1a-92be-53e8f985b219)
