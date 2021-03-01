### 1000보다 작은 소수 찾기
```c
# include <stdio.h>

int main() {

	for (int i = 0; i < 1000; i++) {
		int num = i + 1;
		
		for (int n = num - 1; n > 0; n--) {
			if (n == 1) printf("%d ", num);
			else if (num % n == 0) break;
			else continue;
		}
	}
	return 0;
}
```

### 종강 타이머 만들기
```c
# include <stdio.h>
# include <time.h>
# include <Windows.h>
int main() {

	unsigned int jonggang = 1624276800;

	while (1) {

		time_t current;
		time(&current);

		int left_time = (int)(jonggang - current);
		if (left_time <= 0) {
			printf("Happy jonggang!\n");
			break;
		}

		int days = left_time / (24 * 60 * 60);
		left_time %= (24 * 60 * 60);

		int hour = left_time / (60 * 60);
		left_time %= (60 * 60);

		int min = left_time / 60;
		left_time %= 60;

		int sec = left_time;

		printf("%ddays %dhour %dmin %dsec letf until jonggang...\n" , days, hour, min, sec);
		Sleep(1000);
		
		system("cls");
	}

	return 0;
}
```

### 2진수 변환기
```c
# include <stdio.h>

int main() {

	int input = 0;
	printf("input the decimal number to convert into bibary : ");
	scanf_s("%d", &input);

	printf("binary : ");
	while (input >= 1) {
		printf("%d", input % 2);
		input>>=1 ;
	}
	printf("\n");

	return 0;
}
```
