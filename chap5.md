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


7. 삼각형의 세 변의 길이를 입력받아서 삼각형의 종류를 결정하는 프로그램을 작성하라. 많은 종류 중에서 정삼각형, 이등변삼각형만 구별하여 보자.

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int a, b, c;
	printf("삼각형의 세 변을 입력하시오: ");
	scanf("%d %d %d", &a, &b, &c);
	if (a == b && b == c && c == a) {
		printf("정삼각형");
	}
	else if (a == b || b == c || c == a) {
		printf("이등변 삼각형");
	}

	return 0;
}
```
![image](https://github.com/user-attachments/assets/4228f9e1-7628-4c77-896a-e155a59a391d)


8. 근로 소득세를 계산하는 프로그램을 작성하여 보자. 근로 소득세율은 다음 표와 같다. 사용자가 자신의 과세 표준 금액을 입력하면 근로 소득세를 계산하여 주는 프로그램을 작성하여 보자. 여기서 주의해야 할 점이 있다. 만약 자신의 소득이 3000만원이면 소득 중에서 1000만원 이하는 8%를 적용하고 초과하는 부분은 17%의 세율이 매겨진다. 3000만원 전체에 대해ㅏ여 17%가 적용되는 것이 아니다.

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int  tex;
	printf("과세 표준을 입력하시오(만원): ");
	scanf("%d", &tex);

	if (tex < 1000) {
		tex = tex * 0.08;
	}
	else if (tex > 1000 && tex <= 4000) {
		tex = (tex - 1000) * 0.17 + (1000 * 0.08);
	}
	else if (tex > 4000 && tex <= 8000) {
		tex = (tex - 4000) * 0.26 + (4000 * 0.17) + (1000 * 0.08);
	}
	else {
		tex = (tex - 8000) * 0.35 + (8000 * 0.26) + (4000 * 0.17) + (1000 * 0.08);
	}

	printf("소득세는 %d만원 입니다.\n", tex);
	return 0;
}
```
![image](https://github.com/user-attachments/assets/abe09ebe-0de5-46b5-b205-9c263ecc1d6d)


9. 본문에서는 연속적인 if-else문을 이용하여 계산기를 작성하였다. 이번에는 switch문을 이용하여 간단한 계산기를 작성해보자. +, -, \*, / 연산을 지원한다.

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int a, b, res;
	char op;
	printf("수식을 입력하시오: ");
	scanf("%d %c %d", &a, &op, &b);

	switch(op){
	case '+': res = a + b; printf("%d\n", res); break;
	case '-': res = a - b; printf("%d\n", res); break;
	case '*':res = a * b; printf("%d\n", res); break;
	case '/':res = a / b; printf("%d\n", res); break;
	}

	return 0;
}
```
![image](https://github.com/user-attachments/assets/ce5286a1-9101-4044-9cb0-9f82b96013f8)


10. switch문을 이용하여 자신의 학점을 입력하면 학점에 대한 코멘트를 출력하는 프로그램을 작성해보자.

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	char score;
	printf("학점을 입력하세요: ");
	scanf("%c", &score);

	switch (score) {
	case 'A': printf("아주 잘했어요!\n"); break;
	case 'B': printf("좋습니다.\n"); break;
	case 'C': printf("만족스럽습니다.\n"); break;
	case 'D': printf("더 노력해보세요.\n"); break;
	case 'F': printf("안타깝습니다.\n"); break;
	}

	return 0;
}
```
![image](https://github.com/user-attachments/assets/c40e86e0-7aad-4661-9258-bd24573d5f4b)
