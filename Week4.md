Pi 구하기(재귀문vs반복문)
```c
# include <stdio.h>
# include <math.h>

long double pi(int);

int main() {

	long double pi = 3.;
	for (int i = 0; i < 10000000; i++) {
		long double k = (long double)i + 1;
		pi+= (((-4) * pow(-1, k)) / ((2 * k) * (2 * k + 1) * (2 * k + 2)));
	}

	printf("%.60Lf\n", pi);
	return 0;
}

long double pi(int iteration){
	long double k = (long double)iteration;
	if (k == 0) return (long double)3;
	else return pi(k - 1) + (( (-4) * pow(-1, k) ) / ( (2*k) * (2*k + 1) * (2*k + 2) ));
}
```
