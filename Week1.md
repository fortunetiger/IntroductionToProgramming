### week1 실습 소스

Hello, world!
```c
# include <stdio.h>

int main() {
  printf("hello, world!\n");
  
  return 0;
}
```


덧셈 계산기
```c
# include <stdio.h>

int main() {

	int num1, num2, result = 0;

	printf("첫 번째 수: ");
	scanf_s("%d", &num1);

	printf("두 번째 수: ");
	scanf_s("%d", &num2);

	result = num1 + num2;

	printf("답 : %d\n", result);

	return 0;
}
```

나눗셈 계산기
```c
# include <stdio.h>

int main() {

	float num1, num2, result = 0;

	printf("첫 번째 수: ");
	scanf_s("%f", &num1);

	printf("두 번째 수: ");
	scanf_s("%f", &num2);

	result = num1 / num2;

	printf("답 : %f\n", result);

	return 0;
}
```
