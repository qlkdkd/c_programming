1. 간단한 카운트 다운 프로그램을 작성하여 보자. 60초부터 0초까지 숫자를 출력하고 0초가 되면 "발사"를 출력한다.
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
#include<time.h>

int main() {
	for (int i = 60; i >= 0; i--) {
		printf("%d ", i);

	}
	printf("발사\n");

	return 0;
}
```
![image](https://github.com/user-attachments/assets/2e506f76-edeb-4f99-a6f6-e51e28bb78a1)

2. 사용자로부터 반복 횟수를 받아서 그 수만큼 "안녕하세요"를 출려ㅑㄱ하는 프로그램을 완성해보자.
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int n;
	printf("몇 번이나 반복할까요? ");
	scanf("%d", &n);

	for (int i = 0; i < n; i++) {
		printf("안녕하세요\n");
	}
	return 0;
}
```
![image](https://github.com/user-attachments/assets/727e71fb-1d7e-4886-ad89-15797916621b)

3. 다음과 같은 출력을 생성하는 프로그램을 작성해보자.
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int j;
	for (int i = 1; i <= 7; i++) {
		for (j = 1; j <= i; j++){
			printf("%d", j);
		}
		for (int k = 7; k >= j; k--) {
			printf("*");
		}
	printf("\n");
	}
	return 0;
}
```
![image](https://github.com/user-attachments/assets/6d39db06-48fa-464d-92c6-ae242ca7b0aa)

4. 사용자로부터 정수를 입력받아서 계속 더하는 프로그램을 작성해보자. 사용자가 0을 입력하면 입력된 모든 정수의 합계를 출력하고 종료한다.
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int num;
	int sum=0;
	do {
		printf("정수를 입력하시오: ");
		scanf("%d", &num);
		sum+= num;
	} while (num != 0);
	printf("%d\n", sum);
}
```
![image](https://github.com/user-attachments/assets/0e17366a-316e-4d0f-a5a8-cc88228fbd60)


5. 1부터 100까지의 자연수 중에서 3의 배수를 출력하여 보자

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	for (int i = 3; i < 100; i += 3) {
		printf("%d ", i);
	}

	return 0;
}
```
![image](https://github.com/user-attachments/assets/70a163a3-587b-4c91-8a30-1e6b85b7d772)


6. 1부터 100까지의 자연수 중에서 3의 배수이면서 동시에 5의 배수인 숫자를 출력하여 보자
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

//3의배수이면서 5의 배수인 수=3과 5의 공배수=15의 배수
int main() {
	for (int i = 3 * 5; i < 100; i += (3 * 5)) {
		printf("%d ", i);
	}
	return 0;
}
```
![image](https://github.com/user-attachments/assets/dcc5fd25-b714-401c-829d-3ffe8af88faf)


7. 사용자로부터 정수 x, y를 입력받아서 x에서 y까지의 합을 구하는 프로그램을 작성하라.
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int start, end, sum=0;

	printf("시작정수: ");
	scanf("%d", &start);

	printf("종료정수: ");
	scanf("%d", &end);

	for (int i = start; i <= end; i++) {
		sum = sum + i;
	}
	printf("%d부터 %d까지의 합: %d\n", start, end, sum);
	return 0;
}
```
![image](https://github.com/user-attachments/assets/ac655df2-5bef-479b-a280-d12a27e674e9)


8. 아스키코드 표를 출력하는 프로그램을 작성해보자.

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	for (int i = 65; i <= 90; i++) {
		printf("%d:		%c\n", i, i);
	}

	return 0;
}
```
![image](https://github.com/user-attachments/assets/0e5ad0fc-f7c2-4f20-a329-d3d09a55d431)


9. 반복적으로 사용자에게서 문자를 받아서 'a'가 나오면 카운터를 하나씩 증가한다. 사용자가 '.'을 입력하면 반복을 종료하고 입력한 'a'의 총 개수를 출력한다. 문자를 입력받을 때는 'getchar()'함수를 사용한다.

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
#include<string.h>

int main() {
	char a  ;
	int count=0;
	do {
		printf("문자를 입력하시오(종료 .): ");
		a=getchar();
		getchar();
		if (a == 'a') {
			count++;
		}
	} while (a != '.');
	printf("a의 개수: %d\n", count);
	return 0;
}
```
![image](https://github.com/user-attachments/assets/c8c6c53f-ef6a-452f-9310-3a3fafec6d76)


10. 반복문을 이용하여 화씨 온도 0도부터 100까지의 구간에 대하여 10도 간격으로 섭씨 온도로 환산하는 표를 작성하라.
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	printf("============\n");
	printf("화씨온도		섭씨온도\n");
	printf("============\n");

	for (double F = 0;F <= 100; F++) {
		double C = (F - 32.0) * 5.0 / 9.0;
		printf("%.0lf		%.2lf\n", F, C);
	}
	return 0;
}
```
![image](https://github.com/user-attachments/assets/7afb50e8-92fe-487b-b736-c272f587340b)


11. 중첩 반복문을 사용하여 다음과 같이 출력하는 프로그램을 작성하여 보자.

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int n;
	printf("정수를 입력하시오: ");
	scanf("%d", &n);

	for (int i = 1; i <= n; i++) {
		for (int j = 1;  j <= i; j++) {
			printf("%d ", j);
		}
		printf("\n");
	}

	return 0;
}
```
![image](https://github.com/user-attachments/assets/0bc2ccd8-dd53-43dd-acf2-1ccb57663683)


12. 컴퓨터는 막대 그래프를 그리는 데도 사용된다. 사용자로부터 1부터 50사이의 숫자 10개를 받아서 숫자만큼의 별표를 출력하는 프로그램을 작성하라. 막대는 가로로 그려지게 된다.

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int n;

	for (int i = 0; i < 10; i++) {
		printf("데이터를 입력하시오: ");
		scanf("%d", &n);
		for (int j = 0; j < n; j++) {
			printf("*");
		}
		printf("\n");
	}

	return 0;
}
```
![image](https://github.com/user-attachments/assets/e52fb828-6e11-4ddc-8dbb-5310247ffe87)


13. 피보나치 수열을 계산하는 프로그램을 작성해보자. 피보나치 수열은 0과 1부터 시작하며 앞의 두 수를 더하여 뒤 수를 만든다.

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int n;
	printf("몇 번째 항까지 구할까요?: ");
	scanf("%d", &n);

	int fib1 = 0, fib2 = 1, fib;
	for (int i = 2; i <= n; i++) {
		fib = fib1 + fib2;
		printf("%d, ", fib);
		fib1 = fib2;
		fib2 = fib;
	}
	return 0;
}
```
![image](https://github.com/user-attachments/assets/f2be63ec-5718-475a-8fee-e234a172afc3)


14. $1^2+2^2+3^2+...+n^2$의 값을 계산하여 출력하여 보자

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int n, sum=0;
	printf("n의 값을 입력하시오: ");
	scanf("%d", &n);

	for (int i = 1; i <= n; i++) {
		sum += (i*i);
	}
	printf("계산 값은 %d입니다.\n", sum);
	return 0;
}
```
![image](https://github.com/user-attachments/assets/95527c1c-cbce-4645-b753-a34610bba32e)


15. 자동차의 연료 탱크 프로그램을 시뮬레이션해보자. 초기값이 1000리터이고 사용자가 주행을 하면 연료가 줄어든다. 반복문을 사용하여 사용자가 충전 또는 사용한 연료를 입력받아서 연료 탱크에 남아있는 연료가 10% 미만이면 경고를 출력한다.

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int n, add;
	printf("초기 연료량: ");
	scanf("%d", &n);

	do {
		printf("연료 충전은 +, 소모는 -로 입력해주세요: ");
		scanf("%d", &add);
		n += add;
		printf("현재 남아있는 양은 %lf입니다.\n", (double)n);
	} while (n >n * 0.1);
	printf("(경고) 연료가 10%% 이하입니다.\n");

	return 0;
}
```
![image](https://github.com/user-attachments/assets/91538f15-fdd3-4d7b-b0e0-774010393e15)


16. 사용자가 입력한 수가 소수인지 아닌지를 출력하는 프로그램을 작성하라. 소수는 1과 자기 자신 이외에는 약수를 가지지 않아야 한다. 약수는 %연산자를 이용하여 검사할 수 있다. 즉 i가 5의 약수이려면 i%5==0이여야 한다.
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int n, prime = 0;
	printf("정수를 입력하시오: ");
	scanf("%d", &n);

	for (int i = 2; i <= n; i++) {
		if (n % i == 0) {
			prime = 1;
		}
	}
	if (prime == 1) {
		printf("%d는 소수가 아닙니다.\n", n);
	}
	else {
		printf("%d는 소수입니다.\n", n);
	}

	return 0;
}
```
![image](https://github.com/user-attachments/assets/f812e382-c9a4-4fbb-a677-e3de0e93eb0c)


17. 피타고라스의 정리는 직각삼각형에서 직각을 낀 두 변의 길이를 a, b라 하고, 빗변의 길이를 c라고 하면 $a^2+b^2=c^2$의 수식이 성립한다는 것이다. 각변의 길이가 100보다 작은 작은 삼각형 중에서 피타고라스의 정리가 성립하는 직각 삼각형은 몇 개나 있을까? 3중 반복문을 이용하여 피타고라스의 정리를 만족하는 3개의 정수를 찾도록 한다.

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	for (int i = 1; i < 100; i++) {
		for (int j = 1; j < 100; j++) {
			for (int k = 1; k < 100; k++) {
				if (i * i + j * j == k * k) {
					printf("%d %d %d\n", i, j, k);
				}
			}
		}
	}

	return 0;
}
```
![image](https://github.com/user-attachments/assets/7f9be00d-fe24-4aea-9669-0cb5cadf1c80)


18 라스베가스에서 50달러를 가지고 도박을 하는 사람이 있다. 한 번의 도박에 1달러를 건다고 가정하자. 돈을 따거나 잃을 확률은 0.5로 동일하다고 가정하자. 도박사는 가진 돈을 다 잃거나 목표 금액인 250달러에 도달하면 도박을 중지한다. 도박사가 목표 금액에 도달하는 확률이 얼마나 되는지를 계산해보자.
