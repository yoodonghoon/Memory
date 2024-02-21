#Boxing, UnBoxing

- Boxing은 값 형싱을 참조형식으로 바꾸는 것이고
- unBoxing은 반대로 참조형식을 값 형식으로 바꾸는것이다.

int a= 42;

// Boxing
object b= a

// Unboxing
int c= (int)b;

위의 예제를 보면 좀 이해가 갈것입니다.

이게 가능한 이유가 뭐냐면

c#의 모든 형식은 System.Object를 상속 받기 때문에 가능한 것인데

무심코 썼다가는 큰일이 납니다.

boxing을 하게되면 힙에 새로운 객체로 할당이 되어서 메모리를 할당하거나 해제할때에 비용이 발생되고
unboxing은 형식 변환작업이 수행되기 때문에 성능저하가 일어나기에 사용하면 안됩니다.

이를 피하기 위해 만들어진게 [Generic]() 입니다.