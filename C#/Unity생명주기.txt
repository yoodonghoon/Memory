https://docs.unity3d.com/kr/2019.4/Manual/ExecutionOrder.html

더 자세히 보고 싶다면 위의 주소로 가서 보시면 됩니다.

일단 유니티 생명주기는

Awake -> OnEnable -> Start -> FixedUpadte -> Update ->LateUpdate -> OnDisable -> OnDestory
순으로 작동한다고 보시면 됩니다.

# Awake OnEnable Start 를 비교해보겠습니다.

- Awake
  - Awake 메서드는 스크립트 인스턴스가 생성될 때 호출됩니다.  
  - 스크립트의 인스턴스가 생성되고 초기화되는 시점에서 호출되기 때문에, 다른 MonoBehaviour 메서드보다 먼저 실행됩니다.
  - 리소스 초기화, 변수 초기화 등의 작업에 사용됩니다.
  - 다른 스크립트나 컴포넌트에 대한 초기 설정에 적합합니다.

- OnEnable
  - OnEnable 메서드는 스크립트나 게임 오브젝트가 활성화될 때마다 호출됩니다.
  - 즉, 해당 스크립트나 게임 오브젝트가 활성화되거나, gameObject.SetActive(true) 메서드가 호출될 때마다 실행됩니다.
  - 주로 오브젝트 풀링에 사용이 됩니다.

- Start
  - Start 메서드는 Awake 다음으로 호출되며, 모든 Awake 메서드가 실행된 후에 호출됩니다.
  - 따라서, 다른 스크립트나 컴포넌트의 초기화가 끝나고 게임 오브젝트의 상태가 안정화된 시점에서 호출됩니다.
  - 게임 시작 시 필요한 초기화 작업에 주로 사용됩니다.
