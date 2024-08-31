1. f(x, y)=1.5\*x+3.0\*y를 계산하는 함수를 작성하고 테스트하여 본다.

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int f(double x, double y) {
	return 1.5 * x + 3.0 * y;
}

int main() {
	int x = 1.0, y = 2.0;
	printf("x=%d, y=%d, f(x, y)=%d\n", x, y, f(x, y));
	return 0;
}
```
![image](https://github.com/user-attachments/assets/dcf86d22-718e-488e-8b0b-58d18e6b21e7)


2. 두 수 중에서 더 큰 수를 반환하는 함수 get_bigger()를 다음과 같이 작성하고 이것을 이용해서 사용자로부터 받은 실수 두 개 중에서 더 큰 수를 출력하는 프로그램을 작성하여 본다.

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

double get_bigger(double x, double y) {
	if (x > y)return x;
	else if (x < y) return y;
	else return 0;
}

int main() {
	double x, y;
	printf("실수 입력: "); scanf("%lf", &x);
	printf("실수 입력: "); scanf("%lf", &y);

	printf("더 큰수: %lf\n", get_bigger(x, y));
	return 0;
}
```
![image](https://github.com/user-attachments/assets/db706269-9d1e-4a6e-941b-6b22841a6970)


3. 다음과 같이 화면에 \*\*\*\*\*\*\*...을 출력하는 함수를 작성하고 이것을 호출하여서 다음과 같은 출력을 만들어 보자

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

void draw_start() {
	printf("****************************\n");
}

int main() {
	draw_start();
	return 0;
}
```
![image](https://github.com/user-attachments/assets/27faba6d-04f6-45fc-9714-57f7a89804c4)


4. 주어진 정수의 약수를 모두 찾아내는 함수 get_divisort()을 작성하여 보라. 만약 8이 주어지면 1, 2, 4, 8을 화면에 출력해야 한다. 이 함수를 테스트하기 위한 main()를 작성하여라.
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

void get_divisior(int x) {
	for (int i = x; i >= 1; i--) {
		if (x % i == 0)
			printf("%d ", x / i);
	}
}

int main() {
	int n;
	printf("정수 입력: ");
	scanf("%d", &n);
	get_divisior(n);

	return 0;
}
```
![image](https://github.com/user-attachments/assets/2be96c08-2df7-4f9c-baa7-ce64e7b68792)


5. 본문에 등장한 소수인지를 검사하는 함수 check_prime()을 사용하여 1부터 100 사이에 존재하는 소수들을 모두 출력하는 프로그램을 작성한다.
```c
#include<stdio.h>

int check_prime(int n) {
	for (int i = 2; i < n; i++) {
		if (n % i == 0)
			return 0;
	}
	return 1;
}

int main() {
	for (int i = 2; i <= 100; i++) {
		if (check_prime(i) == 1)
			printf("%d ", i);
	}
	return 0;
}
```
![image](https://github.com/user-attachments/assets/f671672b-fb19-4c9d-94a0-43ab40659d32)


6. 본문에 등장한 거듭제곱 함수 power()를 호출하여 $3^0$부터 $3^10$까지의 값을 출력하는 프로그램을 작성하여라

```c
#include<stdio.h>

int power(int x, int y) {
	int result=1;
	for (int i = 1; i <=y; i++) {
		result *= x;
	}
	return result;
}

int main() {
	for (int i = 0; i <= 10; i++) {
		printf("%d ", power(3, i));
	}

	return 0;
}
```
![image](https://github.com/user-attachments/assets/4f9fe1a5-2d84-4903-bf13-4e675fa07c0b)


7. 두 점 사이의 거리를 계산하는 함수를 작성하여 보자. 2차원 공간에서 두 점(x1, y1)와 (x2, y2)사이의 거리를 계산하는 dist_2d()를 작성하시오. 다음과 같은 두 점 시이의 거리를 계산하는 공식을 사용하여라

$$d=\sqrt{(x_1-x_2)^2+(y_1-y_2)^2}$$

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
#include<math.h>

double dist_2d(double x1, double y1, double x2, double y2) {
	return sqrt((x1 - x2) * (x1 - x2) + (y1 - y2) * (y1 - y2));
}

int main() {
	double x1, y1, x2, y2;
	printf("첫 번째 점의 좌표: ");
	scanf("%lf %lf", &x1, &y1);
	printf("두 번째 점의 좌표: ");
	scanf("%lf %lf", &x2, &y2);

	printf("두 점 사이의 거리: %lf\n", dist_2d(x1, y1, x2, y2));
	return 0;
}
```
![image](https://github.com/user-attachments/assets/13982d78-cae4-45f5-8695-4dbcbd4053e4)


8. 2차 방정식의 근을 계산하는 함수 quad_eqn()를 작성하라. quad_eqn()함수는 a, b, c를 나타내는 double형의 3개의 인수를 받는다. 판별식이 양수인 경우에만 근을 출력하라. 만약 판별식의 값이 음수이면 근이 없다는 메시지를 출력하라.

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
#include<math.h>

double quad_eqn(double a, double b, double c) {
	double D= b * b - 4 * a * c;
	if (D < 0)printf("근이 존재하지 않음\n");
	else {
		double x1 = (-b + sqrt(D)) / (2 * a);
		double x2 = (-b - sqrt(D)) / (2 * a);
		printf("첫 번째 근: %lf\n두 번째 근: %lf\n", x1, x2);
	}
}

int main() {
	double a, b, c;
	printf("2차 방정식의 계수를 구하시오: ");
	scanf("%lf %lf %lf", &a, &b, &c);
	quad_eqn(a, b, c);
}
```
![image](https://github.com/user-attachments/assets/1e0b9294-c06c-41e7-b405-66d2f53fd892)

9. 난수 생성 함수를 이용하여 컴퓨터로 여러 가지 문제를 시뮬레이션하는 것은 흔히 몬테 카를로 시뮬레이션이라고 한다. 간단한 동전 던지기 게임을 시뮬레이션하여 보자. 컴퓨터가 동전을 던지고 사용자는 앞뒤를 말한다. 컴퓨터는 난수 생성 함수를 이용하여 난수를 생성한 후에 난수가 짝수이면 동전의 앞면으로 간주하고, 홀수이면 동전의 뒷면으로 간주한다. 이것을 여러 번 반복하여 승패를 기록한다.

```c

```
