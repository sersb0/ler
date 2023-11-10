

#include "stdafx.h"
#include <stdlib.h>


int _tmain(int argc, _TCHAR* argv[])
{
	int a[8];
	int n = sizeof(a) / sizeof(a[0]);
	for (int i = 0; i < n; i++)
	{
		a[i] = rand();
	}
	for (int i = 0; i < n; i++)
	{
		printf("%d\n", a[i]);
	}
	printf("\nSort:\n");

	for (int j = 0; j < n; j++)
	{
		int s;
		for (int i = 0; i < n - 1; i++)
		{
			if (a[i] > a[i + 1])
			{
				s = a[i];
				a[i] = a[i + 1];
				a[i + 1] = s;
			}
		}
		printf("%d\n", a[j]);
	}

	printf("sort:\n");
	for (int j = 0; j < n; j++)
	{
		int s;
		for (int i = 0; i < n - j - 1; i++)
		{
			if (a[i] < a[i + 1])
			{
				s = a[i];
				a[i] = a[i + 1];
				a[i + 1] = s;
			}
		}
		printf("%d\n", a[j]);
	}
	return 0;
}
