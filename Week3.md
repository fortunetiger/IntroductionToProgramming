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
