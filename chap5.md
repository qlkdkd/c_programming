1. 사용자로부터 정수를 받아서 홀수인지 짝수인지를 출력하는 프로그램을 작성하여라
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int num;
	printf("숫자를 입력하시오: ");
	scanf("%d", &num);
	if (num % 2 == 1) {
		printf("%d은(는) 홀수\n", num);
	}
	else {
		printf("%d은(는) 짝수\n", num);
	}
	return 0;
}
```
![image](https://github.com/user-attachments/assets/7a2c40f0-88ce-4522-9d23-7736abb08e6c)


2. 사용자로부터 입력받은 두 수의 합과 차를 구하여 출력하여 보자. 두 수의 차는 큰 수에서 작은 수를 뺀 것으로 간주한다.
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int a, b;
	printf("정수를 입력하시오: ");
	scanf("%d", &a);
	printf("정수를 입력하시오: ");
	scanf("%d", &b);
	printf("두 수의 합은 %d입니다.\n", a + b);
	if (a > b) {
		printf("두 수의 차는 %d입니다.\n", a - b);
	}
	else {
		printf("두 수의 차는 %d입니다.\n", b - a);
	}
	return 0;
}
```
![image](https://github.com/user-attachments/assets/c48ca870-58f4-44f9-8a14-71c14b218bb8)


3. 요일을 나타내는 숫자(0-6)을 받아서 주중인지, 주말인지를 출력하는 프로그램을 작성하라.
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int day;
	printf("요일을 0(일요일)에서 6까지의 정수로 입력하시오: ");
	scanf("%d", &day);

	if (day == 0 || day == 6) {
		printf("주말입니다.\n");
	}
	else {
		printf("평일입니다.\n");
	}

	return 0;
}
```
![image](https://github.com/user-attachments/assets/11cc12ef-59f6-4a6e-bf52-c2a7ad5ac533)


4. 문자 하나를 받아서 알파벳인지 숫자인지 특수문자인지를 출력하는 프로그램을 작성하라.
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	char c;
	printf("문자를 입력하시오: ");
	scanf("%c", &c);

	if (c >= 48 && c <= 57) {
		printf("숫자입니다.\n");
	}

	else if (c >= 65 && c <= 122) {
		printf("문자입니다.\n");
	}

	else {
		printf("특수문자입니다.\n");
	}
	return 0;
}
```
![image](https://github.com/user-attachments/assets/ab486584-0ed6-4580-9577-c7e498e5dbe0)


5. 문자를 받아서 대문자인지 소문자인지를 출력하는 프로그램을 작성하라
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	char c;
	printf("문자를 입력하시오: ");
	scanf("%c", &c);

	if (c >= 65 && c <= 90) {
		printf("대문자입니다.\n");
	}
	else if (c >= 97 && c <= 122) {
		printf("소문자입니다.\n");
	}
	return 0;
}
```
![image](https://github.com/user-attachments/assets/ff82cd14-862a-4797-aa25-4ccb6240588d)


6. 사용자가 신호등의 색깔을 입력하면 "정지", "주의", "진행"와 같은 문장을 출력하는 프로그램을 작성하여 보자
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	char signal;
	printf("신호등의 색깔 입력(R, G, Y): ");
	scanf("%c", &signal);

	if (signal == 'R') {
		printf("정지\n");
	}
	else if (signal == 'Y') {
		printf("주의\n");
	}
	else {
		printf("진행\n");
	}

	return 0;
}
```
![image](https://github.com/user-attachments/assets/fe39b0d4-b577-476f-a5bc-32e1b37efedc)
