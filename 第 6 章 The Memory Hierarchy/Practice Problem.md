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

这三个函数都是完成同样的功能，将 struct 数组 **P** 传入函数，并将所有结构体的值置零。讨论这三个函数的空间局部性。

> Rank-order the functions with respect to the spatial locality enjoyed by each.

