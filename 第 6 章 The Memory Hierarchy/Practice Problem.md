## Practice Problem 6.8 (solution page 699)

An array of structs

```c
#define N 1000
typedef struct {
	int vel[3];
	int acc[3];
} point; point p[N];
void clear1(point *p, int n)
{
	int i, j;
	for (i = 0; i < n; i++) {
		for (j = 0; j < 3; j++)
			p[i].vel[j] = 0;
		for (j = 0; j < 3; j++)
			p[i].acc[j] = 0;
	}
}
void clear2(point *p, int n)
{
	int i, j;
	for (i = 0; i < n; i++) {
		for (j = 0; j < 3; j++) {
			p[i].vel[j] = 0;
			p[i].acc[j] = 0;
		}
	}
}
void clear3(point *p, int n)
{
	int i, j;
 	for (j = 0; j < 3; j++) {
 		for (i = 0; i < n; i++)
 			p[i].vel[j] = 0;
 		for (i = 0; i < n; i++)
			p[i].acc[j] = 0;
	}
}
```

