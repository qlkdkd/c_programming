1. 배열 days[]를 아래와 같이 초기화하고 배열 원소 값을 다음과 같이 출력하는 프로그램을 작성하여라

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int days[12] = { 31, 29, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31 };
	for (int i = 0; i < 12; i++) {
		printf("%d월은 %d일까지 있습니다.\n", i + 1, days[i]);
	}
	return 0;
}
```
![image](https://github.com/user-attachments/assets/c4985321-9354-4ea1-b9b4-d823dd86ea9f)


2. 사용자로부터 n개의 정수값을 읽어서 배열에 저장하고, 다시 역순으로 출력하는 프로그램을 작성하라.

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int n, arr[100];
	printf("입력할 정수의 개수: ");
	scanf("%d", &n);

	for (int i = 0; i < n; i++) {
		printf("%d번째 요소를 입력하시오: ", i);
		scanf("%d", &arr[i]);
	}

	for (int i = 0; i < n; i++) {
		printf("%d ", arr[i]);
	}
	printf("\n");
	return 0;
}
```
![image](https://github.com/user-attachments/assets/4d43f478-f489-4298-9352-bfe66dffc177)


3. 사용자로부터 n개의 정수값을 읽어서 배열에 저장하고, 배열의 모든 요소의 합을 계싼하여 출력하는 프로그램을 작성해보자.

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int n, arr[100], result=0;
	printf("입력할 정수의 개수: ");
	scanf("%d", &n);

	for (int i = 0; i < n; i++) {
		printf("%d번째 요소를 입력하시오: ", i);
		scanf("%d", &arr[i]);
	}

	for (int i = 0; i < n; i++) {
		result += arr[i];
	}
	printf("합=%d\n", result);
	return 0;
}
```
![image](https://github.com/user-attachments/assets/0226edb7-6b96-4be5-8daa-e309995e0469)


4. 사용자로부터 5개의 정수를 입력받아서 1차원 배열에 저장한다. 1차원 배열에서 최대값과 최솟값을 계산하여 출력해보자.

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int arr[5];
	for (int i = 0; i < 5; i++) {
		printf("정수를 입력하시오: ");
		scanf("%d", &arr[i]);
	}

	int max = arr[0];
	for (int i = 0; i < 5; i++) {
		if (arr[i] > max) {
			max = arr[i];
		}
	}

	int min = arr[0];
	for (int i = 0; i < 5; i++) {
		if (arr[i] < min) {
			min = arr[i];
		}
	}

	printf("최댓값: %d, 최솟값: %d\n", max, min);
	
	return 0;
}
```
![image](https://github.com/user-attachments/assets/ca603ec0-129c-4c44-b2ba-8de5bbb8ef75)


5. 학생들의 시험점수를 통계처리하는 프로그램을 작성하여 보라. 각 학생들은 3번의 시험을 치른다.
  1. 위의 표를 2차원 배열에 저장하여라
  2. 각 학생마다 평균 점수를 출력하도록 하여라
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int arr[3][3] = { {30, 10, 11},
		{40, 90, 32},
		{70, 65, 56} };

	int sum[3] = { 0, 0, 0 };
	int average[3] = { 0, 0, 0 };

	for (int i = 0; i < 3; i++) {
		for (int j = 0; j < 3; j++) {
			sum[i] += arr[i][j];
		}
	}

	for (int i = 0; i < 3; i++) {
		average[i] = sum[i] / 3;

		printf("%i번째 학생의 평균: %d점\n", i + 1, average[i]);
	}

	return 0;
}
```
![image](https://github.com/user-attachments/assets/5e972716-af7b-4609-8120-a5fd1a9cdd06)


6. 1단부터 9단까지의 구구단을 2차원 배열에 저장한다. 사용자로부터 구구단 중의 하나를 받아서 2차원 배열에서 찾는다. 찾은 결과를 화면에 출력하는 프로그램을 작성한다.

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int i, j;
	int gugu[10][10];

	//구구단 배열 저장
	for (i = 1; i <= 9; i++) {
		for (j = 1; j <= 9; j++) {
			gugu[i][j] = j;
			//printf("%3d ", j);
		}
		//printf("\n");
	}

	int n, m;
	int result = 1;
	printf("알고 싶은 구구단을 입력하세요: ");
	scanf("%d %d", &n, &m);
	
	for (i = 1; i <= 9; i++) {
		for (j = 1; j <= 9; j++) {
			if (gugu[i][j] == n || gugu[i][j] == m) {
				result = n * m;
			}
		}
	}

	printf("%d*%d=%d\n", n, m, result);
	return 0;
}
```
![image](https://github.com/user-attachments/assets/eb5f00f2-45b0-4ff4-95fb-0eee211690d9)


7. 두 개의 행렬을 곱하는 프로그램을 작성하시오.

```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	int mat1[3][3], mat2[3][3], mat[3][3];

	printf("행 개수=3\n");
	printf("열 개수=3\n");

	printf("첫 번째 행렬 입력=\n");
	scanf("%d %d %d\n%d %d %d\n%d %d %d", &mat1[0][0], &mat1[0][1], &mat1[0][2], &mat1[1][0], &mat1[1][1], &mat1[1][2], &mat1[2][0], &mat1[2][1], &mat1[2][2]);

	printf("\n두 번째 행렬 입력=\n");
	scanf("%d %d %d\n%d %d %d\n%d %d %d", &mat2[0][0], &mat2[0][1], &mat2[0][2], &mat2[1][0], &mat2[1][1], &mat2[1][2], &mat2[2][0], &mat2[2][1], &mat2[2][2]);
	printf("\n");

	for (int i = 0; i < 3; i++) {
		for (int j = 0; j < 3; j++) {
			mat[i][j] = (mat1[i][0] * mat2[0][i]) + (mat1[i][1] * mat2[1][i]) + (mat1[i][2] * mat2[2][i]);
		}
	}

	printf("%d %d %d\n%d %d %d\n%d %d %d\n", mat[0][0], mat[0][1], mat[0][2], mat[1][0], mat[1][1], mat[1][2], mat[2][0], mat[2][1], mat[2][2]);

	return 0;
}

```
![image](https://github.com/user-attachments/assets/6359c60d-08ac-465c-98d2-a36566800f0e)


8. 주어진 행렬의 전치 행렬을 계산하는 프로그램을 작성하라.
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int main() {
	printf("행 개수=3\n열 개수=3\n");

	int mat[3][3], matT[3][3];
	printf("행렬 입력=\n");
	scanf("%d %d %d\n%d %d %d\n %d %d %d",
		&mat[0][0], &mat[0][1], &mat[0][2],
		&mat[1][0], &mat[1][1], &mat[1][2],
		&mat[2][0], &mat[2][1], &mat[2][2]);
	printf("\n");

	for (int i = 0; i < 3; i++) {
		for (int j = 0; j < 3; j++) {
			matT[i][j] = mat[j][i];
			printf("%d ", matT[i][j]);
		}
		printf("\n");
	}
}
```
![image](https://github.com/user-attachments/assets/ccf74e05-220d-4532-81b3-4552e8ed6143)


9. 0부터 9까지 난수를 100번 생성하여 가장 많이 생성된 수를 출력하는 프로그램을 작성하시오. 난수는 rand()함수를 사용하여 생성하라. 배열을 사용해보자.
```c
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
#include<stdlib.h>

int main() {
	int a[10];
	int num, most;

	most = a[0];

	for (int i = 0; i < 100; i++) {
		num = rand() % 10;
		a[num] += 1;
	}

	for (int j = 0; j < 10; j++) {
		if (most < a[j]) {
			most = a[j];
			num = j;
		}
	}

	printf("가장 많이 생성된 수: %d\n", num);
	return 0;
}
```
![image](https://github.com/user-attachments/assets/a7e3bf68-9680-4ff4-b864-e516e3134d86)


