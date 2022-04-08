# c_pointer_practice

	point + er = pointer = ptr
	
	포인터는 메모리 주소를 저장하기 위한 변수

# ex 1)
```c++
// 타입* 포인터명
int* ptr;
int * ptr;
int *ptr;
int *ptr1, *ptr2;
```

# ex 2)
```c++
#include <iostream>

int main()
{
    int i = 1;
    int* p = &i;

    printf("i = %d\n", i);        // 1
    printf("i adr = %p\n", &i);   // 000000035793F714
    printf("p = %p\n", p);        // 000000035793F714
    printf("p adr = %p\n", &p);   // 000000035793F738

    return 0;
}
```

# 대충 구조는 이렇게..?
||000000035793F738 (address) ||000000035793F714 (address) |
---|---|---|---|
|p|000000035793F714|i|1|

# 이렇다고 한다..
```c++
    printf("%d", *&i == i);   // 1 => true
    printf("%d", &*p == p);   // 1 => true
```
