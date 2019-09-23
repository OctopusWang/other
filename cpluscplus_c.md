```
//test.h
#ifdef __cplusplus
#include <iostream>
using namespace std;
extern "C"
{
#endif
	void mytest();
#ifdef __cplusplus
}
#endif
```

```
//test.c
#include "test.h"
void mytest()
{
#ifdef __cplusplus
	cout << "cout mytest extern ok " << endl;
#else
	printf("printf mytest extern ok n");
#endif
}  
```

```
//main.cpp
#include "test.h"
int main()
{
	mytest();
	system("pause");
	return 0;
}
```
