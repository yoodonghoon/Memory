# List / Dictionary

c#에서 가장 많이 쓰는 컨테이너 클래스들이 바로 List와 Dictionary라고 생각됩니다.

c++을 공부 하셨던 분들이라면

c++의 vector가 c#의 List

c++의 unordered_map이 c#의 Dictionary라고 보시면 됩니다.

List의 내부 구조는 배열로 이루어져 있으며

배열과 List의 차이점은 배열은 동적 할당이 불가능 한점이 있습니다.

시간복잡도는 O(n)을 가지고 있습니다.

Dictionary의 내부구조는 해시테이블로 이루어져있습니다.

해시테이블로 이루어져 있기때문에 시간복잡도는 O(1)을 가지고 있지만

항상 그런것은 아닙니다. 최악의 경우 O(n)이 될 수 있습니다.

# c++ map, c# sortedDictionary

c++의 map 레드블랙트리로 되어있어 Key값을 기준으로 항상 정렬 됩니다.

c#에서는 sortedDictionary가 같은 구조를 가지고 있는데

Dictionary와 sortedDictionary를 비교해보자면

삽입은 Dictionary가 압도적으로 빠르고

검색은 비슷한 속도를 가지고 있습니다.


그래서 항상 정렬된 상태로 데이터를 가지고 있어야 하는 경우가 아니라면

Dictionary를 사용하면 더 좋습니다.
