# Coroutine

코루틴은 비동기 프로그래밍을 필요로 할때 사용합니다.

보통 함수들과는 다르게 일시적으로 멈췄다가 다시 진행할 수 있습니다.


# 예제

![1](https://github.com/yoodonghoon/Memory/assets/145320150/232df5ad-94eb-4c24-8fea-98d5d5503497)

출력은 어떻게 나올까요??

![2](https://github.com/yoodonghoon/Memory/assets/145320150/3b4283b3-ee82-45a1-ab45-93896f51fdb3)

마지막 출력을 보면 

AnotherCoroutine Finished 이 출력된 후에

Coroutine Finished 출력된게 보이는데 

그렇다면 AnotherCoroutine 코루틴을 돌리는 도중에 (3초대기 하는중에)

StopCoroutine(MyCoroutine)을 호출하면 어떻게 될까요?

.......................................................

AnotherCoroutine Finished는 호출되지 않습니다.

의존성이 부여되기 때문에 그렇죠

이런 부분을 유의해줘서 개발을 하시면 됩니다.
