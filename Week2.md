### week2 실습 소스

구구단(1)
```c
# include <stdio.h>

int main() {

	int a = 0;
	printf("input a number :");
	scanf_s("%d", &a);

	for (int b = 1; b < 10; b++) {
		printf("%d X %d = %d\n", a, b, a*b);
	}

	return 0;
}
```

구구단(2)
```c
# include <stdio.h>

int main() {

	int column = 4;

	for (int c = 2; c < 10; c=c+ column) {
		for (int y = 1; y < 10; y++) {
			for (int x = 0; x < column; x++) {
				printf("%d X %d = %d\t", (c+x), y, (c+x)*y);
			}
			printf("\n");
		}
		printf("\n");
	}

	return 0;
}
```



로또번호 생성기
```c
# include <stdio.h>
# include <stdlib.h>
# include <time.h>

int main() {

	srand(time(NULL));

	for (int i = 0; i < 6; i++) {
		int number = (rand() % 45) + 1;
		printf("%d ", number);
	}

	printf("\n");

	return 0;
}
```

up or down(제한 없음)
```c
# include <stdio.h>
# include <stdlib.h>
# include <time.h>

int main() {

	srand(time(NULL));
	int answer = (rand() % 50) + 1; // 0 ~ 50까지 난수 생성

	while (1) {
		int input = 0;
		printf("input a number : ");
		scanf_s("%d", &input);

		if (input == answer) {

			printf("you win!!!\n");
			break;
		}
		else if (input > answer) {
			printf("down\n");
		}
		else if (input < answer) {
			printf("up\n");
		}
	}

	return 0;
}
```

up or down(10번 제한)
```c
# include <stdio.h>
# include <stdlib.h>
# include <time.h>

int main() {

	srand(time(NULL));
	int answer = (rand() % 50) + 1; // 0 ~ 50까지 난수 생성

	for (int i = 0; i<10; i++){

		int input = 0;
		printf("input a number : ");
		scanf_s("%d", &input);

		if (input == answer) {

			printf("you got it!!!\n");
			break;
		}
		else if (input > answer) {
			printf("down\n");
		}
		else if (input < answer) {
			printf("up\n");

		}
		printf("left %d time(s).\n", 10-(i+1));
	}

	return 0;
}
```

평균점수 계산기
```c
# include <stdio.h>

int main() {

	float averageScore = 0;
	int count = 0;

	while (1) {
		int input = 0;
		printf("input score : ");
		scanf_s("%d", &input);

		if (input != -1) {
			if (input >= 0 && input <= 100) {
				count++;
				averageScore += (float)input;
			}
			else {
				printf("[erorr] input correct value. the range of value is 0~100\n");
			}
		}
		else {
			if (count != 0) {
				printf("[result] the mean is %f\n", averageScore / (float)count);
				break;
			}
			else {
				printf("[erorr] cannot divide by zero.\n");
			}
		}
	}

	return 0;
}
```
