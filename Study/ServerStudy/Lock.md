# Lock

지역변수와 다르게 전역변수, 힙메모리, static변수들은 스레드들이 공통으로 사용한다.
  
그렇기 때문에 멀티스레드 방식에서 주의를 해야한다고 했었는데
  
이때 해당 변수를 소유해서 다른 스레드에서는 작업하지 못하게 선점(?)하는 계념이 바로 락이다.
  
![image](https://github.com/yoodonghoon/Memory/assets/145320150/90036fb4-e124-4683-bd86-9d79494d2183)


# SpinLock

만약 다른 스레드가 Lock을 소유하고 있다면 해당 Lock이 반환될때 까지 기다려야 하는데
  
이때 조금만 기다리면 쓸 수 있을거 같은데 컨텍스트 스위칭을 하면서 괜히 부하를 줄 필요가 있을까?에서 개발된 방법입니다.

![image](https://github.com/yoodonghoon/Memory/assets/145320150/cdffbc75-d467-43f0-bf3b-47d7a36676d3)

SpinLock 클래스를 만들어 주고 Acquire 함수에서 무한루프를 돌면서 기다려주는 방식입니다.

Acquire의 while문에서 Interlocked.CompareExchange 함수를 사용해서 현재 Lock값이 0인지 확인을 하는 겁니다.

0이라는 값이라면 아무도 사용하지 않는다고 판단하고 Lock을1로 변경해주고 while을 탈출합니다.

![image](https://github.com/yoodonghoon/Memory/assets/145320150/2713a7c8-3df9-4213-a9e2-6d822b448051)

실행시켜보시면 결과로 num도 0으로 잘 나오는 모습을 보여줍니다.
