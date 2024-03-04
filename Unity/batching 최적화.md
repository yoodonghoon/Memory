# Batch 란
Batch 배치작업은 데이터를 실시간으로 처리하는게 아니라, 일괄적으로 모아서 한번에 처리하는 작업을 의미합니다.

Draw Call뿐 아니라 그래픽을 구성하고 있는 데이터들도 묶어서 gpu한테 넘기는걸 Batch라고 합니다.

Draw call 과 Setpass Call를 알아야 하니 한번 알아보고 갑시다.

# Draw Call

 Cpu들이 데이터들을 가지고 있고 Gpu는 이걸 바탕으로 화면에 그려주는데
 
 Cpu에서 Gpu한테 이렇게 그려라 라고 명령하는게 Draw Call입니다

 Draw Call이 높을수록 역시나 부하도 올라갑니다.

 # Setpass Call

 Draw Call을 할때 Command buffer가 딸려 가는데 그중에서 그래픽 계열(Metarial, shader 등)을 묶어논 것을 Setpass 라고 하고 
 
 이걸 호출 하는게 Setpass Call이라고 합니다.

 # 최적화 방법
 - Single Material
 - Dynamic Batching
 - Static Batching
 - SRP Batching
 - GPU Instancing
