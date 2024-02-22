코루틴 대신 Unitask를 많이 쓰는데 한번 같이 보시죠

https://github.com/Cysharp/UniTask

# Unitask

Unitask도 코루틴과 마찬가지로 비동기 프로그래밍에 쓰이는 라이브러리입니다.

비동기 작업을 더 효과적으로 사용할 수 있게 해주는데 도움이 됩니다.

#특징
- 비동기 작업 처리
  - Unitask는 async 및 await 키워드를 사용하여 비동기 작업을 보다 간편하게 처리할 수 있게 합니다.
  - 예를 들어, await Unitask.Delay(1000)은 1초 동안 대기하는 비동기 작업을 수행합니다.
    
- 코루틴 처리
  - Unitask는 코루틴을 지원하며, await UniTask.Yield()와 같은 키워드를 사용하여 간단하게 코루틴을 구현할 수 있습니다.
  - 코루틴 작성 시, UniTask.Yield() 대신 await를 사용하여 작업을 중단하고 다음 프레임까지 대기할 수 있습니다.
    
- 취소 및 예외 처리
  - Unitask는 비동기 작업 취소 및 예외 처리를 간편하게 다룰 수 있도록 지원합니다.
  - UniTask.WhenAll, UniTask.WhenAny와 같은 메서드를 사용하여 여러 작업을 처리하고 결과를 기다릴 수 있습니다.

- 성능 최적화
  - Unitask는 성능을 최적화하여 메모리 할당을 최소화하고 GC(Garbage Collection) 부하를 감소시킵니다.
  - 또한 코루틴의 관리 및 스케줄링을 더 효율적으로 수행합니다.
