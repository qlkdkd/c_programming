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
